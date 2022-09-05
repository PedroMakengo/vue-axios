<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <header>
    <Nav />
  </header>
</template>

<script>
import { Nav } from "@/components/molecules";
export default {
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
