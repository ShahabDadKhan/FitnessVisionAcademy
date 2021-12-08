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
          <v-img src="/assets/Img/welcome-1.jpg"></v-img>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.contanier {
  background-color: $color-primary;
}

.navbar-container {
  background-color: $color-primary;
  height: 89vh;

  .row {
    display: flex;
    align-items: center;
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
}
</style>
