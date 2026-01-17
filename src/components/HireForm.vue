<template>
  <div class="pa-4 text-center">
    <v-card prepend-icon="mdi-calendar" title="Schedule A Meeting">
      <v-card-text>
        <v-row dense>
          <v-col cols="12" md="6" sm="12">
            <v-text-field label="First name*" v-model="firstName" :rules="[rules.required]"></v-text-field>
          </v-col>


          <v-col cols="12" md="6" sm="12">
            <v-text-field
              label="Last name*"
              persistent-hint
              v-model="lastName"
              :rules="[rules.required]"
            ></v-text-field>
          </v-col>

          <v-col cols="12" md="4" sm="12">
            <v-text-field label="Email*" v-model="email" :rules="[rules.email,rules.emailValidation]"></v-text-field>
          </v-col>


          <v-col cols="12" md="4" sm="12">
            <v-text-field
              label="Phone*"
              v-model="phone"
              type="text"
              :rules="[rules.required]"
            ></v-text-field>
          </v-col>
          <v-col cols="12" md="4" sm="12">
            <v-text-field
              label="Date*"
              v-model="date"
              type="date"
              :rules="[rules.required]"
            ></v-text-field>
          </v-col>

         

          <v-col cols="12" sm="12">
            <v-textarea v-model="meetingDetails" :rules="[rules.required]" label="Meeting Details"></v-textarea>
          </v-col>
        </v-row>

        <small class="text-caption text-medium-emphasis"
          >*indicates required field</small
        >
      </v-card-text>

      <v-divider></v-divider>

      <v-card-actions>
        <v-spacer></v-spacer>

        <v-btn text="Close" variant="plain" @click="closeDialog"></v-btn>

        <v-btn
          color="#1B1B1B"
          text="Share Schedule"
          variant="flat"
          @click="sendSchedule"
        ></v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>
<script setup>
  import {ref} from "vue";
  import axios from "axios";

  const firstName = ref("");
  const lastName = ref("");
  const email = ref("");
  const phone = ref("");
  const date = ref("");
  const meetingDetails = ref("");

  const rules = {
    required:v => !!v || "Field is required",
    email: v => !!v || 'Email is required',
    emailValidation:v => /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(v) || 'Invalid email',
  }

  const emit = defineEmits(['close-dialog'])

const closeDialog = ()=>{
  emit('close-dialog')
}

const sendSchedule = async() =>{
  try {
    const data = {
      firstName:firstName.value,
      lastName:lastName.value,
      email:email.value,
      phone:phone.value,
      date:date.value,
      meetingDetails:meetingDetails.value
    }
    const config =  {
      method:"post",
      data,
      url:'https://bible-quiz-backend-yysg.onrender.com/api/emails',
    }

    const result = await axios.request(config);
    console.log(result)
  } catch (error) {
    console.error(error);
  }
}
</script>
