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
        :left="section.left || false"
        :key="section.title"
      />
    </section>
    <!--   sections end-->

    <!--   FAQ -->
    <section class="faq">
      <div class="faq-content">
        <div class="faq-section">
          <div class="faq-section-text">
            <h3 class="faq-title">faq</h3>
            <h2 class="faq-text">
              Questions and Answers on Professional Traffic Permits:
            </h2>
          </div>
          <div class="faq-section-img-wrapper">
            <img src="./assets/Home/faq.png" alt="" />
          </div>
        </div>
        <div class="faq-section-content">
          <div class="accordion-row" v-for="e in accordions">
            <Accordion :title="e.title" :text="e.text" :key="e.title" />
          </div>
          <div class="accordion-row"></div>
          <div class="accordion-row">
            <AccordionBtn title="load more" />
          </div>
        </div>
      </div>
    </section>
    <!--   FAQ end-->
  </div>
</template>

<script>
import Header from "./components/Header/Header.vue";
import Btn from "./components/Button/Btn.vue";
import SectionComponent from "./components/SectionComponent/SectionComponent.vue";
import Accordion from "./components/Accordion/Accordion.vue";
import AccordionBtn from "./components/Accordion/AccordionButton.vue";

import "./main.css";

export default {
  name: "App",
  components: {
    Header,
    Btn,
    SectionComponent,
    Accordion,
    AccordionBtn,
  },
  data: () => ({
    sections: [
      {
        title: "about us",
        text:
          "The occupational traffic permit is one of the most important things in the company when carrying out freight transport. In fact, it is a prerequisite for doing business traffic at all.",
        warning:
          "How do you do when you need to obtain a commercial traffic permit for freight transport to your business?",
        img: "man.png",
      },
      {
        title: "How to apply",
        text:
          "When applying for a traffic permit, there are certain requirements that you must meet that are included in the examination: requirements for professional knowledge, solid establishment, good reputation and financial resources. Important to remember is to confirm your application for a traffic permit by the company's company signer or CEO.",
        img: "woman.png",
        left: true,
      },
    ],
    accordions: [
      {
        title: "What is a professional traffic permit?",
        text:
          "Traffic permits are a requirement for conducting professional traffic.",
      },
      {
        title: "How to check the traffic condition?",
        text:
          "Traffic permits are a requirement for conducting professional traffic.",
      },
      {
        title: "What are the requirements for a professional traffic permit?",
        text:
          "Traffic permits are a requirement for conducting professional traffic.",
      },
      {
        title:
          "Are there professional traffic permit training courses at a distance?",
        text:
          "Traffic permits are a requirement for conducting professional traffic.",
      },
      {
        title: "When is a professional traffic permit needed?",
        text:
          "Traffic permits are a requirement for conducting professional traffic.",
      },
      {
        title: "Where to look for a traffic permit?",
        text:
          "Traffic permits are a requirement for conducting professional traffic.",
      },
      {
        title:
          "Are there differences between a traffic permit and a professional traffic permit?",
        text:
          "Traffic permits are a requirement for conducting professional traffic.",
      },
      {
        title: "How much does a commercial traffic permit cost for goods?",
        text:
          "Traffic permits are a requirement for conducting professional traffic.",
      },
      {
        title: "How to plug in for the traffic permit test?",
        text:
          "Traffic permits are a requirement for conducting professional traffic.",
      },
      {
        title: "How is the sample for a professional traffic permit booked?",
        text:
          "Traffic permits are a requirement for conducting professional traffic.",
      },
    ],
  }),
};
</script>

<style>
body {
  background: #fef8f5;
  margin: 0;
  padding: 0;
}
</style>
