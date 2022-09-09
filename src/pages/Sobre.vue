<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <main>
    <section class="container">
      <h1>Sobre</h1>

      <div class="about" v-html="about"></div>
    </section>
  </main>
</template>

<script>
import api from "@/services/api";
export default {
  data() {
    return { about: "" };
  },
  mounted() {
    api.get("/about.json").then(response => {
      this.about = response.data.about;
    });
  },
};
</script>

<style scoped>
main {
  align-items: center;
}

.about {
  margin-bottom: 30px;
  color: var(--color-text-dark);
}
</style>
