<template>
  <Header />
  <Main />
</template>

<script>
import Header from "./components/Navigation/Header.vue"
import Main from "./components/Main"

export default {
  name: "App",
  components: {
    Header,
    Main,
  },
}
</script>
