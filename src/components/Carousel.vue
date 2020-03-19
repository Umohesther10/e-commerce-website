<template>
  <div>
    <carousel
      :per-page="1"
      :mouse-drag="true"
      :autoplay="true"
      :loop="true"
      :speed="2000"
      :adjustableHeight="true"
    >
      <slide v-for="slide in images" :key="slide.path">
        <img style="display: block; width: 60%; height: 400px; margin: 0 auto;" :src="slide.path" />
      </slide>
    </carousel>
  </div>
</template>

<script>
export default {
  name: "esther",
  data() {
    return {
      images: [
        {
          path: require("../assets/slide2.jpg")
        },
        {
          path: require("../assets/slider2.jpg")
        },
        {
          path: require("../assets/slider3.jpg")
        },
        {
          path: require("../assets/slider4.jpg")
        },
        {
          path: require("../assets/slider5.jpg")
        },
        {
          path: require("../assets/slider6.jpg")
        },
        {
          path: require("../assets/slider7.jpg")
        }
      ]
    };
  }
};
</script>
