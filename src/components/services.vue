<template>
  <v-container class="serviceContainer">
    <h3 class="specialityText">.Speciality</h3>
    <div class="container">
      <div class="cardsDisplay">
        <v-card
          class="cardBG my-8"
          max-width="344"
          elevation="16"
          v-for="developerSkill in developerSkills"
        >
          <v-card-item>
            <v-card-title class="cardTitle">
              {{ developerSkill.skillTitle }}
            </v-card-title>
            <v-card-subtitle class="cardSubTitle"
              >{{ developerSkill.category }}
            </v-card-subtitle>
          </v-card-item>

          <v-card-text class="cardText">
            {{ developerSkill.description }}
          </v-card-text>
          <div class="hireMeBtns">
            <v-btn rounded="xs" size="large">Hire Me</v-btn>
          </div>
        </v-card>
      </div>
    </div>
  </v-container>
</template>

<script>
export default {
  name: "PortifolioServices",
  developerSkills: [],

  data() {
    this.developerSkills = [
      {
        skillTitle: "Full-stack Web Development",
        category: "websites and web applications",
        description:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
      },
      {
        skillTitle: "UI/UX Design",
        category: "Adobe XD and Figma",
        description:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
      },
      {
        skillTitle: "APIs",
        category: "PHP, Python, Node.JS, Java",
        description:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
      },
    ];
    return {};
  },

  mounted() {},

  methods: {},
};
</script>

<style scoped>
.specialityText {
  color: aliceblue;
  margin-left: 35px;
  font-family: cursive;
  font-size: 0.5in;
  /* margin-top: 10px; */
}
.cardsDisplay {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 100vw;
}
.cardBG {
  background-color: rgb(32, 29, 29);
  /* margin: 10px; */
}

.cardTitle {
  color: aliceblue;
}
.cardSubTitle {
  color: aliceblue;
}
.cardText {
  color: aliceblue;
}
.serviceContainer {
  margin-left: 10vh;
  /* background-color: rgb(125, 124, 124); */
  border-radius: 5px;
}
.container {
  display: flex;
  position: relative;
}
.hireMeBtns {
  display: flex;
  justify-content: flex-end;
  margin: 10px;
}
</style>
