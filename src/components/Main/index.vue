<template>
  <main class="main">
    <Home />
    <About />
    <Skills />
    <Qualification />
    <Portfolio />
  </main>
</template>

<script>
import Home from "./Home.vue"
import About from "./About.vue"
import Skills from "./Skills.vue"
import Qualification from "./Qualification.vue"
import Portfolio from "./Portfolio.vue"
export default {
  name: "Main",
  components: {
    Home,
    About,
    Skills,
    Qualification,
    Portfolio,
  },
}
</script>

<style></style>
