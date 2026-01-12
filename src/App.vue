<script setup>
import { ref, watch } from 'vue'
import { useDisplay } from 'vuetify'
import Profile from "./components/profile.vue"
import SideView from "./components/SideView.vue"

const { mdAndUp } = useDisplay()
const drawer = ref(mdAndUp.value)

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

      <div class="d-flex w-100 justify-end mr-4 ">
        <img src="./assets/me.jpg" class="rounded-circle border" height="60" width="60"/>
      </div>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      :permanent="mdAndUp"
    >
      <SideView />
    </v-navigation-drawer>

    <v-main>
      <Profile />
    </v-main>
  </v-app>
</template>
