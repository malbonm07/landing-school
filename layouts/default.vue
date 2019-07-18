<template>
  <div class="main__container">
    <nav class="navbar">
      <div class="navbar__block">
        <div class="navbar__menu">
          <font-awesome-icon :icon="['fas', 'bars']"/>
        </div>
        <div class="navbar__search">
          <font-awesome-icon :icon="['fas', 'search']"/>
        </div>
      </div>
      <div class="navbar__logo">
        <div><h1 class="text-h6 text-space1">CREHANA</h1></div>
      </div>
      <div class="navbar__buy">
        <font-awesome-icon :icon="['fas', 'shopping-cart']"/>
      </div>
    </nav>
    <nuxt />
    <footer class="footer">
      <div class="footer__box1">
        <div class="footer__dropdown">
          <div class="footer__dropdown--title text-grey1 dropdown" ref="dropdown">CATEGORÍAS<span style="width:100%;" class="text-right text-body1 chevron"><font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-right']"/></span></div>
          <div class="footer__dropdown--list">
            <a>Cursos de Ilustración y Dibujo</a>
            <a>Cursos de Diseño</a>
            <a>Cursos de Animación & 3D</a>
            <a>Cursos de Web</a>
            <a>Cursos de Fotografía</a>
            <a>Cursos de Marketing Digital</a>
          </div>
        </div>
        <div class="footer__dropdown">
          <div class="footer__dropdown--title text-grey1 dropdown" ref="dropdown">SOFTWARE<span style="width:100%;" class="text-right text-body1 chevron"><font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-right']"/></span></div>
          <div class="footer__dropdown--list">
            <a>Cursos de Adobe Animate CC</a>
            <a>Cursos de Audition</a>
            <a>Cursos de Photoshop Lightroom</a>
            <a>Cursos de Premiere</a>
            <a>Cursos de Illustrator</a>
            <a>Cursos de Adobe Photoshop</a>
          </div>
        </div>
        <div class="footer__dropdown">
          <div class="footer__dropdown--title text-grey1 dropdown" ref="dropdown">CONÓCENOS<span style="width:100%;" class="text-right text-body1 chevron"><font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-right']"/></span></div>
          <div class="footer__dropdown--list">
            <a>estamos contratando!</a>
            <a>sobre crehana</a>
            <a>terminos y condiciones</a>
            <a>politicas de privacidad</a>
            <a>politica de cookies</a>
            <!-- <a>solicitudes</a> -->
          </div>
        </div>
        <div class="footer__dropdown">
          <div class="footer__dropdown--title text-grey1 dropdown" ref="dropdown">COMUNIDAD<span style="width:100%;" class="text-right text-body1 chevron"><font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-right']"/></span></div>
          <div class="footer__dropdown--list">
            <a>becas</a>
            <a>historias</a>
            <a>tarjetas de regalo</a>
            <a>proyectos</a>
            <a>recursos</a>
            <a>blog</a>
          </div>
        </div>
      </div>
      <div class="footer__box2">
        <div class="footer__boxicons">
          <div class="footer__boxicons--item"><font-awesome-icon :icon="['fab', 'facebook-f']"/></div>
          <div class="footer__boxicons--item"><font-awesome-icon :icon="['fab', 'twitter']"/></div>
          <div class="footer__boxicons--item"><font-awesome-icon :icon="['fab', 'instagram']"/></div>
          <div class="footer__boxicons--item"><font-awesome-icon :icon="['fab', 'linkedin']"/></div>
          <div class="footer__boxicons--item"><font-awesome-icon :icon="['fab', 'youtube']"/></div>
        </div>
        <div class="footer__boxbuttons">
          <h5 class="text-grey1" style="line-height: 3rem;">DESCARGA NUESTRA APP EN:</h5>
          <button class="btn text-subtitle1 text-white" style="margin-bottom: 20px;">
            <span class="text-h6"><font-awesome-icon :icon="['fab', 'google-play']"/></span>
            Google play
          </button>
          <button class="btn text-subtitle1 text-white">
            <span class="text-h6"><font-awesome-icon :icon="['fab', 'apple']"/></span>
            App store
          </button>
          <button class="btn-outline text-body1 text-black" style="margin-top:40px; margin-bottom: 40px;">
            <span><font-awesome-icon :icon="['fas', 'comments-dollar']"/></span>
            Perú | $/(PEN)
          </button>
        </div>
      </div>
    </footer>
    <hr class="separator">
    <div class="footer__copyright">
      <div>
        <h6 class="text-grey2 text-regular text-space3" style="text-align: center;">Copyright&#169; Crehana 2019</h6>
        <h6 class="text-grey2 text-regular text-space3" style="text-align: center;">Todos los derechos reservados</h6>
      </div>
    </div>
  </div>
</template>
<!-- <p>Icons</p>
<font-awesome-icon :icon="['fab', 'facebook']"/>
<font-awesome-icon :icon="['fab', 'github']"/>
<font-awesome-icon :icon="['fab', 'facebook']"/>
<font-awesome-icon :icon="['fas', 'shopping-cart']"/> -->
<script>

export default {
  mounted() {
    let dropdownBtn = document.querySelectorAll('.footer__dropdown--title');
    let dropdownList = document.querySelectorAll('.footer__dropdown--list');
    const dropdownBtnArray = Array.from(dropdownBtn)
    dropdownBtnArray.forEach(btn => {
      btn.addEventListener('click', () => {
        btn.classList.toggle('active');
        let btnContent = btn.nextElementSibling;
        let btnIcon = btn.childNodes[1].childNodes[0]
        btnContent.classList.toggle('activeDropdownContent')
        btnIcon.classList.toggle('activeChevron')
      })
    })

  }
}
</script>

<style lang="scss">
*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
</style>
