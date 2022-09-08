<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <nav class="container">
    <Logo />
    <button id="menu-button">
      <img
        src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg"
        alt="Abrir menu"
      />
    </button>

    <MenuOverlay />
  </nav>
</template>

<script>
import { Logo } from "@/components/atoms";
import { MenuOverlay } from "@/components/molecules";

export default {
  components: { Logo, MenuOverlay },
};
</script>

<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100%;
}

#menu-button {
  width: 30px;
}

#menu-button img {
  width: 100%;
}
</style>
