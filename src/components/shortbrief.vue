<template>
  <div class="container">
    <div class="imageProfile">
      <img src="../assets/me.jpg" aspect-ratio="1" class="image" cover />
    </div>
    <div class="nameCont">
      <h1 class="hOne">
        I'm Keith Anesu Mbofana
        <span class="profession">.Systems Developer (ICT)</span>
      </h1>
    </div>

    <v-sheet class="shortMe">
      I am a passionate developer with a keen interest in technology. I love
      programming and enjoy exploring new technologies and frameworks. I am
      always looking for ways to improve my skills and stay up-to-date with the
      latest trends in the industry. I am a quick learner and enjoy working on
      challenging projects that push me to my limits. I am a team player and
      enjoy collaborating with others to achieve common goals. I am excited
      about the future of technology and look forward to being a part of it.
    </v-sheet>

    <Service />
  </div>
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
  color: aliceblue;
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
.shortMe {
  width: 49vw;
  justify-self: left;
  border: 1px;
  border-style: solid;
  border-color: aqua;
  color: aliceblue;
  padding: 10px;
  margin: auto;
  /* margin-left: 50px; */
  margin-top: 2%;
  border-radius: 2px;
  background-color: transparent;
}
.container {
  display: flex;
  flex-direction: column;
  margin-left: 50px;
  /* overflow: scroll; */
  position: relative;
  height: 100vh;
  width: 100vw;
  /* background-color: brown; */
}
.imageProfile {
  height: 35vh;
  width: 32vh;
  border-radius: 100%;
  position: absolute;
  background-color: beige;
  margin-left: 50px;
  margin-top: 40px;
}
.image {
  height: 35vh;
  width: 32vh;
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
</style>
