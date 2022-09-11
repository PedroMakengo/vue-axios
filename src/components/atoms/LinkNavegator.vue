<template>
  <li class="link-navegator">
    <router-link class="link" :to="to">{{ text }}</router-link>
  </li>
</template>

<script>
export default {
  props: {
    to: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.link {
  color: var(--color-text-light);
  cursor: pointer;
}
</style>
