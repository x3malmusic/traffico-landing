<template>
  <button class="btn">
    {{ title }}
    <span v-if="arrow" class="arrow">&#10132;</span>
  </button>
</template>

<script>
import "./btn.css";

export default {
  props: {
    title: String,
    arrow: Boolean,
  },
  name: "Btn",
};
</script>
