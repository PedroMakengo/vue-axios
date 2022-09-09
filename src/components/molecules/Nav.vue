<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <nav class="container">
    <Logo />
    <button id="menu-button" @click="$emit('openMenu')">
      <img
        src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg"
        alt="Abrir menu"
      />
    </button>

    <SideBarMenu
      v-if="menuActive"
      :classActive="classActive"
      @closeMenu="closeMenu"
    />
  </nav>
</template>

<script lang="js">
import { Logo } from "@/components/atoms";
import  SideBarMenu from "@/components/molecules/SideBarMenu.vue";

export default {
  props: {
    menuActive: {
      type: String,
      required: false
    },
    classActive: {
      type: String,
      required: false
    },
    closeMenu: {
      type: Function,
      required: true
    }
  },
  components: { Logo, SideBarMenu },
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
