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
        <button class="header__box__button">
          <a class="text-subtitle1 text-white">Empezar ahora</a>
        </button>
      </div>
    </header>
    <section class="sub-header">
      <div class="sub-header__item">
        <div class="sub-header__item--icon">
          <font-awesome-icon :icon="['fas', 'hourglass-half']"/>
        </div>
        <h3 class="text-h5">Aprende a tu ritmo</h3>
        <p>Cursos las 24h sin caducidad</p>
      </div>
      <div class="sub-header__item">
        <div class="sub-header__item--icon">
          <font-awesome-icon :icon="['fas', 'lightbulb']"/>
        </div>
        <h3 class="text-h5">Crea Proyectos</h3>
        <p>Cursos las 24h sin caducidad</p>
      </div>
      <div class="sub-header__item">
        <div class="sub-header__item--icon">
          <font-awesome-icon :icon="['fas', 'star']"/>
        </div>
        <h3 class="text-h5">Certificate</h3>
        <p>Cursos las 24h sin caducidad</p>
      </div>
    </section>
    <section class="cursos-section">
      <div v-swiper:mySwiper="swiperOption" class="swiper-container">
          <ul class="swiper-wrapper">
              <li class="swiper-slide" v-for="(course, i) in courses" :key="i">
                <sliderCard :courseObject="course">
                </sliderCard>
              </li>
          </ul>
          <div class="swiper-pagination__content">
            <button
                class="swiper-button swiper-left"
            >
                <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-left']"/>
            </button>
            <div class="swiper-pag" slot="pagination"></div>
            <button
                class="swiper-button swiper-right"
            >
                <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-right']"/>
            </button>
          </div>
      </div>
      <div class="text-medium text-subtitle1" style="text-align:center; margin-top: 2rem; color: #62D4DD;">
        <a>Explora todo Aquí</a>
      </div>
    </section>
    <hr class="separator-fluid">
    <section class="stats-section">
      <div class="stats-flex">
        <div class="stats-title text-h4 text-medium text-center">
          Formando los lideres del<br><span style="color: #4B22F4;">sector creative</span>
        </div>
        <ul class="stats-list">
          <li class="stats-list__li text-center text-h3 text-title">900,009<span style="display:block; margin-top: 1rem;" class="text-body1 text-grey1">ALUMNOS APRENDIENDO</span></li>
          <li class="stats-list__li text-center text-h3 text-title">+500<span style="display:block; margin-top: 1rem;" class="text-body1 text-grey1">CURSOS DISPONIBLES</span></li>
          <li class="stats-list__li text-center text-h3 text-title">10,608<span style="display:block; margin-top: 1rem;" class="text-body1 text-grey1">PROYECTOS CERTIFICADOS</span></li>
        </ul>
      </div>
    </section>
    <section>
      <div v-swiper:mySwiper2="swiperOption2" class="swiper-container">
          <ul class="swiper-wrapper">
              <li class="swiper-slide" v-for="(banner, index) in banners" :key="index">
                <sliderCardImg :dataObject="banner">
                </sliderCardImg>
              </li>
          </ul>
      </div>
    </section>
  </div>
</template>

<script>
import sliderCard from '~/components/sliderCard.vue'
import sliderCardImg from '~/components/sliderCardImg.vue'
import img1 from '~/assets/imagens/courses/img1.jpg'
import img2 from '~/assets/imagens/courses/img2.jpg'
import img3 from '~/assets/imagens/courses/img3.jpg'

export default {
  components: {
    sliderCard,
    sliderCardImg
  },
  data () {
      return {
            courses: [
              {
                img: "https://images.pexels.com/photos/1438081/pexels-photo-1438081.jpeg?cs=srgb&dl=casual-college-connection-1438081.jpg&fm=jpg",
                title: "Aprender a dibujar al estilo cómic",
                nivel: "Nivel introductorio",
                precio: 29.99,
                link: "null",
                students: "176",
                time: "2h 21m"
              },
              {
                img: "https://images.pexels.com/photos/1438081/pexels-photo-1438081.jpeg?cs=srgb&dl=casual-college-connection-1438081.jpg&fm=jpg",
                title: "Aprender a dibujar al estilo cómic",
                nivel: "Nivel introductorio",
                precio: 29.99,
                link: "null",
                students: "176",
                time: "2h 21m"
              },
              {
                img: "https://images.pexels.com/photos/1438081/pexels-photo-1438081.jpeg?cs=srgb&dl=casual-college-connection-1438081.jpg&fm=jpg",
                title: "Aprender a dibujar al estilo cómic",
                nivel: "Nivel introductorio",
                precio: 29.99,
                link: "null",
                students: "176",
                time: "2h 21m"
              },
              {
                img: "https://images.pexels.com/photos/1438081/pexels-photo-1438081.jpeg?cs=srgb&dl=casual-college-connection-1438081.jpg&fm=jpg",
                title: "Aprender a dibujar al estilo cómic",
                nivel: "Nivel introductorio",
                precio: 49.99,
                link: "null",
                students: "176",
                time: "2h 21m"
              },
              {
                img: "https://images.pexels.com/photos/1438081/pexels-photo-1438081.jpeg?cs=srgb&dl=casual-college-connection-1438081.jpg&fm=jpg",
                title: "Aprender a dibujar al estilo cómic",
                nivel: "Nivel introductorio",
                precio: 49.99,
                link: "null",
                students: "176",
                time: "2h 21m"
              },
              {
                img: "https://images.pexels.com/photos/1438081/pexels-photo-1438081.jpeg?cs=srgb&dl=casual-college-connection-1438081.jpg&fm=jpg",
                title: "Aprender a dibujar al estilo cómic",
                nivel: "Nivel introductorio",
                precio: 49.99,
                link: "null",
                students: "176",
                time: "2h 21m"
              },
            ],
            swiperOption: {
                slidesPerView: 'auto',
                // centeredSlides: true,
                spaceBetween: 15,
                slidesPerView: 1.5,
                freeMode: true,
                loop: false,
                navigation: {
                    nextEl: '.swiper-right',
                    prevEl: '.swiper-left'
                },
                pagination: {
                  el: '.swiper-pag',
                  type: 'fraction'
                },
            },
            banners: [
              {
                img: img1,
                title: 'ilustracion y diseño',
                description: '4h 20m'
              },
              {
                img: img2,
                title: 'introduccion a la direccion de fotografia',
                description: '5h 10m'
              },
              {
                img: img3,
                title: 'aprende a tocar diferentes instrumentos',
                description: '7h 25m'
              },
              {
                img: img2,
                title: 'introduccion a la direccion de fotografia',
                description: '5h 10m'
              }
            ],
            swiperOption2: {
              spaceBetween: 30,
              slidesPerView: 1.5,
              loop: true,
              pagination: {
                el: '.swiper-pagination'
              },
              // some swiper options...
            }
      }
  },
  mounted() {
  }
}
</script>

<style lang='scss'>

</style>
