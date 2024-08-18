<template>
  <v-container class="serviceContainer">
    <h3 class="specialityText">.Speciality</h3>
    <div class="container">
      <div class="cardsDisplay">
        <v-card
          class="cardBG my-8"
          max-width="344"
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
          "Developing intutitive web applications and websites is my drive. I have worked with react and laravel on a couple of applications for the companies i have worked for. This year am exploring the beauty of Vue js ✨",
      },
      {
        skillTitle: "UI/UX Design",
        category: "Adobe XD, Figma and Illustrator",
        description:
          "Aesthetical and user friendly designs are my motive. I work with Adobe XD, Figma and Adobe Illustrator as my magical tools 💪. Several other tools available for exploitation upon research ",
      },
      {
        skillTitle: "APIs",
        category: "PHP, Python, Node.JS, Java",
        description:
          "Highly skilled developer with 5+ years of experience in designing, developing, and deploying scalable APIs using Java, Node.js, PHP, and Python. Proficient in creating RESTful APIs, microservices, and cloud-native applications. Strong understanding of API security, performance optimization, and versioning. Proficient in Agile development methodologies and collaborative version control systems like Git.",
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
  margin-left: 60px;
  font-family: cursive;
  font-size: 0.5in;
  /* margin-top: 10px; */
}
.cardsDisplay {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 80vw;
  margin-left: 60px;
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

@media (max-width: 768px) {
  .serviceContainer {
    margin-left: 0%;
  }
}
</style>
