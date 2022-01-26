<template>
  <div id="app">
    <Header />
    <Jumbotron />
    <SectionStory />
    <SectionServices />
    <SectionProcedure />
    <SectionResult />
    <SectionFeedback />
    <SectionContact />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Jumbotron from "./components/Jumbotron.vue"
import SectionStory from "./components/SectionStory.vue"
import SectionServices from "./components/SectionServices.vue"
import SectionProcedure from "./components/SectionProcedure.vue"
import SectionResult from "./components/SectionResult.vue"
import SectionFeedback from "./components/SectionFeedback.vue"
import SectionContact from "./components/SectionContact.vue"
import Footer from "./components/Footer.vue"

export default {
  name: "App",
  components: {
    Header,
    Jumbotron,
    SectionStory,
    SectionServices,
    SectionProcedure,
    SectionResult,
    SectionFeedback,
    SectionContact,
    Footer
  },
};
</script>

<style lang="scss">
@import "./assets/style.scss";
</style>
