<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <header>
    <nav class="container">
      <a href="/">
        <img
          src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg"
          alt="WDED"
          id="logo"
        />
      </a>

      <button id="menu-button">
        <img
          src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg"
          alt="Abrir menu"
        />
      </button>

      <div id="menu-overlay"></div>
    </nav>
  </header>
</template>

<script>
export default {};
</script>

<style scoped>
header {
  background-color: var(--color-background-nav);
  height: 60px;
  width: 100%;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100%;
}

#logo {
  width: 130px;
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
</style>
