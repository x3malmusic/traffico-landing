<template>
  <div class="accordion accordion-btn" @click="active = !active">
    <div class="accordion-btn-bg"></div>
    <div class="content">{{ title }}</div>
    <span class="char char-btn">+</span>
  </div>
</template>

<script>
export default {
  name: "AccordionBtn",
  props: {
    title: String,
  },
};
</script>

<style scoped>
@import "./accordion.css";
</style>
