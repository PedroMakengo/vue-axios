<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <footer>
    <a
      v-for="socialLink of socialLinks"
      :key="socialLink"
      class="socialLink"
      :href="socialLink"
    >
      <img :src="socialLink.icon" :alt="socialLink.label" />
    </a>
  </footer>
</template>

<script>
import api from "@/services/api";
export default {
  data() {
    return { socialLinks: [] };
  },
  mounted() {
    api
      .get("social-links.json")
      .then(response => (this.socialLinks = response.data));
  },
};
</script>

<style scoped>
footer {
  width: 100%;
  height: 60px;
  background-color: var(--color-background-nav);
  display: flex;
  align-items: center;
  justify-content: center;
}

.socialLink {
  border: 1px solid var(--color-text-light);
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;

  width: 40px;
  height: 40px;
  margin: 0 10px;
}

.socialLink img {
  width: 20px;
}
</style>
