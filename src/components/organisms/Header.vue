<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <header>
    <Nav
      :menuActive="menuActive"
      :classActive="{ active: menuActive }"
      @openMenu="openMenu"
      :closeMenu="closeMenu"
      :mudarRota="mudarRota"
    />
  </header>
</template>

<script>
import { Nav } from "@/components/molecules";
export default {
  data() {
    return { menuActive: false };
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
  props: {
    mudarRota: {
      type: Function,
      required: true,
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
