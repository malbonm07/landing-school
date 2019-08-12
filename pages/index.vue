<template>
  <div class="container">


    <!--------------------------- HEADER ------------------------------>
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
    <!--------------------------- END HEADER ------------------------------>
    

    <!--------------------------- SUB-HEADER ------------------------------>
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
    <!--------------------------- END SUB-HEADER ------------------------------>


    <!--------------------------- CURSOS SECTION ------------------------------>
    <section class="cursos-section">
      <div class="text-h4 text-title mt-4 mb-4 text-center"><h2>¿Qué deseas aprender hoy?</h2></div>
      <div class="cursos-swiper-responsive">
        <div v-swiper:mySwiper="swiperOption" class="swiper-container">
            <ul class="swiper-wrapper">
                <li class="swiper-slide" v-for="(course, i) in courses" :key="i">
                  <sliderCard :courseObject="course" :promo="course.promo">
                  </sliderCard>
                </li>
            </ul>
            <div class="swiper-pagination__content">
              <button
                  class="swiper1-button swiper-left"
              >
                  <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-left']"/>
              </button>
              <div class="swiper-pag" slot="pagination"></div>
              <button
                  class="swiper1-button swiper-right"
              >
                  <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-right']"/>
              </button>
            </div>
        </div>
      </div>
      <div class="cursos-grid pl-2 pr-2">
        <div class="cursos-grid__item" v-for="(course, i) in courses" :key="i">
            <sliderCard :courseObject="course" :promo="course.promo">
            </sliderCard>
        </div>
      </div>
      <div class="text-medium text-subtitle1 mt-4" style="text-align:center;color: #62D4DD;">
        <a style="cursor: pointer;">Explora todo Aquí</a>
      </div>
    </section>
    <!--------------------------- END CURSOS SECTION ------------------------------>


    <hr class="separator-fluid">


    <!--------------------------- STATS SECTION ------------------------------>
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
    <!--------------------------- END STATS SECTION ------------------------------>


    <!--------------------------- LANZAMIENTOS SECTION ------------------------------>
    <section class="lanza-section mt-4 relative">
      <div class="lanza-section__title">
        <div class="lanza-section__title-flex line-height3">
          <p class="text-caption text-regular pt-2">ENTÉRATE DE LO ÚLTIMO</p>
          <h4 class="text-h4 text-title pb-2">Lanzamientos recientes</h4>
          <button class="lanza-btn text-body1 text-white text-medium">
            Click Aquí
          </button>
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
                  class="swiper2-button swiper2-left"
              >
                  <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-left']"/>
              </button>
              <div class="swiper2-pag" slot="pagination"></div>
              <button
                  class="swiper2-button swiper2-right"
              >
                  <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-right']"/>
              </button>
            </div>
        </div>
      </div>
    </section>
    <div class="spacer"></div>
    <!--------------------------- END LANZAMIENTOS SECTION ------------------------------>


    <!--------------------------- LANZAMIENTOS INFO ------------------------------>
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
                    <div class="swiper-info__card">
                      <h5 class="text-subtitle1 mb-1">Carreras</h5>
                      <p class="text-body1 text-light text-left line-height1 mb-2">Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                      sed do eiusmod tempor incididunt ut labore et dolore.</p>
                      <a class="text-body1" style="cursor: pointer;">
                        Explorar
                        <span class="text-body1 ml-1"><font-awesome-icon class="chevronIcon" :icon="['fas', 'arrow-right']"/>
                        </span>
                      </a>
                    </div>
                  </li>
                  <li class="swiper-slide">
                    <div class="swiper-info__card">
                      <h5 class="text-subtitle1 mb-1">Certificaciones</h5>
                      <p class="text-body1 text-light text-left line-height1 mb-2">Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                      sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim.</p>
                      <a class="text-body1" style="cursor: pointer;">
                        Explorar
                        <span class="text-body1 ml-1"><font-awesome-icon class="chevronIcon" :icon="['fas', 'arrow-right']"/>
                        </span>
                      </a>
                    </div>
                  </li>
                  <li class="swiper-slide">
                    <div class="swiper-info__card">
                      <h5 class="text-subtitle1 mb-1">Cursos</h5>
                      <p class="text-body1 text-light text-left line-height1 mb-2">Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                      sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco</p>
                      <a class="text-body1" style="cursor: pointer;">
                        Explorar
                        <span class="text-body1 ml-1"><font-awesome-icon class="chevronIcon" :icon="['fas', 'arrow-right']"/>
                        </span>
                      </a>
                    </div>
                  </li>
              </ul>
          </div>   
        </div>
      </div>
      <div class="lanza-desktop">
        <div class="lanza-desktop__text-container pl-2">
          <p class="text-grey1 text-caption mb-1">ELIGE TU PROPIO CAMINO</p>
          <button class="btn-info text-medium text-grey1" 
          @click="infoBanner=infoBanners[0]"
          :class="{'active-btn' : infoBanner === infoBanners[0]}"
          >
          Carreras
          </button>
          <button class="btn-info text-medium text-grey1" 
          @click="infoBanner=infoBanners[1]"
          :class="{'active-btn' : infoBanner === infoBanners[1]}"
          >
          Certificaciones
          </button>
          <button class="btn-info text-medium text-grey1" 
          @click="infoBanner=infoBanners[2]"
          :class="{'active-btn' : infoBanner === infoBanners[2]}"
          >
          Cursos
          </button>
        </div>
        <div class="lanza-desktop__board">
          <div class="lanza-desktop__board-box pt-1 pb-1">
            <p class="text-h6 pl-2 pr-5 mb-1 text-light">{{infoBanner.description}}</p>
            <a class="text-subtitle1 text-medium ml-2 mr-5">
              Explorar Cursos<span style="padding-left: 8px;"><font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-right']"/></span>
              </a>
            <div class="lanza-desktop__board-box-img">
              <img :src="infoBanner.img" alt="Imagen de referencia" width="100%">
            </div>
          </div>
        </div>
      </div>
    </section>
    <!--------------------------- END LANZAMIENTOS INFO ------------------------------>


    <!--------------------------- EXP-SECTION ------------------------------>
    <section class="exp-section mt-4">
      <div>
        <div class="exp-section__title">
          <span class="subtitle-desktop text-caption pl-4 line-height3 text-grey1">NUESTROS PROFESORES</span>
          <h4 class="text-h4 text-title text-center pl-1 pr-1 mb-2">Los mejores expertos de Latinoamerica</h4>
          <p class="text-subtitle1 text-center pl-1 pr-1 mb-3">Los mejores expertos de la industria que guiaran tu aprendizaje te comunicarán lo mejor de sus experiencias.</p>
        </div>
        <div class="exp-section__swiper">
          <div v-swiper:mySwiper4="swiperOption4" class="swiper-container">
              <ul class="swiper-wrapper">
                  <li class="swiper-slide" v-for="(teacher, index) in teachers" :key="index">
                    <teacherCard :dataObject="teacher" :style="`transform: translateY(${teacher.translate}px)`">
                    </teacherCard>
                  </li>
              </ul>
              <div class="swiper-pagination__content exp-section__swiper4-btn-desktop">
                <button
                    class="swiper4-button swiper4-left"
                >
                    <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-left']"/>
                </button>
                <div class="swiper4-pag" slot="pagination"></div>
                <button
                    class="swiper4-button swiper4-right"
                >
                    <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-right']"/>
                </button>
              </div>
          </div>
        </div>
      </div>
    </section>
    <!--------------------------- END EXP-SECTION ------------------------------>


    <!--------------------------- CASOS SECTION ------------------------------>
    <section class="casos-section mt-4 mb-4">
      <div class="casos-section__title">
        <h4 class="text-h4 text-title pl-1 pr-1 mb-2">Nuestros casos de éxito</h4>
      </div>
      <div class="casos-section__swiper">
        <div v-swiper:mySwipe5="swiperOption5" class="swiper-container">
            <ul class="swiper-wrapper">
                <li class="swiper-slide" v-for="(caso, i) in casos" :key="i">
                  <casosCard :casoObject="caso">
                  </casosCard>
                </li>
            </ul>
            <div class="swiper-pagination__content casos-btn-box">
              <button
                  class="swiper5-button swiper5-left"
              >
                  <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-left']"/>
              </button>
              <div class="swiper5-pag" slot="pagination"></div>
              <button
                  class="swiper5-button swiper5-right"
              >
                  <font-awesome-icon class="chevronIcon" :icon="['fas', 'chevron-right']"/>
              </button>
            </div>
        </div>
      </div>
      <!-- <div class="casos-grid">
        <div class="casos-grid__item" v-for="(caso, i) in casos" :key="i">
            <casosCard :casoObject="caso">
            </casosCard>    
        </div>
      </div> -->
    </section>
    <!--------------------------- END CASOS SECTION ------------------------------>


    <!--------------------------- CALL SECTION ------------------------------>
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
        <h4 class="text-h4 text-title mb-2">Potencia el talento de tu equipo con nuestros planes.</h4>
        <button class="call-section__empresas--btn text-body1 text-white text-medium text-space4">
          Entérate más
        </button>
      </div>
    </section>
    <!--------------------------- END CALL SECTION ------------------------------>


  </div>
