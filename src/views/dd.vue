<!-- <template>
  <div>
    <v-app-bar color="#3073D8" dark>
      <v-toolbar-title><h1>eDodoso</h1></v-toolbar-title>
      <v-spacer></v-spacer>
      <div>
        <h4>mshamugervas@gmail.com<v-icon right>mdi-account-circle</v-icon></h4>
      </div>
    </v-app-bar>
    <v-main>
      <v-container class="contain">
        <v-row justify="center">
          <v-col class="d-flex align-center justify-center">
            <h1>Institutional Account</h1>
          </v-col>
        </v-row>
        <v-row>
          <v-col class="d-flex justify-center">
            <h3>Royal Tour subscription</h3>
          </v-col>
        </v-row>
        <v-row>
          <v-col class="justify-center" cols="12">
            <v-container>
              <v-layout row align-center wrap>
                <v-flex lg4> </v-flex>
              </v-layout>
              <v-row justify="center">
                <v-col cols="3" class=" justify-center mx-2">
                  <v-card width="300" height="100">

                  </v-card>
                </v-col>
                              <v-col cols="3" class=" justify-center mx-2">
                  <v-card width="300" height="100">

                  </v-card>
                </v-col> -->
                <!-- <v-col
                  cols="12"
                  v-for="i in 2"
                  :key="i"
                  class="d-flex justify-center"
                >
                  <v-card :key="i" class="" width="200" height="100">
                    ffff
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
    <v-container class="grey lighten-5">
      <v-row v-for="j in justify" :key="j" :justify="j">
        <v-col v-for="k in 2" :key="k" md="4">
          <v-card class="pa-2" outlined tile> One of two columns </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
 
<template>
  <div class="dashboard">
    <h1 class="subheading grey--text">Dashboard</h1>
    <v-container class="my-5">
      <v-layout row wrap>
        <v-flex xs12 md6>
          <v-btn outline block class="primary">1</v-btn>
        </v-flex>
        <v-flex xs12 md6>
          <v-btn outline block class="primary">1</v-btn>
        </v-flex>
      </v-layout>

      <!-- <v-layout row justify-center wrap>
        <v-flex xs12 md3 class="ma-5" v-for="i in 5" :key="i">
          <v-card height="100"></v-card>
        </v-flex> -->
      <!-- <v-flex xs12 md3 class="mx-5">
          <v-btn outline block class="primary">1</v-btn></v-flex
        > -->

      <div>
        <v-layout row justify-center wrap class="lay1 mx-5 ">
          <v-flex>
            <v-layout row justify-center wrap>
              <v-flex xs12 md3 class="ma-5" v-for="i in 8" :key="i">
                <v-card height="150" class="cad">

                </v-card>
              </v-flex>
            </v-layout>
          </v-flex>
        </v-layout>
      </div>
    </v-container>
  </div>
</template>
<script>
export default {
  name: "InstitutionalView",
  data: () => ({}),
};
</script>

<style scoped>
.contain {
  margin-top: 3%;
}
.lay1 {
     margin-top: 3%;
}
.cad{

}
</style>