<template>
  <div class="navbar-container">
    <v-container>
      <v-row>
        <v-col md="5">
          <div class="welcome-text">
            Fox Valley Physical Therapy & Wellness Clinic
          </div>
          <div class="welcome-subheading">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo veniam,
            inventore reiciendis amet consectetur adipisicing.
          </div>
          <div>
            <v-btn class="btn" elevation="1" large>Get In Touch</v-btn>
          </div>
        </v-col>
        <v-col md="5">
          <no-ssr>
            <v-img src="Img/welcome-1.jpg" class="welcome"></v-img>
          </no-ssr>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.container {
  height: 100%;
  background-color: $color-primary;
}

.navbar-container {
  background-color: $color-primary;
  height: 89vh;

  .row {
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  & .welcome-text {
    font-size: 60px;
    font-weight: 900;
    color: $color-secondary;
  }

  & .welcome-subheading {
    line-height: 1.5;
    font-size: 15px;
    font-weight: 500;
    margin: 5% 0%;
    color: $color-secondary;
  }

  & .btn {
    color: white;
    background-color: $color-secondary;
  }

  .welcome {
    max-width: 90%;
    border-radius: 50%;
    background: transparent;
    // background-color: red;
    background-blend-mode: multiply;
  }
}
</style>
