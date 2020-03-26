<template>
  <button class="btn">
    {{ title }}
    <span v-if="arrow" class="arrow">&#10132;</span>
  </button>
</template>

<script>
export default {
  props: {
    title: String,
    arrow: Boolean,
  },
  name: "Btn",
};
</script>

<style scoped>
@import "./btn.css";
</style>
