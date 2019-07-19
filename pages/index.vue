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
        <div class="sub-header__item--icon text-center">
          <font-awesome-icon :icon="['fas', 'hourglass-half']"/>
        </div>
        <h3 class="text-h5">Aprende a tu ritmo</h3>
        <p>Cursos las 24h sin caducidad</p>
      </div>
      <div class="sub-header__item">
        <div class="sub-header__item--icon text-center">
          <font-awesome-icon :icon="['fas', 'lightbulb']"/>
        </div>
        <h3 class="text-h5">Crea Proyectos</h3>
        <p>Cursos las 24h sin caducidad</p>
      </div>
      <div class="sub-header__item">
        <div class="sub-header__item--icon text-center">
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
    <section class="lanza-section mt-4">
      <div class="lanza-section__title">
        <div class="lanza-section__title-flex line-height3">
          <p class="text-caption text-regular pt-2">ENTÉRATE DE LO ÚLTIMO</p>
          <h4 class="text-h4 pb-2">Lanzamientos recientes</h4>
        </div>
      </div>
      <div class="lanza-section__swiper">
        <div v-swiper:mySwiper2="swiperOption2" class="swiper-container">
            <ul class="swiper-wrapper">
                <li class="swiper-slide" v-for="(banner, index) in banners" :key="index">
                  <sliderCardImg :dataObject="banner">
                  </sliderCardImg>
                </li>
            </ul>
            <div class="swiper-pagination__content">
              <button
                  class="swiper-button swiper2-left"
              >
                  <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-left']"/>
              </button>
              <div class="swiper2-pag" slot="pagination"></div>
              <button
                  class="swiper-button swiper2-right"
              >
                  <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-right']"/>
              </button>
            </div>
        </div>
      </div>
    </section>
    <section class="lanza-section-info mt-4">
      <div class="lanza-section-info__flex">
        <div class="lanza-section-info__description">
          <h4 class="text-h4 text-title text-center pl-1 pr-1 mb-2">Elige tu propio camino</h4>
          <p class="text-subtitle1 text-center pl-1 pr-1 mb-3">Los mejores expertos de la industria que guiarán tu aprendizaje te comunicarán lo mejor de sus experiencias.</p>
        </div>
        <div class="lanza-section-info__swiper">
          <div v-swiper:mySwiper3="swiperOption3" class="swiper-container mt-4">
              <ul class="swiper-wrapper">
                  <li class="swiper-slide">
                    <div class="swiper-info__card card1" style="transform: translateY(60px);">
                      <h5 class="text-subtitle1 mb-1">Carreras</h5>
                      <p class="text-body1 text-light text-left line-height1 mb-2">Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                      sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco</p>
                      <a class="text-body1">
                        Explorar carreras
                        <span class="text-body1 ml-1"><font-awesome-icon class="chevronIcon" :icon="['fas', 'arrow-right']"/>
                        </span>
                      </a>
                    </div>
                  </li>
                  <li class="swiper-slide">
                    <div class="swiper-info__card card2" style="transform: translateY(30px)">
                      <h5 class="text-subtitle1 mb-1">Certificaciones</h5>
                      <p class="text-body1 text-light text-left line-height1 mb-2">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor. Dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco</p>
                      <a class="text-body1">
                        Explorar certificaciones
                        <span class="text-body1 ml-1"><font-awesome-icon class="chevronIcon" :icon="['fas', 'arrow-right']"/>
                        </span>
                      </a>
                    </div>
                  </li>
                  <li class="swiper-slide">
                    <div class="swiper-info__card card3">
                      <h5 class="text-subtitle1 mb-1">Cursos</h5>
                      <p class="text-body1 text-light text-left line-height1 mb-2">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna.</p>
                      <a class="text-body1">
                        Explorar cursos
                        <span class="text-body1 ml-1"><font-awesome-icon class="chevronIcon" :icon="['fas', 'arrow-right']"/>
                        </span>
                      </a>
                    </div>
                  </li>
              </ul>
              <!-- <div class="swiper-pagination__content">
                <button
                    class="swiper-button swiper2-left"
                >
                    <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-left']"/>
                </button>
                <div class="swiper-pag" slot="pagination"></div>
                <button
                    class="swiper-button swiper2-right"
                >
                    <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-right']"/>
                </button>
              </div> -->
          </div>   
        </div>
      </div>
    </section>
    <section class="exp-section mt-4">
      <div>
        <div>
          <h4 class="text-h4 text-title text-center pl-1 pr-1 mb-2">Los mejores expertos de Latinoamerica</h4>
          <p class="text-subtitle1 text-center pl-1 pr-1 mb-3">Los mejores expertos de la industria que guiaran tu aprendizaje te comunicarán lo mejor de sus experiencias.</p>
        </div>
        <div>
          <div v-swiper:mySwiper4="swiperOption4" class="swiper-container">
              <ul class="swiper-wrapper">
                  <li class="swiper-slide" v-for="(teacher, index) in teachers" :key="index">
                    <teacherCard :dataObject="teacher">
                    </teacherCard>
                  </li>
              </ul>
              <div class="swiper-pagination__content">
                <button
                    class="swiper-button swiper4-left"
                >
                    <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-left']"/>
                </button>
                <div class="swiper4-pag" slot="pagination"></div>
                <button
                    class="swiper-button swiper4-right"
                >
                    <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-right']"/>
                </button>
              </div>
          </div>
        </div>
      </div>
    </section>
    <section class="casos-section mt-4 mb-4">
      <div>
        <h4 class="text-h4 text-title text-center pl-1 pr-1 mb-2">Nuestros casos de éxito</h4>
      </div>
      <div>
        <div v-swiper:mySwipe5="swiperOption5" class="swiper-container">
            <ul class="swiper-wrapper">
                <li class="swiper-slide" v-for="(caso, i) in casos" :key="i">
                  <casosCard :casoObject="caso">
                  </casosCard>
                </li>
            </ul>
            <div class="swiper-pagination__content">
              <button
                  class="swiper-button swiper5-left"
              >
                  <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-left']"/>
              </button>
              <div class="swiper5-pag" slot="pagination"></div>
              <button
                  class="swiper-button swiper5-right"
              >
                  <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-right']"/>
              </button>
            </div>
        </div>
      </div>
    </section>
    <section class="call-section">
      <div class="call-section__premium pl-1 pr-1 pt-3 pb-3">
        <span class="text-caption mb-1 block">PREMIUM</span>
        <h4 class="text-h4 text-title mb-2">Obtén accseso total al catalogo con una membresia.</h4>
        <button class="call-section__premium--btn text-body1 text-white text-medium text-space4">
          Me interesa
        </button>
      </div>
      <div class="call-section__empresas pl-1 pr-1 pt-3 pb-3">
        <span class="text-caption mb-1 block">EMPRESAS</span>
        <h4 class="text-h4 text-title mb-2">Potencia el talento de tu equipo con nuestros planes</h4>
        <button class="call-section__empresas--btn text-body1 text-white text-medium text-space4">
          Entérate más
        </button>
      </div>
    </section>
  </div>
