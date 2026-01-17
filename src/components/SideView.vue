<template>
      <v-card> 
              <v-table density="compact" class="" color="#F4F4F4">
                <thead style="background-color: #1B1B1B;">
                  <tr style="color: #fff" class="">
                    <th>Country:</th>
                    <th>Zimbabwe</th>
                  </tr>
                  <tr style="color: #fff" class="">
                    <th>City:</th>
                    <th>Harare</th>
                  </tr>
                  <tr style="color: #fff" class="">
                    <th>Age:</th>
                    <th>{{ age }}</th>
                  </tr>
                </thead>
                <tbody>
                    <tr>
                      <td class="text-center font-weight-bold" colspan="2">Front-End</td>
                    </tr>
                    <tr class="rowsDesign">
                      <td class="dataText">HTML</td>
                      <td class="dataText">
                        <v-progress-linear
                          color="#707678"
                          model-value="100"
                        ></v-progress-linear>
                      </td>
                    </tr>

                    <tr class="rowsDesign">
                      <td class="dataText">CSS</td>
                      <td class="dataText">
                        <v-progress-linear
                          color="#707678"
                          model-value="100"
                        ></v-progress-linear>
                      </td>
                    </tr>
                    <tr class="rowsDesign">
                      <td class="dataText">VueJS</td>
                      <td class="dataText">
                        <v-progress-linear
                          color="#707678"
                          model-value="100"
                        ></v-progress-linear>
                      </td>
                    </tr>
                    <tr class="rowsDesign">
                      <td class="dataText">React JS</td>
                      <td class="dataText">
                        <v-progress-linear
                          color="#707678"
                          model-value="100"
                        ></v-progress-linear>
                      </td>
                    </tr>
                  <tr>
                      <td class="text-center font-weight-bold" colspan="2">Back-End</td>
                    </tr>
                    <tr class="rowsDesign">
                      <td class="dataText">Node.JS</td>
                      <td class="dataText" width="100">
                        <v-progress-linear
                          color="#707678"
                          model-value="100"
                        ></v-progress-linear>
                      </td>
                    </tr>
                    <tr class="rowsDesign">
                      <td class="dataText">PHP</td>
                      <td class="dataText">
                        <v-progress-linear
                          color="#707678"
                          model-value="100"
                        ></v-progress-linear>
                      </td>
                    </tr>
                    <tr class="rowsDesign">
                      <td class="dataText">Python</td>
                      <td class="dataText">
                        <v-progress-linear
                          color="#707678"
                          model-value="100"
                        ></v-progress-linear>
                      </td>
                    </tr>
                    <tr class="rowsDesign">
                      <td class="dataText">Java</td>
                      <td class="dataText">
                        <v-progress-linear
                          color="#707678"
                          model-value="50"
                        ></v-progress-linear>
                      </td>
                    </tr>
                    <tr>
                      <td class="text-center font-weight-bold" colspan="2">Database</td>
                    </tr>
                    <tr class="rowsDesign">
                      <td class="dataText">MongoDB</td>
                      <td class="dataText ml-4">
                        <v-progress-linear
                          color="#707678"
                          :model-value="100"
                        ></v-progress-linear>
                      </td>
                    </tr>
                    <tr class="rowsDesign">
                      <td class="dataText">Firebase</td>
                      <td class="dataText ml-4">
                        <v-progress-linear
                          color="#707678"
                          :model-value="100"
                        ></v-progress-linear>
                      </td>
                    </tr>
                    <tr class="rowsDesign">
                      <td class="dataText">MySQL</td>
                      <td class="dataText ml-4">
                        <v-progress-linear
                          color="#707678"
                          :model-value="100"
                        ></v-progress-linear>
                      </td>
                    </tr>
                     <tr class="rowsDesign">
                      <td class="dataText">PostgresSQL</td>
                      <td class="dataText">
                        <v-progress-linear
                          color="#707678"
                          model-value="700"
                        ></v-progress-linear>
                      </td>
                    </tr>
                    <tr>
                      <td class="text-center font-weight-bold" colspan="2">Version Controls</td>
                    </tr>
                    <tr class="rowsDesign">
                      <td class="dataText">Git</td>
                      <td class="dataText">
                        <v-progress-linear
                          color="#707678"
                          model-value="100"
                        ></v-progress-linear>
                      </td>
                    </tr>
                    </tbody>
                  </v-table>              
      <v-btn rounded="xs" block color="#1B1B1B" class="text-white" @click="dialog = !dialog">Schedule Meeting</v-btn>
    </v-card>
<v-dialog v-model="dialog">
  <HireForm @close-dialog="closeDialog"/>
</v-dialog>

</template>

<script setup>
import { ref } from 'vue';
import HireForm from './HireForm.vue';

const dialog = ref(false)


const age = new Date().getFullYear() - 1996;

const closeDialog = ()=>{
  dialog.value = false;
}

</script>

<style scoped>
.menuContainer {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
  overflow-y: auto; /* YES */
}

.menuTitles {
  color: aqua;
}
.tableContainer {
  margin-top: 5vh;
  margin-left: 5px;
  padding: 5px;
}

.dataText {
  margin-left: 5px;
}

.rowsDesign {
  color:#000;
}

.dividerDesign {
  margin-left: 5px;
  margin-top: 5px;
}

</style>
