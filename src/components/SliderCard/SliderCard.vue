<template>
  <div class="slider-card">
    <p class="slider-text">{{ text }}</p>
      <div class="slider-avatar">
        <img :src="getImage" alt="" />
        <p class="slider-name">{{ name }}</p>
      </div>
  </div>
</template>

<script>
export default {
  name: "SliderCard",
  props: {
    text: String,
    avatar: String,
    name: String,
  },
  computed: {
    getImage() {
      return require(`../../assets/Home/${this.avatar}`);
    },
  },
};
</script>

<style scoped>
@import "./slidercard.css";
</style>
