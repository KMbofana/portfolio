<template>
<v-container fluid class="pa-0">
  <v-sheet class="container position-relative pa-6" elevation="4" >
    <div class="">
      
        <h1 class="text-h6 text-wrap font-weight-bold">
          Name: Keith Anesu Mbofana
        </h1>
        <p class="text-h6 font-weight-bold">Job Profession: Software Engineer</p>

      <p class="text-wrap text-justify">
        I am a passionate developer with a keen interest in technology. I love
        programming and enjoy exploring new technologies and frameworks. I am
        always looking for ways to improve my skills and stay up-to-date with
        the latest trends in the industry. I am a quick learner and enjoy
        working on challenging projects that push me to my limits. I am a team
        player and enjoy collaborating with others to achieve common goals. I am
        excited about the future of technology and look forward to being a part
        of it.
      </p>
    </div>
   </v-sheet>
  </v-container>

  <Service />
</template>

<script>
import Service from "./services.vue";

export default {
  name: "PortifolioShortbrief",

  data() {
    return {};
  },

  mounted() {},

  components: {
    Service,
  },

  methods: {},
};
</script>

<style scoped>
.hOne {
  color: aqua;
  font-family: cursive, "Lucida Sans", Arial, sans-serif;
  font-weight: bold;
  font-size: 0.7in;
  font-style: italic;
}
.profession {
  color: #000;
  font-size: xx-large;
  font-variant-caps: titling-caps;
  text-decoration: wavy;
}
.nameCont {
  display: flex;
  flex-wrap: wrap;
  width: 50vw;
  align-self: center;
  justify-self: center;
  margin: auto;
}
.container {
  display: flex;
  flex-direction: row;
  width: 100%;
  /* background-color: blueviolet; */
}
.container2 {
  display: flex;
  flex-direction: column;
}
.imageProfile {
  display: flex;
  justify-content: center;
  /* background-color: beige; */
  width: 100%;
}
.image {
  /* height: 50vh; */
  /* width: 40vh; */
  border-radius: 100%;
}

.mySkills {
  padding: 15px;
  margin-left: 5px;
  margin-top: 30px;
}
.skillsTitle {
  color: aliceblue;
  font-weight: bold;
}
.skillsPills {
  background-color: aqua;
  color: black;
  padding: 8px;
  border-radius: 20px;
  margin: 5px;
  font-size: small;
}
.skillsContainer {
  display: flex;
  flex-wrap: wrap;
  margin: 10px;
}



@media (max-width: 768px) {
  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-left: 0%;
  }
  .imageProfile {
    margin-left: 0px;
  }
  .nameCont {
    align-self: self-start;
    justify-self: self-start;
    width: 60vw;
    margin: 0%;
  }
  .hOne {
    color: aqua;
    font-family: cursive, "Lucida Sans", Arial, sans-serif;
    font-weight: bold;
    font-size: 0.5in;
    font-style: italic;
  }

  .tableDesign {
    width: 60%;
  }

}
</style>
