<template>
  <div id="app">
    <Header />
    <Jumbotron />
    <SectionStory />
    <SectionServices />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Jumbotron from "./components/Jumbotron.vue"
import SectionStory from "./components/SectionStory.vue"
import SectionServices from "./components/SectionServices.vue"
import Footer from "./components/Footer.vue"

export default {
  name: "App",
  components: {
    Header,
    Jumbotron,
    SectionStory,
    SectionServices,
    Footer
  },
};
</script>

<style lang="scss">
@import "./assets/style.scss";
</style>
