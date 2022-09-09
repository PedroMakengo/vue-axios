<template>
  <div id="app">
    <Header />
    <Home />
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/organisms/Header";
import Footer from "@/components/organisms/Footer";
import Home from "@/pages/Home.vue";

export default {
  name: "App",

  components: {
    Header,
    Home,
    Footer,
  },
};
</script>
