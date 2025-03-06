<template>
  <HeaderComp />
  <MainSection />
  <FooterComp />
</template>

<script lang="ts">
import FooterComp from "./components/FooterComp.vue";
import HeaderComp from "./components/HeaderComp.vue";
import MainSection from "./components/MainSection.vue";

export default {
  name: "App",
  components: {
    HeaderComp,
    MainSection,
    FooterComp,
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
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
  background: $primary-color;
}

@media (max-width: 768px) {
  #app {
    padding: 0;
  }
}
</style>
