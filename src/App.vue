<template>
  <div id="app">
    <Header :mudarRota="mudarRota" />
    <Home v-if="statePage === 'Home'" />
    <Videos v-if="statePage === 'Videos'" />
    <Sobre v-if="statePage === 'Sobre'" />
    <Contato v-if="statePage === 'Contato'" />
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/organisms/Header";
import Footer from "@/components/organisms/Footer";
import { Home, Videos, Sobre, Contato } from "@/pages";

export default {
  name: "App",

  data() {
    return { statePage: "Home" };
  },

  components: {
    Header,
    Home,
    Videos,
    Sobre,
    Contato,
    Footer,
  },

  methods: {
    mudarRota(link) {
      this.statePage = link;
    },
  },
};
</script>
