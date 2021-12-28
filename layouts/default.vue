<template>
  <v-container fluid>
    <div class="bg">
      <the-navbar />
      <welcome-screen />
    </div>
    <section-2 />
    <!-- <error /> -->
  </v-container>
</template>

<script>
import Section2 from "./section-2.vue";
// import error from "./error.vue";
import TheNavbar from "./TheNavbar.vue";
import WelcomeScreen from "./WelcomeScreen.vue";
export default {
  components: {
    //  error
    TheNavbar,
    WelcomeScreen,
    Section2,
  },
};
</script>

<style lang="scss">
html {
  font-family: "Assistant", Volkhov;
  font-size: 18px;
  font-weight: 400;
}

.bg {
  background: url("../static/Img/welcome.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}

.container {
  padding: 0px;
  // display: flex;
  // align-items: center;
  // background-color: $color-primary;
}
</style>
