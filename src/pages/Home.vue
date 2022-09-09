<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <main>
    <div class="text-top">Vídeos novos toda <b>quinta</b> às <b>20h</b></div>
    <a href="https://youtube.com/wdevoficial" target="_blank">
      <img
        src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/subscribe.svg"
        alt="Inscreva-se"
        id="subscribe"
      />
      <div class="text-bottom">youtube.com/wdevoficial</div>
    </a>
  </main>
</template>

<style scoped>
main {
  background-color: var(--color-background-home);
  justify-content: center;
  align-items: center;
  text-align: center;
}

.text-top {
  color: var(--color-text-light);
  font-size: 22px;
}

#subscribe {
  margin-block: 20px;
  width: 340px;
}

.text-bottom {
  color: var(--color-text-light);
  font-size: 18px;
}

@media (min-width: 700px) {
  #subscribe {
    width: 370px;
  }
}
</style>
