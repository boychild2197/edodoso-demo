<template>
  <div>
    <v-app>
      <div>
        <v-img src="../assets/upperbanner1.png" class="img"></v-img>
      </div>
      <v-main class="main">
        <v-sheet rounded class="mx-auto my-5 sheet ">
          <v-row class="">
            <v-col cols="12" class="d-flex justify-center">
              <div class="d-flex justify-center toprow">
                <!-- <v-text-field
                  clearable
                  flat
                  solo
                  outlined
                  dense
                  class="textfield"
                  prepend-inner-icon="mdi-topic"
                  placeholder="Enter Survey number"
                /> -->
                <v-text-field
                  clearable
                  flat
                  solo
                  outlined
                  dense
                  class="textfield"
                  placeholder="Enter Survey number"
                >
                  <template v-slot:prepend-inner>
                    <img
                      width="24"
                      height="24"
                      src="../assets/topic.svg"
                    /> </template
                ></v-text-field>
                <v-btn class="mx-2 primary white--text btn" medium
                  ><v-icon left>mdi-script</v-icon><span>open</span></v-btn
                >
              </div>
            </v-col>
          </v-row>
          <div>
            <v-divider> </v-divider>
          </div>
          <v-container class="my-3">
            <v-row>
              <v-col cols="12">
                <div>
                  <h2 class="">Public Surveys</h2>
                </div>
                <div>
                  <h3 class="text--disabled">Categories</h3>
                </div>
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="5">
                <v-list flat subheader>
                  <v-list-item-group
                    multiple
                    v-model="settings"
                    active-class=""
                  >
                    <v-list-item
                      v-for="(category, index) in categories"
                      :key="index"
                    >
                      <template v-slot:default="{ active }">
                        <v-list-item-action>
                          <v-checkbox :input-value="active"></v-checkbox>
                        </v-list-item-action>
                        <v-list-item-content>
                          <v-list-item-title>{{
                            category.title
                          }}</v-list-item-title>
                        </v-list-item-content>
                      </template>
                    </v-list-item>
                  </v-list-item-group>
                </v-list>
              </v-col>
              <v-divider vertical class="divider"></v-divider>
              <v-col cols="7" class="">
                <v-virtual-scroll
                  :items="surveys"
                  :item-height="50"
                  height="300"
                >
                  <template v-slot:default="{ item }">
                    <v-list-item link >
                      <v-list-item-avatar color="primary">
                        <v-icon class="white--text">mdi-script</v-icon>
                      </v-list-item-avatar>

                      <v-list-item-content>
                        <v-list-item-title>{{ item.title }}</v-list-item-title>
                      </v-list-item-content>

                      <v-list-item-action  >
                        <!-- <v-btn depressed class="d-none d-lg-block"   >
                          Open survey -->
                          <v-icon color="primary" >
                            mdi-open-in-new
                          </v-icon>
                        <!-- </v-btn> -->
                      </v-list-item-action>
                    </v-list-item>
                  </template>
                </v-virtual-scroll>
              </v-col>
            </v-row>
          </v-container>
        </v-sheet>
      </v-main>
    </v-app>
  </div>
</template>

<script>
import HomeComponent from "@/components/HomeComponent.vue";
export default {
  name: "Home",
  data: () => ({
    categories: [
      {
        title: "All",
      },
      {
        title: "Economics",
      },
      {
        title: "Electricity",
      },
      {
        title: "Technology",
      },
      {
        title: "Social",
      },
    ],
    surveys: [
      {
        title: "Ai in development",
        time: "jan 21",
      },
      {
        title: "Green Computing",
        time: "jan 21",
      },
      {
        title: "Ai in development",
        time: "jan 21",
      },
      {
        title: "Ai in development",
        time: "jan 21",
      },
      {
        title: "Ai in development",
        time: "jan 21",
      },
      {
        title: "Ai in development",
        time: "jan 21",
      },
      {
        title: "Ai in development",
        time: "jan 21",
      },
      {
        title: "Ai in development",
        time: "jan 21",
      },
      {
        title: "Ai in development",
        time: "jan 21",
      },
      {
        title: "Ai in development",
        time: "jan 21",
      },
      {
        title: "Ai in development",
        time: "jan 21",
      },
      {
        title: "Ai in development",
        time: "jan 21",
      },
    ],
  }),

  components: {
    HomeComponent,
  },
};
</script>
<style scoped>
.main {
  margin-top: 4%;
}
div[data-app="true"] {
  background: url("../assets/bg_image1.png") no-repeat center center fixed !important;
  background-size: cover;
}
.img {
  width: auto;
  height: aut;
}
.toprow{
  margin-top: 1%;
}
.card {
  margin-top: 5%;
  height: 20%;
}
.btn_shape_open {
  border-radius: 5px;
  padding: 2px;
  position: absolute;
  margin-top: 3px;
}
.extend_icon {
  padding: 3px;
}
.textfield {
  width: 30vw;
}
.btn {
  margin-top: 2px;
}
.sheet {
  width: 60%;
}
.divider {
}
</style>
