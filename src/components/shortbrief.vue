<template>
  <v-container class="container">
    <div class="imageProfile">
      <img src="../assets/me.jpg" aspect-ratio="1" class="image" cover />
    </div>
    <div class="container2">
      <div class="nameCont">
        <h1 class="hOne">
          I'm Keith Anesu Mbofana
          <span class="profession">.Systems Developer (ICT)</span>
        </h1>
      </div>

      <v-sheet class="shortMe">
        I am a passionate developer with a keen interest in technology. I love
        programming and enjoy exploring new technologies and frameworks. I am
        always looking for ways to improve my skills and stay up-to-date with
        the latest trends in the industry. I am a quick learner and enjoy
        working on challenging projects that push me to my limits. I am a team
        player and enjoy collaborating with others to achieve common goals. I am
        excited about the future of technology and look forward to being a part
        of it.
      </v-sheet>
    </div>
  </v-container>

  <div class="mobileSkills">
    <table class="tableDesign">
      <tr class="rowsDesign">
        <td class="dataText">Node.JS</td>
        <td class="dataText">
          <v-progress-linear
            color="white"
            model-value="100"
          ></v-progress-linear>
        </td>
      </tr>
      <tr class="rowsDesign">
        <td class="dataText">PHP</td>
        <td class="dataText">
          <v-progress-linear
            color="white"
            model-value="100"
          ></v-progress-linear>
        </td>
      </tr>
      <tr class="rowsDesign">
        <td class="dataText">Python</td>
        <td class="dataText">
          <v-progress-linear
            color="white"
            model-value="100"
          ></v-progress-linear>
        </td>
      </tr>
      <tr class="rowsDesign">
        <td class="dataText">HTML</td>
        <td class="dataText">
          <v-progress-linear
            color="white"
            model-value="100"
          ></v-progress-linear>
        </td>
      </tr>

      <tr class="rowsDesign">
        <td class="dataText">CSS</td>
        <td class="dataText">
          <v-progress-linear
            color="white"
            model-value="100"
          ></v-progress-linear>
        </td>
      </tr>
      <tr class="rowsDesign">
        <td class="dataText">Javascript</td>
        <td class="dataText">
          <v-progress-linear
            color="white"
            model-value="100"
          ></v-progress-linear>
        </td>
      </tr>
      <tr class="rowsDesign">
        <td class="dataText">VueJS</td>
        <td class="dataText">
          <v-progress-linear color="white" model-value="80"></v-progress-linear>
        </td>
      </tr>
      <tr class="rowsDesign">
        <td class="dataText">React JS</td>
        <td class="dataText">
          <v-progress-linear
            color="white"
            model-value="100"
          ></v-progress-linear>
        </td>
      </tr>
      <tr class="rowsDesign">
        <td class="dataText">MySQL</td>
        <td class="dataText">
          <v-progress-linear
            color="white"
            model-value="700"
          ></v-progress-linear>
        </td>
      </tr>
      <tr class="rowsDesign">
        <td class="dataText">Java</td>
        <td class="dataText">
          <v-progress-linear color="white" model-value="60"></v-progress-linear>
        </td>
      </tr>
      <tr class="rowsDesign">
        <td class="dataText">MongoDB</td>
        <td class="dataText">
          <v-progress-linear color="white" model-value="60"></v-progress-linear>
          <v-progress-circular> </v-progress-circular>
        </td>
      </tr>
      <tr class="rowsDesign">
        <td class="dataText">.Net</td>
        <td class="dataText">
          <v-progress-linear color="white" model-value="40"></v-progress-linear>
        </td>
      </tr>
    </table>
  </div>
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
  width: 48vw;
  justify-self: left;

  color: aliceblue;
  padding: 10px;
  margin-top: 2%;
  border-radius: 2px;
  background-color: transparent;
}
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin-left: 10vh;
  /* background-color: blueviolet; */
  width: 100vw;
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
  height: 40vh;
  width: 40vh;
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

.mobileSkills {
  display: none;
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

  .mobileSkills {
    display: flex;
    justify-content: center;
    /* background-color: brown; */
  }
  .tableDesign {
    width: 60%;
  }
  .shortMe {
    width: 80%;
  }
}
</style>
