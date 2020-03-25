<template>
  <div class="section-wrapper">
    <div class="section-content">
      <h3 class="title">{{ title }}</h3>
      <p class="text">{{ text }}</p>
      <div class="warning-wrapper">
        <div class="warning-bg"></div>
        <h3 class="warning">{{ warning }}</h3>
      </div>
    </div>
    <div class="img-wrapper">
      <img src="../../assets/Home/man.png" alt="" />
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
  },
  computed: {
    getImg() {
      return require(this.img);
    },
  },
  name: "SectionComponent",
};
</script>

<style scoped>
@import "sectioncomponent.css";
</style>
