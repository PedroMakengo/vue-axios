<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <header>
    <Nav :menuActive="menuActive" :classActive="{ active: menuActive }" />
  </header>
</template>

<script>
import { Nav } from "@/components/molecules";
export default {
  data() {
    return { menuActive: true };
  },
  components: { Nav },
  methods: {
    openMenu: function () {
      this.menuActive = true;
    },
    closeMenu: function () {
      this.menuActive = false;
    },
  },
};
</script>

<style scoped>
header {
  background-color: var(--color-background-nav);
  height: 60px;
  width: 100%;
}
</style>
