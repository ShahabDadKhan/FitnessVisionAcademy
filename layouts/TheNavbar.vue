<template>
  <div class="navbar-container">
    <v-container>
      <v-row class="navbar">
        <v-col md="2">
          <div class="links">
            <v-img src="Img/logo.jpg" class="logo-img"></v-img>
          </div>
        </v-col>
        <v-col md="5" class="links-container">
          <ul>
            <a href="#">Home</a>
            <a href="#">About Us</a>
            <a href="#">Service</a>
            <!-- <a href="#">Courses</a> -->
            <a href="#">Blog</a>
            <a href="#"
              >Let's <br />
              Talk</a
            >
          </ul>
          <!-- <v-col md="2"> Let's Talk </v-col> -->
          <!-- <div class="talk-badge">Let's Talk</div> -->
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.navbar-container {
  background-color: $color-primary;
  height: 15vh;
}

.container {
}

.navbar {
  height: 100%;
  // background-color: orangered;
  display: flex;
  // flex-direction: row;
  align-items: center;
  justify-content: space-between;

  .logo-img {
    cursor: pointer;
    // max-height: "100%";
    max-width: 80%;
    border-radius: 50%;
  }

  .links {
    width: 70px;
  }

  & .links-container {
    // display: flex;
    ul {
      display: flex;
      // flex-direction: row;
      justify-content: space-between;

      a {
        display: flex;
        align-items: center;
        // color: $color-light;
        cursor: pointer;
        font-weight: 600;
        list-style: none;
        text-decoration: none;

        &:last-child {
          display: flex;
          align-items: center;
          justify-content: center;
          color: $color-white;
          background-color: $color-secondary;
          width: 60px;
          height: 80px;
          text-align: center;
          border-radius: 0px 0px 15px 15px;
        }

        &:not(:last-child) {
          &:hover,
          &:focus {
            font-size: 20px;
            font-weight: 700;
            color: $color-secondary;
            // text-decoration: underline;
            transition: 0.3s;
            // border-bottom: 1px solid $color-secondary;
          }
        }
      }
    }
  }
}
</style>
