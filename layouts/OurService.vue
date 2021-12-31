<template>
  <v-container>
    <v-card flat>
      <v-tabs v-model="tab" background-color="" centered dark icons-and-text>
        <!-- <v-tabs-slider></v-tabs-slider> -->

        <v-tab class="tab-1" href="#tab-1">
          Education
          <v-icon>fas fa-book-open</v-icon>
        </v-tab>

        <v-tab class="tab-2" href="#tab-2">
          Gym
          <v-icon>mdi-weight-lifter</v-icon>
        </v-tab>
      </v-tabs>

      <v-tabs-items v-model="tab">
        <v-tab-item :value="'tab-' + 1">
          <div v-for="(info, i) in academyInfo" :key="i" class="academyInfo">
            <h4>{{ info.heading }}</h4>
            <p>{{ info.para }}</p>
          </div>
          <v-btn class="btn" elevation="1">
            <NuxtLink to="/components/our-courses">Find Courses</NuxtLink>
          </v-btn>
        </v-tab-item>

        <v-tab-item :value="'tab-' + 2">
          <v-card flat>
            <v-card-text>Hi from 2</v-card-text>
          </v-card>
        </v-tab-item>
      </v-tabs-items>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      tab: null,
      text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
      academyInfo: [
        {
          heading: "Foundation Course:",
          para: " This course is for those who are stepping into the fitness field for the first time. Course will cover the anatomy of the human body along with a general idea.",
        },
        {
          heading: "ACE Course:",
          para: "This course provides science based health and fitness information and inspire people with quality education about fitness. Along with preparing them for the coveted certification from American Council on Exercise, thus enhancing employability and professional growth.",
        },
        {
          heading: "Mission:",
          para: "The Fitness Vision Academy is designed to promote fitness as an education. The objective guides fitness professionals and enthusiasts in their career graph. With the advent of technology and irregular eating habits, obesity and fatal diseases are at a high time. Our objective here as a whole is to create a safe and educated environment for generations to come, we focus primarily on enabling a healthy mindset that leads to a healthy and fit body.",
        },
        {
          heading: "Vision:",
          para: "With the aim of spreading fitness vision academy awareness, creating acceptance in the world for adopting fitness as a career. Maintain international standards for trainers in India. Keep up with the new changing fitness trends. Promote safe and effective training for all. Promote an active and healthy lifestyle for all individuals in society",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.v-tabs {
  display: flex;
  justify-content: center;
  color: rgba(0, 0, 0, 0.54) !important;
  margin: 5% 0%;
}

.v-tab {
  width: 180px;
  background-color: $color-light-grey;
  color: rgba(0, 0, 0, 0.54) !important;

  .v-icon {
    color: rgba(0, 0, 0, 0.54) !important;
  }
}

.v-window-item {
  display: flex;
  flex-direction: column;
  background-color: white;
  justify-content: space-between;
}

.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.5;
  position: absolute;
  width: 100%;
}

.academyInfo {
  margin-bottom: 3%;
  // display: flex;
  // flex-direction: column;

  h4 {
    color: $color-secondary;
  }
  p {
    // color: ;
  }
}

.v-btn {
  width: 150px;
  height: 50px;
  color: white;
  // margin-bottom: 1%;
  background-color: $color-secondary !important;
}
</style>
