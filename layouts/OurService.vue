<template>
  <v-container>
    <v-card flat>
      <v-tabs
        v-model="tab"
        background-color="deep-purple accent-4"
        centered
        dark
        icons-and-text
      >
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
          <div class="course-1"></div>
          <div class="course-2"></div>
          <div class="course-3"></div>
          <div class="course-4"></div>
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
    };
  },
};
</script>

<style lang="scss" scoped>
.v-tabs {
  display: flex;
  justify-content: center;
  color: red !important;
}

.v-tab {
  width: 180px;
}

.v-window-item {
  display: flex;
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
</style>
