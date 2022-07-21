<template>
  <div>
    <v-app-bar color="#3073D8" dark>
      <v-toolbar-title
        ><h1 class="subheading white--text">eDodoso</h1></v-toolbar-title
      >
      <v-spacer></v-spacer>
      <div>
        <h4>mshamugervas@gmail.com<v-icon right>mdi-account-circle</v-icon></h4>
      </div>
    </v-app-bar>
    <v-main>
      <v-container class="contain">
        <v-layout row justify-center wrap class="mx-5">
          <v-flex class="d-flex justify-center">
            <h1>Institutional Account</h1>
          </v-flex>
        </v-layout>
        <v-layout row justify-center wrap class="mx-5 my-5">
          <v-flex class="d-flex justify-center align-center">
            <v-avatar size="10" color="green" class="mx-1"></v-avatar>
            <h4 class="cation">Royal Tour subscription</h4>
            <h5 class="caption green--text">(active)</h5>
          </v-flex>
        </v-layout>

        <v-layout row justify-center wrap class=" mx-5">
          <v-flex class="d-flex justify-center align-center flex1" >
            <v-layout row justify-center wrap>
              <v-flex
                xs12
                md3
                class="ma-5"
                v-for="(card, index) in cards"
                :key="index"
              >
                <v-hover v-slot="{ hover }">
                  <v-card
                    height="150"
                    :class="{ 'on-hover': hover }"
                    flat
                    :color="hover ? '#90CAF9' : '#E3F2FD'"
                    link
                  >
                    <v-card-text>
                      <v-container class="continerIcon">
                        <v-layout row justify-center>
                          <v-flex class="d-flex justify-center">
                            <v-icon size="70" color="black">{{
                              card.icon
                            }}</v-icon>
                          </v-flex>
                        </v-layout>
                        <v-layout row justify-center>
                          <v-flex class="d-flex justify-center">
                            <v-card-title>{{ card.title }}</v-card-title>
                          </v-flex>
                        </v-layout>
                      </v-container>
                    </v-card-text>
                  </v-card>
                </v-hover>
              </v-flex>
            </v-layout>
          </v-flex>
        </v-layout>
      </v-container>
    </v-main>
  </div>
</template>

<script>
export default {
  name: "InstitutionalView",
  data: () => ({
    cards: [
      {
        icon: "mdi-shopping",
        title: "Surveys",
      },
      {
        icon: "mdi-cards",
        title: "Payments",
      },
      {
        icon: "mdi-shopping",
        title: "Subscription",
      },
      {
        icon: "mdi-cards",
        title: "Settings",
      },
      {
        icon: "mdi-cards",
        title: "System Management",
      },
      {
        icon: "mdi-cards",
        title: "System Management",
      },
    ],
  }),
};
</script>

<style>
.contain {
  margin-top: 3%;
}
.flex1 {
  margin-top: 3%;
}
.continerIcon {
  margin-top: 2%;
}
</style>