<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <header>
    <Nav :menuActive="menuActive" />
  </header>
</template>

<script>
import { Nav } from "@/components/molecules";
export default {
  data() {
    return { menuActive: false };
  },
  components: { Nav },
};
</script>

<style scoped>
header {
  background-color: var(--color-background-nav);
  height: 60px;
  width: 100%;
}
</style>
