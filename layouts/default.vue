<template>
  <v-container fluid>
    <the-navbar />
    <welcome-screen />
    <section-2 />
    <section-3 />
    <!-- <error /> -->
  </v-container>
</template>

<script>
import Section2 from "./section-2.vue";
import Section3 from "./section-3.vue";
// import error from "./error.vue";
import TheNavbar from "./TheNavbar.vue";
import WelcomeScreen from "./WelcomeScreen.vue";
export default {
  components: {
    //  error
    TheNavbar,
    WelcomeScreen,
    Section2,
    Section3,
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
  // display: flex;
  // align-items: center;
  // background-color: $color-primary;
}
</style>
