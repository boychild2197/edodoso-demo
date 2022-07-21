<template>
  <div>
    <v-app>
      <v-main class="main">
        <v-container class="container">
          <v-row>
            <v-col class="d-flex justify-center">
              <v-card :loading="loading" class="mx-auto my-12" max-width="374">
                <template slot="progress">
                  <v-progress-linear
                    color="deep-purple"
                    height="10"
                    indeterminate
                  ></v-progress-linear>
                </template>

                <!-- <v-img
                  height="250"
                  src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
                ></v-img> -->
                <v-row class="avatarow">
                  <v-col class="d-flex justify-center">
                    <v-avatar color="blue" size="150">
                      <v-img
                        src="../assets/coat2.jpg"
                        width="150"
                        height="150"
                      />
                    </v-avatar>
                  </v-col>
                </v-row>
                <v-row>
                  <v-col class="d-flex justify-center">
                    <h2>Login</h2>
                  </v-col>
                </v-row>

                <v-card-text>
                  <v-row align="center" class="mx-0">
                    <v-col>
                      <v-form>
                        <v-text-field
                          label="Email"
                          placeholder="eg. xxx@xxx.com"
                          outlined
                          dense
                          prepend-inner-icon="mdi-email"
                        ></v-text-field>
                        <v-text-field
                          label="Password"
                          placeholder="eg. ******"
                          outlined
                          dense
                          prepend-inner-icon="mdi-lock"
                        ></v-text-field>
                        <v-btn
                          color="primary"
                          class="white--text btn-login"
                          block
                        >
                          <v-icon left size="20">mdi-login</v-icon>Login
                        </v-btn>
                      </v-form>
                    </v-col>
                  </v-row>
                </v-card-text>

                <v-divider></v-divider>
                <v-card-text>
                  <div class="text-center">
                    <v-btn class="mx- btn" color="primary" small text link>
                      <a href="">Back Home</a>
                    </v-btn>
                    <v-btn class="mx-4 btn" color="primary" small text link>
                      <a href="">Forgot password?</a>
                    </v-btn>
                  </div>
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </v-main>
    </v-app>
  </div>
</template>

<script>
export default {
  name: "LoginView",
  data: () => ({}),
};
</script>
<style scoped>
.container {
  margin-top: 5%;
}
.avatarow {
  margin-top: 3%;
}
.btn {
  text-transform: unset;
}
</style>