</template>

<script>
import sliderCard from '~/components/sliderCard.vue'
import sliderCardImg from '~/components/sliderCardImg.vue'
import teacherCard from '~/components/teacherCard.vue'
import casosCard from '~/components/casosCard.vue'

import img1 from '~/assets/imagens/courses/img1.jpg'
import img2 from '~/assets/imagens/courses/img2.jpg'
import img3 from '~/assets/imagens/courses/img3.jpg'

import teacher1 from '~/assets/imagens/teachers/img1.jpg'
import teacher2 from '~/assets/imagens/teachers/img2.jpg'
import teacher3 from '~/assets/imagens/teachers/img3.jpg'
import teacher4 from '~/assets/imagens/teachers/img4.jpg'

import caso1 from '~/assets/imagens/casos/img1.jpg'
import caso2 from '~/assets/imagens/casos/img2.jpg'
import caso3 from '~/assets/imagens/casos/img3.jpg'
import caso4 from '~/assets/imagens/casos/img4.jpg'

export default {
  components: {
    sliderCard,
    sliderCardImg,
    teacherCard,
    casosCard
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
                spaceBetween: 20,
                slidesPerView: 4,
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
                breakpoints: {
                  1024: {
                    slidesPerView: 4,
                    spaceBetween: 20,
                  },
                  768: {
                    slidesPerView: 3,
                    spaceBetween: 20
                  },
                  640: {
                    slidesPerView: 2,
                    spaceBetween: 20
                  },
                  425: {
                    slidesPerView: 1.5,
                    spaceBetween: 20
                  },
                  320: {
                    slidesPerView: 1.2,
                    spaceBetween: 20
                  }
                }
            },
            banners: [
              {
                img: img1,
                title: 'ilustracion y diseño',
                description: '4h 20m',
                translate: '20'
              },
              {
                img: img2,
                title: 'introduccion a la direccion de fotografia',
                description: '5h 10m',
                translate: '30'
              },
              {
                img: img3,
                title: 'aprende a tocar diferentes instrumentos',
                description: '7h 25m',
                translate: '50'
              },
              {
                img: img2,
                title: 'introduccion a la direccion de fotografia',
                description: '5h 10m',
                translate: '70'
              }
            ],
            teachers: [
              {
                img: teacher3,
                title: 'Roe Zambrano',
                description: 'Sr account manager',
                translate: '20'
              },
              {
                img: teacher4,
                title: 'Arturo Aragon',
                description: 'Fotografo',
                translate: '30'
              },
              {
                img: teacher1,
                title: 'Pia Valdivia',
                description: 'Colorista',
                translate: '50'
              },
              {
                img: teacher2,
                title: 'Patricia Lombardi',
                description: 'Comic Artist',
                translate: '70'
              }
            ],
            casos: [
              {
                img: caso1,
                name: 'ana barbara t.',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea.'
              },
              {
                img: caso2,
                name: 'elizabeth betancurt r.',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea.'
              },
              {
                img: caso3,
                name: 'vanessa ale g.',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea.'
              },
              {
                img: caso4,
                name: 'carmen de los angeles',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea.'
              }
            ],
            swiperOption2: {
              spaceBetween: 20,
              slidesPerView: 5,
              slidesPerView: 1.1,
              loop: false,
              pagination: {
                  el: '.swiper2-pag',
                  type: 'fraction'
              },
              navigation: {
                  nextEl: '.swiper2-right',
                  prevEl: '.swiper2-left'
              },
              breakpoints: {
                  1024: {
                    slidesPerView: 4,
                    spaceBetween: 20
                  },
                  768: {
                    slidesPerView: 2.5,
                    spaceBetween: 20
                  },
                  640: {
                    slidesPerView: 2,
                    spaceBetween: 20
                  },
                  425: {
                    slidesPerView: 1.3,
                    spaceBetween: 20
                  },
                  320: {
                    slidesPerView: 1.1,
                    spaceBetween: 20
                  }
                }
            },
            swiperOption3: {
              spaceBetween: 20,
              slidesPerView: 5,
              slidesPerView: 1.3,
              pagination: {
                  el: '.swiper3-pag',
                  type: 'fraction'
              },
              breakpoints: {
                  1024: {
                    slidesPerView: 4,
                    spaceBetween: 20
                  },
                  768: {
                    slidesPerView: 3,
                    spaceBetween: 20
                  },
                  640: {
                    slidesPerView: 2,
                    spaceBetween: 20
                  },
                  425: {
                    slidesPerView: 1.6,
                    spaceBetween: 20
                  },
                  320: {
                    slidesPerView: 1.3,
                    spaceBetween: 20
                  }
              }
            },
            swiperOption4: {
              spaceBetween: 20,
              slidesPerView: 5,
              loop: false,
              pagination: {
                  el: '.swiper4-pag',
                  type: 'fraction'
              },
              navigation: {
                  nextEl: '.swiper4-right',
                  prevEl: '.swiper4-left'
              },
              breakpoints: {
                  1024: {
                    slidesPerView: 4,
                    spaceBetween: 20
                  },
                  768: {
                    slidesPerView: 2.5,
                    spaceBetween: 20
                  },
                  640: {
                    slidesPerView: 2,
                    spaceBetween: 20
                  },
                  425: {
                    slidesPerView: 1.3,
                    spaceBetween: 20
                  },
                  320: {
                    slidesPerView: 1.2,
                    spaceBetween: 20
                  }
              }
            },
            swiperOption5: {
                slidesPerView: 'auto',
                spaceBetween: 20,
                slidesPerView: 5,
                freeMode: true,
                loop: false,
                navigation: {
                    nextEl: '.swiper5-right',
                    prevEl: '.swiper5-left'
                },
                pagination: {
                  el: '.swiper5-pag',
                  type: 'fraction'
                },
                breakpoints: {
                  1024: {
                    slidesPerView: 4,
                    spaceBetween: 20
                  },
                  768: {
                    slidesPerView: 2,
                    spaceBetween: 20
                  },
                  640: {
                    slidesPerView: 2,
                    spaceBetween: 20
                  },
                  425: {
                    slidesPerView: 1,
                    spaceBetween: 20
                  },
                  320: {
                    slidesPerView: 1,
                    spaceBetween: 20
                  }
                }
            },
      }
  },
  mounted() {
  }
}
</script>

<style lang='scss'>

</style>
