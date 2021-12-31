<template>
  <div class="footer">
    <v-container>
      <v-row>
        <v-col md="4">
          <div class="fva">Fitness Vission</div>
          <ul>
            <li>
              <v-icon>fab fa-instagram</v-icon>
            </li>
            <li>
              <v-icon>fab fa-twitter</v-icon>
            </li>
            <li>
              <v-icon>fab fa-facebook</v-icon>
            </li>
            <li>
              <v-icon>fab fa-pinterest</v-icon>
            </li>
          </ul>
        </v-col>
        <v-col md="4">
          <ul>
            <li>
              <h3>Home</h3>
            </li>
            <li>
              <h3>About Us</h3>
            </li>
            <li>
              <h3>Blog</h3>
            </li>
            <li>
              <h3>Testimonial</h3>
            </li>
          </ul>
        </v-col>
        <v-col md="4">
          <ul>
            <li>
              <h3>Location</h3>
            </li>
            <li>
              <h3>Phone</h3>
            </li>
            <li>
              <h3>Email</h3>
            </li>
          </ul>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.footer {
  margin-top: 3%;
  background-color: $color-primary;
  color: $color-secondary;
}

.fva {
  font-size: 32px;
  font-weight: 800;

  margin-bottom: 10%;
}

.container {
  height: 50vh;

  .row {
    height: 100%;
    :first-child {
      ul {
        flex-direction: row !important;
      }
    }
    .col {
      display: flex;
      flex-direction: column;
      justify-content: center;

      ul {
        display: flex;
        flex-direction: column;
        list-style: none;

        li {
          margin-bottom: 5%;
        }
      }
    }
  }
}
</style>
