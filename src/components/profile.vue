<template>
   <v-container fluid class="pa-0 fill-height">
    <v-row class="fill-height">
      <v-col cols="12" class="pa-0">
        <Shortbrief />
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import Shortbrief from "./shortbrief.vue";


export default {
  name: "PortifolioProfile",

  data() {
    return {};
  },

  mounted() {},

  components: {
    Shortbrief,
  },

  methods: {},
};
</script>

<style scoped>

</style>
