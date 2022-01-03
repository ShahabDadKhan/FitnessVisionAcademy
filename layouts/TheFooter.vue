<template>
  <div class="footer">
    <v-container>
      <v-row>
        <v-col md="4">
          <div class="fva">Fitness Vission</div>
          <ul class="social-media">
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
              Inside Universal Plaza Hotel, Ist Floor On Diamond Road,
              Rampur(U.P)
            </li>
            <li>
              <h3>Phone</h3>
              +91 8920985643
            </li>
            <li>
              <h3>Email</h3>
              fitnessvisionacademy@gmail.com
            </li>
          </ul>
        </v-col>
      </v-row>
    </v-container>
    <div class="copyright">
      COPYRIGHT©Fitness Vision Academy. All rights reserved
    </div>
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
  display: flex;
  align-items: center;
  border-bottom: 1px solid $color-secondary;

  .row {
    height: 80%;
    :first-child {
      ul {
        flex-direction: row !important;
      }
    }
    .col {
      display: flex;
      flex-direction: column;
      justify-content: flex-start;

      ul {
        display: flex;
        flex-direction: column;
        list-style: none;

        li {
          margin-bottom: 5%;
          cursor: pointer;

          .v-icon {
            color: $color-secondary;
            cursor: pointer;
            transition: transform 0.2s;

            &:hover {
              transform: scale(1.2);
            }
          }
        }
      }
    }
  }
  .copyright {
    font-size: 20px;
    font-weight: 600;
    text-align: center;
    padding: 2% 0%;
  }

  .social-media {
    width: 50%;
    justify-content: space-between;
  }
}
</style>
