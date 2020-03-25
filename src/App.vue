<template>
  <div>
    <!--    your awesome traffic-->
    <section class="awesome-traffic-section">
      <Header />
      <div class="section awesome-traffic-section-content">
        <h1>Your awesome traffic permit consultant.</h1>
        <Btn title="get started" :arrow="true" />
      </div>
      <img src="./assets/Home/mobel.png" alt="" class="traffic-car" />
    </section>
    <!--    your awesome traffic end-->

    <!--   sections -->
    <section class="sections-section section">
      <section-component
        v-for="section in sections"
        :title="section.title"
        :text="section.text"
        :warning="section.warning"
        :img="section.img"
      />
    </section>
    <!--   sections end-->
  </div>
</template>

<script>
import Header from "./components/Header/Header.vue";
import Btn from "./components/Button/Btn.vue";
import SectionComponent from "./components/SectionComponent/SectionComponent.vue";

import "./main.css";

export default {
  name: "App",
  components: {
    Header,
    Btn,
    SectionComponent,
  },
  data: () => ({
    sections: [
      {
        title: "about us",
        text:
          "The occupational traffic permit is one of the most important things in the company when carrying out freight transport. In fact, it is a prerequisite for doing business traffic at all.",
        warning:
          "How do you do when you need to obtain a commercial traffic permit for freight transport to your business?",
        img: "../../assets/Home/man.png",
      },
    ],
  }),
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
</style>
