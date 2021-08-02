<template>
  <main class="main">
    <Home />
    <About />
    <Skills />
    <Qualification />
    <Portfolio />
    <ProjectsInMind />
    <Certifications />
    <ContactMe />
  </main>
</template>

<script>
import Home from "./Home.vue";
import About from "./About.vue";
import Skills from "./Skills.vue";
import Qualification from "./Qualification.vue";
import Portfolio from "./Portfolio.vue";
import ProjectsInMind from "./ProjectsInMind.vue";
import Certifications from "./Certifications.vue";
import ContactMe from "./ContactMe.vue";
export default {
  name: "Main",
  components: {
    Home,
    About,
    Skills,
    Qualification,
    Portfolio,
    ProjectsInMind,
    Certifications,
    ContactMe,
  },
};
</script>

<style></style>
