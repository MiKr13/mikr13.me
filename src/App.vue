<template>
  <Header />
  <Main />
  <Footer />
</template>

<script>
import Header from "./components/Navigation/Header.vue";
import Main from "./components/Main";
import Footer from "./components/Navigation/Footer";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
};
</script>
