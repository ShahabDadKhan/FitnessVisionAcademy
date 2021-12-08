<template>
  <v-container fluid>
    <the-navbar />
    <welcome-screen />
    <!-- <error /> -->
  </v-container>
</template>

<script>
// import error from "./error.vue";
import TheNavbar from "./TheNavbar.vue";
import WelcomeScreen from "./WelcomeScreen.vue";
export default {
  components: {
    //  error
    TheNavbar,
    WelcomeScreen,
  },
};
</script>

<style lang="scss">
html {
  font-family: "Assistant", Volkhov;
  font-size: 18px;
  font-weight: 400;
}

.container {
  padding: 0px;
  // background-color: $color-primary;
}
</style>
