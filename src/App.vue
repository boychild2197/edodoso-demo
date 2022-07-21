<template>
  <v-app>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
<style scoped>
/* main{
  background-image: url('./assets/bg_image1.png');
  backgorund-size:cover;
} */
</style>
