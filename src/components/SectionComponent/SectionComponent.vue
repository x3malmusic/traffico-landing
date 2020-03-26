<template>
  <div class="section-wrapper">
    <div class="section-content">
      <div :class="left ? 'wrapper' : ''">
        <h3 class="title">{{ title }}</h3>
        <p class="text">{{ text }}</p>
      </div>
      <div class="warning-wrapper" v-if="warning">
        <div class="warning-bg"></div>
        <h3 class="warning">{{ warning }}</h3>
      </div>
    </div>
    <div :class="left ? 'img-wrapper left' : 'img-wrapper'">
      <div class="img" :style="`background-image: url(${getImg})`"></div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    text: String,
    warning: String,
    img: String,
    left: Boolean,
  },
  computed: {
    getImg() {
      return require(`../../assets/Home/${this.img}`);
    },
  },
  name: "SectionComponent",
};
</script>

<style scoped>
@import "sectioncomponent.css";
</style>
