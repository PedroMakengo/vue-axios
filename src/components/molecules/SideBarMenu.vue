<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="sidebar">
    <div id="menu-overlay" v-if="menuActive" @click="$emit('closeMenu')"></div>
    <div id="menu-items" :class="classActive">
      <Logo classLogo="logo" />
      <ul>
        <LinkNavegator
          v-for="link of links"
          :key="link.id"
          :to="link.to"
          :text="link.text"
          @click.prevent="$emit('mudarRota', link.text)"
          @click="$emit('closeMenu')"
        />
      </ul>
    </div>
  </div>
</template>

<script lang="js">
import { Logo, LinkNavegator } from "@/components/atoms";

export default {
  data(){
    return {
      links: [
        { id: 1, to: "/", text:"Home"},
        { id: 2, to: "/videos", text:"Videos"},
        { id: 3, to: "/sobre", text:"Sobre"},
        { id: 4, to: "/contato", text:"Contato"},
      ]
    }
  },
  props: {
    classActive: {
      type: String,
      required: false
    },
    menuActive: {
      type: String,
      required: false
    },
  },
  components: { Logo, LinkNavegator },
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

  display: none;
  flex-direction: column;
  align-items: center;
}

#menu-items.active {
  display: flex;
}

ul {
  text-align: center;
}

ul li {
  margin: 20px 0;
}

@media (min-width: 700px) {
  #menu-overlay {
    display: none;
  }

  #menu-items {
    display: flex;
    position: static;
    height: 60px;
    width: auto;
  }

  ul {
    display: flex;
    height: 100%;
    align-items: center;
  }

  ul li {
    margin: 0;
    margin-left: 20px;
  }
}
</style>
