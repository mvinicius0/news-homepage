<template>
  <HeaderComp />
  <MainSection />
</template>

<script lang="ts">
import HeaderComp from "./components/HeaderComp.vue";
import MainSection from "./components/MainSection.vue";
export default {
  name: "App",
  components: {
    HeaderComp,
    MainSection,
  },

  data() {
    return {};
  },
};
</script>

<style lang="scss">
.body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: $font-primary;
}

#app {
  height: 100vh;
  margin: 5% 10%;
  background: $primary-color;
}
</style>
