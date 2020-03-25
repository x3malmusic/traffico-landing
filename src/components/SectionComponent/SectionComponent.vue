<template>
  <div class="section-wrapper">
    <div class="section-content">
      <h3>{{ title }}</h3>
      <p>{{ text }}</p>
      <div>
        <h3>{{ warning }}</h3>
      </div>
    </div>
    <img :src="getImg" alt="" />
  </div>
</template>

<script>
import "./sectioncomponent.css";

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
