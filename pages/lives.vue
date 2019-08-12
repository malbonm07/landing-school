<template>
    <div class="lives-container">
        <div class="lives-container__hashtag">
            <h2 class="text-h4 mb-1">#LOREMPAGLORE</h2>
            <p class="text-subtitle1">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna.</p>
        </div>
        <div class="lives-container__links">
            <span class="link1" style="color:#5CCBD0;">Próximos</span>
            <span class="link2">Anteriores</span>
        </div>
        <div class="lives-container__banner">
            <div class="lives-img">
                <img :src="imagen" alt="imagen de lives" width="100%">
            </div>
            <div class="lives-description">
                <h4 class="text-h6 mb-1 mt-1">¿Como expresar mis ideas y no sufrir en el intento?</h4>
                <h6 class="text-caption text-grey2 mt-1 mb-1">02 de Noviembre 2:00pm</h6>
                <p class="text-subtitle1">Por Andres Molina Gio, ilustración y Diseño gráfico</p>
                <div class="insc-box mt-2">
                    <a class="text-subtitle1 mr-1" style="color:#5CCBD0;">Más info</a>
                    <button class="text-subtitle1 btn-lives">
                        ¡Inscríbete ahora!
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            imagen: 'https://i.imgur.com/ZSzacVN.jpg',
        }
    }
}
</script>

<style>

</style>
