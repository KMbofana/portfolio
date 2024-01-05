<template>
  <div class="container">
    <h3 class="specialityText">.Speciality</h3>

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
      </v-card>
    </div>
  </div>
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
  margin-top: 10px;
}
.cardsDisplay {
  display: flex;
  flex-wrap: wrap;
  width: 80%;

  /* justify-content: space-between; */
  /* justify-content: center;
  margin-left: 20px; */
}
.cardBG {
  background-color: rgb(32, 29, 29);
  margin: 10px;
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
.container {
  width: 80%;
  margin-left: 5px;
}
</style>
