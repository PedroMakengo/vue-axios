<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="sidebar">
    <div id="menu-overlay" @click="$emit('closeMenu')"></div>
    <div id="menu-items" :class="classActive">
      <Logo classLogo="logo" />
      <ul>
        <LinkNavegator
          v-for="link of links"
          :key="link.id"
          :to="link.to"
          :text="link.text"
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
        { id: 2, to: "/videos", text:"Vídeos"},
        { id: 3, to: "/sobre", text:"Sobre"},
        { id: 4, to: "/contato", text:"Contato"},
      ]
    }
  },
  props: {
    classActive: {
      type: String,
      required: false
    }
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
</style>
