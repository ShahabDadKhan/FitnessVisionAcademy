<template>
  <div class="section-3">
    <v-container>
      <v-row class="row-1">
        <v-col class="box-1" md="3">
          <div class="blue"></div>
          <div class="grey"></div>
        </v-col>
        <v-col md="6">
          <h2>
            The Values We <br />
            Live By
          </h2>
        </v-col>
        <v-col class="box-2" md="3">
          <div class="grey"></div>
          <div class="blue"></div>
        </v-col>
      </v-row>
      <v-row class="row-2">
        <v-col
          class="value-box"
          v-for="(value, i) in values"
          :key="i"
          sm="12"
          md="3"
        >
          <img
            :src="require(`../static/Img/${value.img}.jpg`)"
            alt="Work-Hard"
          />
          <h3>{{ value.heading }}</h3>
          <h6>{{ value.subheading }}</h6>
          <p>{{ value.para }}</p>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      values: [
        {
          heading: "Daily Hard Work",
          subheading: "We Work Hard Everyday",
          para: "We keep our promises, provide upfront timelines & bring predictablity.",
          img: "work-hard",
          //   icon: "",
        },
        {
          heading: "Passion Before Money",
          subheading: "Money is not the factor",
          para: "We keep our promises, provide upfront timelines & bring predictablity.",
          img: "passion",
          //   icon: "",
        },
        {
          heading: "Teamwork  drives results",
          subheading: "Together,We Create!",
          para: "We keep our promises, provide upfront timelines & bring predictablity.",
          img: "team-work",
          //   icon: "",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.section-3 {
  //   background-color: $color-light-grey;
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.container {
  height: 100%;

  .row-1 {
    justify-content: space-between;
    align-items: center;
    height: 30%;
    margin-bottom: 5%;
  }

  .row-2 {
    height: 50%;

    .col {
      background-color: $color-light-grey;
    }
  }
  .row {
    display: flex;
    justify-content: space-around;

    .col {
      display: flex;
      justify-content: center;

      img {
        transition: transform 0.2s;
        margin-bottom: 10px;

        &:hover {
          transform: scale(1.05);
          -webkit-filter: blur(4px); /* Chrome, Safari, Opera */
          filter: blur(1px);
        }
      }

      h3 {
        color: $color-secondary;
        margin-bottom: 2%;
      }

      h6 {
        color: $color-secondary;
        margin-bottom: 3%;
      }
    }
  }

  h2 {
    font-size: 36px;
    color: $color-secondary;
    text-align: center;
  }
}

.value-box {
  display: flex;
  flex-direction: column;
}

.box-1 {
  justify-content: right !important;
}

.box-2 {
  justify-content: left !important;
}

.blue {
  width: 50px;
  height: 50px;
  background-color: $color-secondary;
}

.grey {
  width: 50px;
  height: 50px;
  background-color: $color-light-grey;
}
</style>
