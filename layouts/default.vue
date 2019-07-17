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
    <footer>
      <div>
        <div>CATEGORÍAS<span><font-awesome-icon :icon="['fas', 'chevron-right']"/></span></div>
        <div>
          <a>Cursos de Ilustración y Dibujo</a>
          <a>Cursos de Diseño</a>
          <a>Cursos de Animación & 3D</a>
          <a>Cursos de Web</a>
          <a>Cursos de Fotografía</a>
          <a>Cursos de Marketing Digital</a>
        </div>
        <div>SOFTWARE<span><font-awesome-icon :icon="['fas', 'chevron-right']"/></span></div>
        <div>
          <a>Cursos de Adobe Animate CC</a>
          <a>Cursos de Audition</a>
          <a>Cursos de Photoshop Lightroom</a>
          <a>Cursos de Premiere</a>
          <a>Cursos de Illustrator</a>
          <a>Cursos de Adobe Photoshop</a>
        </div>
        <div>CONÓCENOS<span><font-awesome-icon :icon="['fas', 'chevron-right']"/></span></div>
        <div>
          <a>estamos contratando!</a>
          <a>sobre crehana</a>
          <a>terminos y condiciones</a>
          <a>politicas de privacidad</a>
          <a>politica de cookies</a>
        </div>
        <div>COMUNIDAD<span><font-awesome-icon :icon="['fas', 'chevron-right']"/></span></div>
        <div>
          <a>becas</a>
          <a>historias</a>
          <a>tarjetas de regalo</a>
          <a>proyectos</a>
          <a>recursos</a>
          <a>blog</a>
        </div>
      </div>
      <div>
        <div><font-awesome-icon :icon="['fab', 'facebook-f']"/></div>
        <div><font-awesome-icon :icon="['fab', 'twitter']"/></div>
        <div><font-awesome-icon :icon="['fab', 'instagram']"/></div>
        <div><font-awesome-icon :icon="['fab', 'linkedin']"/></div>
        <div><font-awesome-icon :icon="['fab', 'youtube']"/></div>
      </div>
      <div>
        <h5>DESCARGA NUESTRA APP EN:</h5>
        <button><span><font-awesome-icon :icon="['fab', 'google-play']"/></span>Google play</button>
        <button><span><font-awesome-icon :icon="['fab', 'apple']"/></span>App store</button>
        <button><span><font-awesome-icon :icon="['fas', 'comments-dollar']"/></span>App store</button>
      </div>
      <div>
        <div>
          <h6>Copyright&#169; Crehana 2019</h6>
          <h6>Todos los derechos reservados</h6>
        </div>
      </div>
    </footer>
  </div>
</template>
<!-- <p>Icons</p>
<font-awesome-icon :icon="['fab', 'facebook']"/>
<font-awesome-icon :icon="['fab', 'github']"/>
<font-awesome-icon :icon="['fab', 'facebook']"/>
<font-awesome-icon :icon="['fas', 'shopping-cart']"/> -->
<style lang="scss">
*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
</style>
