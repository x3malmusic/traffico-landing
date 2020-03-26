<template>
  <div class="acc-wrapper">
    <div class="accordion" @click="active = !active">
      <div class="content">{{ title }}</div>
      <div class="char">{{ this.active ? "-" : "+" }}</div>
    </div>
    <transition name="fade">
      <div v-if="active" :class="active ? 'active' : 'not-active'">
        {{ text }}
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: "Accordion",
  data: () => ({
    active: false,
  }),
  props: {
    title: String,
    text: String,
  },
};
</script>

<style scoped>
@import "./accordion.css";

.fade-enter-active,
.fade-leave-active {
  transition: all 0.5s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
  transform: translateY(-80px);
}
</style>
