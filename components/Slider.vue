<template>
  <div class="slider">
    <div v-for="(slide, index) in slides" :key="index">
      <div class="slide" :style="`background-image: url(${slide.image})`">
        <div class="slide-content">
          <h1>Slider 1</h1>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import "boxicons";
import Vue from "vue";
export default Vue.extend({
  name: "slider",
  data() {
    return {
      slides: [
        {
          image: `${require("~/assets/images/img1.jpg")}`,
        },
      ],
    };
  },
});
</script>

<style scoped>
.slider {
  width: 100vw;
  height: 80vh;
  overflow-x: hidden;
}
.slide {
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  height: 100%;
  width: 100%;
}
/*
prefix width css
sm     640   @media (min-width: 640px)
md     768   @media (min-width: 768px)
lg     1024   @media (min-width: 1024px)
xl     1280   @media (min-width: 1280px)
2xl     1536   @media (min-width: 1536px)
*/
</style>