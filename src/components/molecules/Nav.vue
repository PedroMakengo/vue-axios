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

    <div id="menu-overlay"></div>
  </nav>
</template>

<script>
import { Logo } from "@/components/atoms";
export default {
  components: { Logo },
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

#menu-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 40%;
  height: 100vh;
  background-color: #000;
  opacity: 0.8;
}

#menu-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 40%;
  height: 100vh;
  background-color: #000;
  opacity: 0.8;
}
</style>
