<template>
  <v-container class="layoutD">
    <div>
      <v-card class="navigationCard">
        <v-layout>
          <v-navigation-drawer
            floating
            permanent
            style="width: 15vw; background-color: rgb(25, 23, 23)"
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
                thickness="2"
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
                      <td class="dataText">VueJS</td>
                      <td class="dataText">
                        <v-progress-linear
                          color="white"
                          model-value="80"
                        ></v-progress-linear>
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
                thickness="2"
              ></v-divider>

              <div class="actionButtons">
                <v-col cols="12" sm="6" md="4" lg="12">
                  <v-btn rounded="xs" size="large">Contact Me</v-btn>
                </v-col>
              </div>
            </div>
          </v-navigation-drawer>
        </v-layout>
      </v-card>
    </div>
    <!-- <div
      style="
        display: flex;
        flex-direction: column;
        justify-content: center;
        background-color: brown;
        width: 100vw;
      "
    > -->
    <Shortbrief />
    <!-- </div> -->
  </v-container>
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
.layoutD {
  width: 100%;
}
.menuContainer {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100vh;

  overflow: hidden;
}
.menuTitles {
  color: aqua;
}
.tableContainer {
  margin-top: 5vh;
  margin-left: 5px;
  padding: 5px;
}
.tableDesign {
  background-color: transparent;
}
.tableDesign {
  width: 80%;
  margin-left: 20px;
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

@media (max-width: 768px) {
  .navigationCard {
    display: none;
  }
}
</style>
