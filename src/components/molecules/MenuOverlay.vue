<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div id="menu-overlay">
    <div id="menu-items">
      <Logo />
      <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/videos">Video</a></li>
        <li><a href="/sobre">Sobre</a></li>
        <li><a href="/contato">Contato</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
import { Logo } from "@/components/atoms";

export default {
  components: { Logo },
};
</script>

<style scoped>
#menu-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 40%;
  height: 100vh;
  background-color: #000;
  opacity: 0.8;
}

#menu-items {
  position: fixed;
  top: 0;
  right: 0;
  background-color: var(--color-background-nav);
  width: 60%;
  height: 100vh;
}
</style>
