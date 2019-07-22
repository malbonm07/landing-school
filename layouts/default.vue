<template>
  <div class="main__container">

    <!-------------------------- NAVBAR -------------------------->
    <nav class="navbar">
      <div class="navbar__block">
        <div class="navbar__search">
          <font-awesome-icon :icon="['fas', 'search']"/>
        </div>
      </div>
      <div class="navbar__logo">
        <div><h1 class="text-h6 text-title text-space3">CREHANA</h1></div>
      </div>
      <div class="navbar__buy">
        <font-awesome-icon :icon="['fas', 'shopping-cart']"/>
      </div>
    </nav>
    <!-------------------------- END NAVBAR -------------------------->



    <!-------------------------- NAVBAR IN DESKTOP -------------------------->
    <div class="desktop-nav pl-2 pr-2">
      <div class="desktop-nav__logo">
        <h2 class="text-space4">CREHANA</h2>
        <div class="logo-btn__appear-menu">
          <button class="text-white desktop-nav__logo-btn text-body1" 
          @click.stop="showAprendeTabs = !showAprendeTabs">
            Aprende
          </button>
          <transition name="tabs">
            <div v-if="showAprendeTabs" class="aprende-tab-menu">
              <div class="aprende-tab-menu__header">
                <button
                  class="aprende-tab__btn text-body1 mr-4" 
                  @click="currentAprendeTab = tabs[0]"
                  :class="{'tab-active' : currentAprendeTab === tabs[0]}"
                >
                  <span><font-awesome-icon :icon="['fas', 'book']"/></span>
                  Cursos
                </button>
                <button
                  class="aprende-tab__btn text-body1" 
                  @click="currentAprendeTab = tabs[1]"
                  :class="{'tab-active' : currentAprendeTab === tabs[1]}"
                >
                  <span><font-awesome-icon :icon="['fas', 'chalkboard']"/></span>
                  Carreras
                </button>
                <button
                  class="aprende-tab__btn text-body1 ml-4" 
                  @click="currentAprendeTab = tabs[2]"
                  :class="{'tab-active' : currentAprendeTab === tabs[2]}"
                >
                  <span><font-awesome-icon :icon="['fas', 'certificate']"/></span>
                  Certificaciones
                </button>
                <button class="close-tabs-menu" 
                @click.stop="closeAprendeTabs"
                >
                  <font-awesome-icon :icon="['fas', 'times']"/>
                </button>
              </div>
              <div class="aprende-tab-menu__banner">
                <keep-alive>
                  <component v-bind:is='currentAprendeTabComponent'>
                  </component>
                </keep-alive>
              </div>
              <div class="aprende-tab-menu__aside">
                <div class="aprende-tab-menu__aside__img">
                  <img src="~/assets/imagens/promo/img1.jpg" alt="promo imagen" width="100%">
                </div>
                <p class="text-regular text-grey3 mt-1">Vive los mejores eventos.</p>
                <button class="aprende-tab-menu__aside__btn mt-2 text-white text-body1">
                  Ver Promociones
                </button>
              </div>
            </div>
          </transition>
          <transition name="tabs">
            <div v-if="showAprendeTabs" class="aprende-tabs-overlay"
            @click.stop="closeAprendeTabs"
            >
            </div>
            </transition>
        </div>
        <div class="desktop-nav__line"></div>
      </div>
      <div class="desktop-nav__search">
        <span class="desktop-nav__search-btn">
          <font-awesome-icon class="search-btn-icon" :icon="['fas', 'search']"/>
        </span>
      </div>
      <div class="desktop-nav__links">
        <a>Lives</a>
        <a>Blog</a>
        <a>Membresias</a>
        <div class="desktop-nav__line"></div>
        <a><font-awesome-icon :icon="['fas', 'shopping-cart']"/></a>
        <button class="text-white desktop-nav__links-login text-body1">Ingresar</button>
        <button class="text-white desktop-nav__links-registration text-body1">Regístrate</button>
      </div>
    </div>
    <!-------------------------- END NAVBAR IN DESKTOP -------------------------->



    <!-------------------------- MENU HAMBURGUER -------------------------->
    <div class="navbar__menu">
      <input type="checkbox" id="menu-toggle" @click="show = !show">
      <label for="menu-toggle" class="menu-toggle-label">
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
      </label>
      <!-- <font-awesome-icon :icon="['fas', 'bars']"/> -->
    </div>
    <!-------------------------- END MENU HAMBURGUER -------------------------->



    <!-------------------------- NUXT VIEWS -------------------------->
    <nuxt />
    <!-------------------------- END NUXT VIEWS -------------------------->



    <!-------------------------- FOOTER -------------------------->
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
          <a class="footer__boxicons--item"><font-awesome-icon :icon="['fab', 'facebook-f']"/></a>
          <a class="footer__boxicons--item"><font-awesome-icon :icon="['fab', 'twitter']"/></a>
          <a class="footer__boxicons--item"><font-awesome-icon :icon="['fab', 'instagram']"/></a>
          <a class="footer__boxicons--item"><font-awesome-icon :icon="['fab', 'linkedin']"/></a>
          <a class="footer__boxicons--item"><font-awesome-icon :icon="['fab', 'youtube']"/></a>
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
    <!-------------------------- END FOOTER -------------------------->
    



    <!-------------------------- SIDE-BAR -------------------------->
    <div class="side-bar" :class="{'appear-sidebar': show}">
      <transition name="fade">
        <div v-if="show" class="side-bar__logo text-h6 text-center text-title text-space3 text-grey3">CREHANA</div>
      </transition>
        <div class="side-bar__content pr-2 pl-2 pb-2">
          <ul class="side-bar__content-list">
            <li class="pt-1 pb-1"><a class="text-subtitle1 text-light">Cursos<span></span></a></li>
            <li class="pt-1 pb-1"><a class="text-subtitle1 text-light">Lives</a></li>
            <li class="pt-1 pb-1"><a class="text-subtitle1 text-light">Blog</a></li>
            <li class="pt-1 pb-1"><a class="text-subtitle1 text-light">Membresías</a></li>
            <li class="pt-1 pb-1"><a class="text-subtitle1 text-light">Carreras</a></li>
            <li class="pt-1 pb-1"><a class="text-subtitle1 text-light">Certificaciones</a></li>
          </ul>
          <button class="btn-registration text-subtitle1 text-white mt-1 mb-1">Regístrate</button>
          <button class="btn-login text-subtitle1 text-grey mb-1">Iniciar Sesión</button>
          <div class="side-social">
            <div class="side-social__icon"><font-awesome-icon :icon="['fab', 'facebook-f']"/></div>
            <div class="side-social__icon"><font-awesome-icon :icon="['fab', 'twitter']"/></div>
            <div class="side-social__icon"><font-awesome-icon :icon="['fab', 'instagram']"/></div>
            <div class="side-social__icon"><font-awesome-icon :icon="['fab', 'linkedin']"/></div>
            <div class="side-social__icon"><font-awesome-icon :icon="['fab', 'youtube']"/></div>
          </div>
          <h6 class="text-body1 text-medium text-center" style="color: #75DAE1;"><a>¿Necesitas ayuda?<br>Aquí te atenderemos</a></h6>
        </div>
      <div>

      </div>
    </div>
    <!-------------------------- END SIDE-BAR -------------------------->
    
  </div>
</template>

<script>

import cursosTab from '~/components/aprende-tabs/cursos.vue'
import carrerasTab from '~/components/aprende-tabs/carreras.vue'
import certificacionesTab from '~/components/aprende-tabs/certificaciones.vue'

export default {
  components: {
    cursosTab,
    carrerasTab,
    certificacionesTab
  },
  data() {
    return {
      show: false,
      currentAprendeTab: 'cursos',
      tabs: [
        'cursos',
        'carreras',
        'certificaciones'
      ],
      showAprendeTabs: false
    }
  },
  methods: {
    closeAprendeTabs() {
      if(this.showAprendeTabs) {
        this.showAprendeTabs = false
      }
    }
  },
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
  },
  computed: {
    currentAprendeTabComponent() {
      return `${this.currentAprendeTab}Tab`;
    }
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
