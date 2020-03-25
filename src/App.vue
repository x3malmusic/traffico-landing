<template>
  <div>
    <!--    your awesome traffic-->
    <section class="awesome-traffic-section">
      <Header />
      <div class="awesome-traffic-section-content">
        <h1>Your awesome traffic permit consultant.</h1>
        <Btn title="get started" :arrow="true" />
      </div>
      <img src="./assets/Home/mobel.png" alt="" class="traffic-car"/>
    </section>
    <!--    your awesome traffic end-->
  </div>
</template>

<script>
import Header from "./components/Header/Header.vue";
import Btn from "./components/Button/Btn.vue";

import "./main.css";

export default {
  name: "App",
  components: {
    Header,
    Btn,
  },
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
</style>
