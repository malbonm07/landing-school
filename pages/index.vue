<template>
  <div class="container">
    <header class="header header__container">
      <div class="header__video">
        <video src="~/assets/video/internet.mp4" muted autoplay="true" loop="true"></video>
      </div>
      <div class="header__overlay"></div>
      <div class="header__box">
        <h1 class="text-h4 text-title text-space3">Lleva tu talento al siguiente nivel</h1>
        <p class="text-subtitle1 text-light">Construye tu camino profesional. Sin horarios ni límites. 100% Online.</p>
        <div class="header__box__button">
          <a class="text-subtitle1">Empezar ahora</a>
        </div>
      </div>
    </header>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style lang='scss'>

</style>
