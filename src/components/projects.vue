<template>
  <v-container fluid>
    <h3 class="specialityText">.Projects</h3>
    <v-row >
      <v-col v-for="(project, index) in projectList" cols="12" lg="4" md="4" sm="12" xs="12">
        <v-card
          color="#fff"
        >
          <v-card-item :key="index">
            <v-card-title class="text-black">
              {{ project.skillTitle }}
            </v-card-title>
            <v-card-subtitle class="text-black"
              >Tech Stake : {{ project.category }}
            </v-card-subtitle>
          </v-card-item>

          <v-card-text class="">
            {{ project.description }}
            <v-btn variant="text" size="small" :href="project.url" class="font-weight-bold" color="red">VISIT</v-btn>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
        
  </v-container>
</template>

<script setup>
import {ref} from "vue";

  const projectList = ref([
        {
          id: 1,
          skillTitle: "Supply Chain Connect (WIP)",
          category: "NodeJS, VueJS, MongoDB and OpenAI",
          description:"Supply Chain connect is an e-commerce platform that provides remarkable opportunities throughtout the medical supply chain. Manufacturers, retailers, logistics and human resources are interdepended and given the platform are able to render each other service support that promote business.",
          url:"https://easybizyview.vercel.app/"
        },
        {
          id: 2,
          skillTitle: "Grilling Road Hideout (WIP)",
          category: "NodeJS, VueJS and MongoDB",
          description:"Grilling Road Hideout website is an e-commerce platform owned by Grilling Road Hideout resort company. The platform was created to sell represent the company in the virtual world handling product purchases and profer company information primarily",
          url:"https://grillingroadhideout.vercel.app/"
        },
        {
          id: 3,
          skillTitle: "Maxmusic",
          category: "NodeJs, ReactJS and MongoDB",
          description:"A music listening platform created to bring musicians and listeners together. Maxmusic give both the renowned and upcoming artist a platform to reach a wider audience from allover the world, providing a means to earn royalties.",       
          url:"https://maxmusic.vercel.app/"
        },
         {
          id: 4,
          skillTitle: "Bible Quiz (WIP)",
          category: "NodeJs, ReactJS and MongoDB",
          description:"A music listening platform created to bring musicians and listeners together. Maxmusic give both the renowned and upcoming artist a platform to reach a wider audience from allover the world, providing a means to earn royalties.",       
          url:"https://bible-quiz-app-peach.vercel.app/"
        },
         {
          id: 5,
          skillTitle: "November Trust (WIP)",
          category: "NodeJs, ReactJS and MongoDB",
          description:"A music listening platform created to bring musicians and listeners together. Maxmusic give both the renowned and upcoming artist a platform to reach a wider audience from allover the world, providing a means to earn royalties.",       
          url:"https://novembertrust.vercel.app/"
        },
         {
          id: 6,
          skillTitle: "ZEUC (WIP) - closed",
          category: "NodeJs, ReactJS and MongoDB",
          description:"A music listening platform created to bring musicians and listeners together. Maxmusic give both the renowned and upcoming artist a platform to reach a wider audience from allover the world, providing a means to earn royalties.",       
          url:"https://zeuc.vercel.app/"
        },
         {
          id: 7,
          skillTitle: "Yeshua (WIP)",
          category: "NodeJs, ReactJS and MongoDB",
          description:"A music listening platform created to bring musicians and listeners together. Maxmusic give both the renowned and upcoming artist a platform to reach a wider audience from allover the world, providing a means to earn royalties.",       
          url:"https://yeshuafront.vercel.app/"
        },
         {
          id: 8,
          skillTitle: "Roof World",
          category: "NodeJs, ReactJS and MongoDB",
          description:"A music listening platform created to bring musicians and listeners together. Maxmusic give both the renowned and upcoming artist a platform to reach a wider audience from allover the world, providing a means to earn royalties.",       
          url:"https://roofworld.vercel.app/"
        },
         {
          id: 9,
          skillTitle: "Yunxi Group Website",
          category: "NodeJs, ReactJS and MongoDB",
          description:"A music listening platform created to bring musicians and listeners together. Maxmusic give both the renowned and upcoming artist a platform to reach a wider audience from allover the world, providing a means to earn royalties.",       
          url:"https://yunxi.vercel.app/"
        }
      ])
      
    

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
