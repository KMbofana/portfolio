<template>
  <v-row no-gutters>
    <v-col cols="2">
      <v-card>
        <v-layout>
          <v-navigation-drawer
            floating
            permanent
            style="width: 15vw; background-color: black"
          >
            <div class="menuContainer">
              <v-table density="compact" theme="dark" class="tableContainer">
                <tbody>
                  <tr style="color: aqua" class="tableDesign">
                    <th>Country:</th>
                    <th>Zimbabwe</th>
                  </tr>
                  <tr style="color: aqua" class="tableDesign">
                    <th>City:</th>
                    <th>Harare</th>
                  </tr>
                  <tr style="color: aqua" class="tableDesign">
                    <th>Age:</th>
                    <th>27</th>
                  </tr>
                </tbody>
              </v-table>
              <v-divider
                color="white"
                class="dividerDesign"
                thickness="4"
                length="200"
              ></v-divider>
              <div class="skillList">
                <div class="skillListContainer">
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
                        <v-progress-linear
                          color="white"
                          model-value="60"
                        ></v-progress-linear>
                      </td>
                    </tr>
                    <tr class="rowsDesign">
                      <td class="dataText">MongoDB</td>
                      <td class="dataText">
                        <v-progress-linear
                          color="white"
                          model-value="60"
                        ></v-progress-linear>
                        <v-progress-circular> </v-progress-circular>
                      </td>
                    </tr>
                    <tr class="rowsDesign">
                      <td class="dataText">.Net</td>
                      <td class="dataText">
                        <v-progress-linear
                          color="white"
                          model-value="40"
                        ></v-progress-linear>
                      </td>
                    </tr>
                  </table>
                </div>
              </div>

              <v-divider
                color="white"
                class="dividerDesign"
                thickness="4"
                length="200"
              ></v-divider>

              <div class="actionButtons">
                <v-col cols="12" sm="6" md="4" lg="12">
                  <v-btn rounded="xs" size="large">Hire Me</v-btn>
                </v-col>
                <v-col cols="12" sm="6" md="4" lg="12">
                  <v-btn rounded="xs" size="large">Contact Me</v-btn>
                </v-col>
              </div>
            </div>
          </v-navigation-drawer>
        </v-layout>
      </v-card>
    </v-col>
    <v-col>
      <div style="background-color: black">
        <Shortbrief />
      </div>
    </v-col>
  </v-row>
</template>
<script>
import Shortbrief from "./shortbrief.vue";

export default {
  name: "PortifolioProfile",

  data() {
    return {};
  },

  mounted() {},

  components: {
    Shortbrief,
  },

  methods: {},
};
</script>

<style scoped>
.menuContainer {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100vh;
  /* border-right: 2px;
  border-right-color: aqua;
  border-right-style: solid; */

  overflow: hidden;
  /* box-shadow: 5px 10px 10px 12px red; */
}
.menuTitles {
  color: aqua;
}
.tableContainer {
  margin: 5px;
  padding: 5px;
}
.tableDesign {
  background-color: black;
}
.tableDesign {
  width: 80%;
  margin-left: 24px;
  margin-top: 10px;
}
.dataText {
  margin-left: 5px;
}

.rowsDesign {
  color: aqua;
  margin-top: 5px;
}
.actionButtons {
  /* display: flex;
  flex-direction: column;
  justify-content: center;
  margin-top: 15%; */
}
.dividerDesign {
  margin-left: 5px;
  margin-top: 5px;
}
</style>