</template>

<script>
import sliderCard from '~/components/sliderCard.vue';
import sliderCardImg from '~/components/sliderCardImg.vue';
import teacherCard from '~/components/teacherCard.vue';
import casosCard from '~/components/casosCard.vue';

export default {
  components: {
    sliderCard,
    sliderCardImg,
    teacherCard,
    casosCard
  },
  data () {
      return {
            infoBanner: {
                img: 'https://i.imgur.com/Jwx6uPc.jpg',
                description: 'Estudia con nosotros y asegura el éxito, haz la diferencia con las habilidades que aprenderás. Te estamos esperando!'
              },
            courses: [
              {
                img: 'https://i.imgur.com/p00nsl4.jpg',
                title: "Aprender a dibujar al estilo cómic",
                nivel: "Nivel introductorio",
                precio: 160.99,
                link: "null",
                students: "156",
                time: "2h 21m",
                promo: true
              },
              {
                img: 'https://i.imgur.com/EdBsGwi.jpg',
                title: "Aprender a dibujar al estilo cómic",
                nivel: "Nivel introductorio",
                precio: 170.99,
                link: "null",
                students: "176",
                time: "2h 21m",
                promo: true
              },
              {
                img: 'https://i.imgur.com/ZSzacVN.jpg',
                title: "Aprender a dibujar al estilo cómic",
                nivel: "Nivel introductorio",
                precio: 29.99,
                link: "null",
                students: "142",
                time: "2h 21m",
                promo: false
              },
              {
                img: 'https://i.imgur.com/VA0gLxg.jpg',
                title: "Aprender a dibujar al estilo cómic",
                nivel: "Nivel introductorio",
                precio: 49.99,
                link: "null",
                students: "132",
                time: "2h 21m",
                promo: false
              },
              {
                img: 'https://i.imgur.com/p00nsl4.jpg',
                title: "Aprender a dibujar al estilo cómic",
                nivel: "Nivel introductorio",
                precio: 49.99,
                link: "null",
                students: "176",
                time: "2h 21m",
                promo: false
              },
              {
                img: 'https://i.imgur.com/EdBsGwi.jpg',
                title: "Aprender a dibujar al estilo cómic",
                nivel: "Nivel introductorio",
                precio: 49.99,
                link: "null",
                students: "116",
                time: "2h 21m",
                promo: false
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
                img: 'https://i.imgur.com/xFOzt6j.jpg?1',
                title: 'ilustracion y diseño',
                description: '4h 20m',
                translate: '20'
              },
              {
                img: 'https://i.imgur.com/qPuNoXt.jpg?3',
                title: 'introduccion a la direccion de fotografia',
                description: '5h 10m',
                translate: '30'
              },
              {
                img: 'https://i.imgur.com/xZdIgku.jpg',
                title: 'aprende a tocar diferentes instrumentos',
                description: '7h 25m',
                translate: '50'
              },
              {
                img: 'https://i.imgur.com/xFOzt6j.jpg?1',
                title: 'introduccion a la direccion de fotografia',
                description: '5h 10m',
                translate: '70'
              }
            ],
            teachers: [
              {
                img: 'https://i.imgur.com/fAofY8n.jpg',
                title: 'Roe Zambrano',
                description: 'Sr account manager',
                translate: '20'
              },
              {
                img: 'https://i.imgur.com/iS84N3S.jpg?1',
                title: 'Arturo Aragon',
                description: 'Fotografo',
                translate: '30'
              },
              {
                img: 'https://i.imgur.com/Kl4ness.jpg?1',
                title: 'Pia Valdivia',
                description: 'Colorista',
                translate: '50'
              },
              {
                img: 'https://i.imgur.com/bHdX3AP.jpg?1',
                title: 'Patricia Lombardi',
                description: 'Comic Artist',
                translate: '70'
              },
              {
                img: 'https://i.imgur.com/Kl4ness.jpg?1',
                title: 'Roe Zambrano',
                description: 'Sr account manager',
                translate: '20'
              },
              {
                img: 'https://i.imgur.com/iS84N3S.jpg?1',
                title: 'Arturo Aragon',
                description: 'Fotografo',
                translate: '30'
              },
              {
                img: 'https://i.imgur.com/Kl4ness.jpg?1',
                title: 'Pia Valdivia',
                description: 'Colorista',
                translate: '50'
              },
              {
                img: 'https://i.imgur.com/fAofY8n.jpg',
                title: 'Patricia Lombardi',
                description: 'Comic Artist',
                translate: '70'
              }
            ],
            infoBanners: [
              {
                img: 'https://i.imgur.com/Jwx6uPc.jpg',
                description: 'Estudia con nosotros y asegura el éxito, haz la diferencia con las habilidades que aprenderás. Te estamos esperando!'
              },
              {
                img: 'https://i.imgur.com/JgCIefz.jpg',
                description: 'Contamos con packs de cursos complementarios que te ayudarán a profundizar y especializarte en lo que más te apasiona.'
              },
              {
                img: 'https://i.imgur.com/94u0iyG.jpg',
                description: 'Contamos con cursos en diversas categorías y niveles para que aprendas desde cero o complementes tus habilidades junto a expertos de la industria.'
              },
            ],
            casos: [
              {
                img: 'https://i.imgur.com/rHywXOR.jpg',
                name: 'ana barbara t.',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea.'
              },
              {
                img: 'https://i.imgur.com/YGQvo5Q.jpg',
                name: 'elizabeth betancurt r.',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea.'
              },
              {
                img: 'https://i.imgur.com/645F3GL.jpg',
                name: 'vanessa ale g.',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea.'
              },
              {
                img: 'https://i.imgur.com/YY7umbf.jpg',
                name: 'carmen de los angeles',
                text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea.'
              }
            ],
            swiperOption2: {
              spaceBetween: 20,
              slidesPerView: 2.2,
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
                    slidesPerView: 2.3,
                    spaceBetween: 20,
                    navigation: {
                        nextEl: '.swip2-right',
                        prevEl: '.swip2-left'
                    },
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
              slidesPerView: 3,
              pagination: {
                  el: '.swiper3-pag',
                  type: 'fraction'
              },
              breakpoints: {
                  1024: {
                    slidesPerView: 3,
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
                    slidesPerView: 1.2,
                    spaceBetween: 20
                  }
              }
            },
            swiperOption4: {
              spaceBetween: 40,
              slidesPerView: 4,
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
                spaceBetween: 40,
                slidesPerView: 2,
                centeredSlides: false,
                freeMode: false,
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
                    slidesPerView: 2,
                    spaceBetween: 40
                  },
                  768: {
                    slidesPerView: 2,
                    spaceBetween: 20
                  },
                  640: {
                    slidesPerView: 1,
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
