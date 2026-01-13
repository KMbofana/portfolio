<template>
  <v-container fluid>
    <h3 class="specialityText">.Speciality</h3>
    <v-row >
      <v-col v-for="(developerSkill, index) in developerSkills" cols="12" lg="4" md="4" sm="12" xs="12">
        <v-card
          color="#fff"
        >
          <v-card-item :key="index">
            <v-card-title class="text-black">
              {{ developerSkill.skillTitle }}
            </v-card-title>
            <v-card-subtitle class="text-black"
              >{{ developerSkill.category }}
            </v-card-subtitle>
          </v-card-item>

          <v-card-text class="">
            {{ developerSkill.description }}
          </v-card-text>
          <v-card-actions class="d-flex justify-end" no-data>
            <v-btn variant="flat" size="small" href="https://wa.me/263779363209" class="font-weight-bold" color="red">Request Service</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
        
  </v-container>
  <Project />
</template>

<script>
import HiringForm from "./HireForm.vue";
import Project from "./projects.vue";

export default {
  name: "PortifolioServices",
  developerSkills: [],

  data() {
    return {
      developerSkills: [
        {
          id: 1,
          skillTitle: "APIs",
          category: "PHP, Python, Node.JS, Java",
               description:
            "Highly skilled developer with 5+ years of experience in designing, developing, and deploying scalable APIs using Java, Node.js, PHP, and Python. Proficient in creating RESTful APIs, microservices, and cloud-native applications. Strong understanding of API security, performance optimization, and versioning. Proficient in Agile development methodologies and collaborative version control systems like Git.",
  },
        {
          id: 2,
          skillTitle: "Full-stack Web Development",
          category: "websites and web applications",
                 
          description:
            "Developing intutitive web applications and websites is my drive. I have worked with react and laravel on a couple of applications for the companies i have worked for. This year am exploring the beauty of Vue js ✨",
      
      },
        {
          id: 3,
          skillTitle: "UI/UX Design",
          category: "Adobe XD, Figma and Illustrator",
               description:
            "Aesthetical and user friendly designs are my motive. I work with Adobe XD, Figma and Adobe Illustrator as my magical tools 💪. Several other tools available for exploitation upon research ",
       
      },
      ],
      dialog: false,
    };
  },

  mounted() {},

  methods: {},

  components: {
    HiringForm,
    Project
  },
};
</script>

<style scoped>
.specialityText {
  color: #000;
  font-family: cursive;
  font-size: 0.5in;
  /* margin-top: 10px; */
}

.serviceContainer {
  /* margin-left: 2vh; */
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
