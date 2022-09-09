<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <a href="/">
    <img
      src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg"
      alt="WDED"
      :class="[classLogo, 'logoDefault']"
    />
  </a>
</template>

<script>
export default {
  props: {
    classLogo: {
      type: String,
      required: false,
    },
  },
};
</script>

<style scoped>
.logoDefault {
  width: 130px;
}

.logo {
  width: 110px;
  margin-top: 30px;
  margin-bottom: 10px;
}

@media (min-width: 700px) {
  .logo {
    display: none;
  }
}
</style>
