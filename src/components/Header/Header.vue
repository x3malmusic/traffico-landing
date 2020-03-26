<template>
  <nav>
    <img src="../../assets/header/logo.png" alt="" class="logo" />
    <ul class="links">
      <div class="links-div">
        <li v-for="link in links">
          <a :href="link.to">{{ link.title }}</a>
        </li>
      </div>
      <Btn title="contact us" />
    </ul>
  </nav>
</template>

<script>
import Btn from "../Button/Btn.vue";

export default {
  name: "Header",
  data: () => ({
    links: [
      { title: "about", to: "#" },
      { title: "how to", to: "#" },
      { title: "faqs", to: "#" },
    ],
  }),
  components: {
    Btn,
  },
};
</script>

<style scoped>
@import "./header.css";
</style>
