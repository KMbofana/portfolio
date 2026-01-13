<script setup>
import { ref, watch } from 'vue'
import { useDisplay } from 'vuetify'
import Profile from "./components/profile.vue"
import SideView from "./components/SideView.vue"

const { mdAndUp } = useDisplay()
const drawer = ref(mdAndUp.value)
 const overlay = ref(false)

watch(mdAndUp, val => {
  drawer.value = val
})

const openDrawer = () => {
  drawer.value = !drawer.value
}
</script>

<template>
  <v-app>
    <v-app-bar>
      <v-btn icon color="#1B1B1B" @click="openDrawer">
        <v-icon>mdi-menu</v-icon>
      </v-btn>

      <div class="d-flex w-100 justify-end mr-4">
        <v-btn icon height="60" width="60">
          <img src="./assets/me.jpg" class="rounded-circle border" height="60" width="60" @click="overlay = !overlay"/>
        </v-btn>
      </div>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      :permanent="mdAndUp"
    >
      <SideView />
    </v-navigation-drawer>
    <v-overlay v-model="overlay" class="d-flex fill-height align-center justify-center">
          <img
            src="./assets/me.jpg"
            class="rounded-circle border"
            height="300"
            width="300"
            
          />
          <h1 class="text-center text-white">Hey It's Keith</h1>
    </v-overlay>
    <v-main>
      <Profile />
    </v-main>
  </v-app>
</template>
