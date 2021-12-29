<template>
  <div class="section-2">
    <v-container>
      <v-row class="top">
        <v-col md="6" class="Checking-engine">
          We provide the best <span> Checking Engine </span> for our patient
        </v-col>
        <v-col md="6">
          <div class="">
            <VueSlickCarousel v-bind="settings" ref="carousel" class="carousel">
              <div v-for="(icon, index) in icons" :key="index">
                <v-icon>{{ icon.name }}</v-icon>
                <span> {{ icon.detail }} </span>
              </div>
            </VueSlickCarousel>
          </div>
        </v-col>
      </v-row>
      <v-row class="down">
        <div>
          <h2>About Us</h2>
          <p>
            In 2018 the Fitness Vision Academy was established and teaching many
            disciples about the method of training and the art of changing
            lifestyles. Fitness Vision academy is India most prestigious fitness
            learning training center for fitness learners. Purpose is dedicated
            to making a career in the fitness industry. We offer different
            courses, different programs because we want everyone to be able to
            make their dream their career. We provide services from American,
            European bodies such as FOUNDATION COURSE FOR BEGINNERS, ACE, ACSM,
            NASM, CSCS and we are a recognized institution which allows us to
            not only award certifications but also offer diplomas in the field
            of fitness.
          </p>
        </div>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
// optional style for arrows & dots
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";
export default {
  name: "MyComponent",
  components: { VueSlickCarousel },
  data: () => ({
    settings: {
      dots: false,
      arrows: true,
      dotsClass: "slick-dots custom-dot-class",
      edgeFriction: 0.35,
      infinite: true,
      autoplay: false,
      autoplaySpeed: 5000,
      speed: 500,
      slidesToShow: 4,
      slidesToScroll: 1,
    },
    icons: [
      { name: "mdi-heart-pulse", detail: "Heart Rate" },
      { name: "mdi-weight-lifter", detail: "Balance" },
      { name: "fas fa-lungs", detail: "Respiratory" },
      { name: "fas fa-wheelchair", detail: "Recovery" },
      { name: "fas fa-book-open", detail: "Information" },
      { name: "fas fa-dumbbell", detail: "Exercise" },
      { name: "fas fa-user-md", detail: "Treatment" },
    ],
  }),
};
</script>

<style lang="scss" scoped>
.section-2 {
  .container {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    height: 100vh;

    .top {
      width: 80%;
      height: 0%;
      background: white;
      margin-top: -4%;
      z-index: 1;
      border-radius: 8px;
      box-shadow: 0px 5px 10px black;
      display: flex;
      align-items: center;
      flex-direction: column;

      .col {
        min-width: 90% !important;
        display: flex;
        justify-content: center;

        &:first-child {
          align-items: center;
          max-height: 40%;
          font-size: 30px;
          font-weight: 700;
          color: $color-secondary;

          span {
            color: $color-primary;
            margin: 0px 10px;
          }
        }

        &:last-child {
          flex-direction: column;
        }
      }

      .carousel {
        display: flex;
        align-items: center;
        justify-content: center;

        div {
          display: flex !important;
          flex-direction: column;
          text-align: center;
          cursor: pointer;
        }
      }

      ::v-deep .slick-slide {
        display: flex;
        justify-content: center;
      }

      ::v-deep .slick-slider {
        border-top: 1px solid rgba(0, 0, 0, 0.54);
        padding-top: 26px;
      }

      ::v-deep .slick-arrow {
        // background: red;
        position: relative;
        top: -40px;
        &::before {
          color: black;
          //   background: black;
        }
      }

      .cars {
        height: 225px !important;
      }

      //   ::v-deep .v-pagination__navigation {
      //     // color: red;
      //     // background: pink;
      //     // border-radius: 50%;
      //   }
    }

    .down {
      text-align: center;
      display: flex;
      justify-content: center;
      align-items: center;
      // height: 70vh;

      div {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
      }

      h2 {
        font-size: 32px;
        color: $color-secondary;
        margin-bottom: 3%;
        font-weight: 900;
      }
      p {
        width: 90%;
        line-height: 1.5;
        font-size: 22px;
      }
    }
  }
}
</style>
