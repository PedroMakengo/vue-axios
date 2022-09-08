<template>
  <li class="link-navegator">
    <a :href="to">{{ text }}</a>
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
a {
  color: var(--color-text-light);
}
</style>
