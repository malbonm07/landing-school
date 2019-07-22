<template>
    <div class="certificaciones-tabContainer">
        <ul class="certificaciones-tabContainer__grid">
            <li class="certificaciones-tabContainer__grid-item" v-for="(certificacion, i) in certificaciones" :key="i">
                <div class="img-container">
                    <img :src="certificacion.img" alt="carrera imagen" width="80px">
                </div>
                <div class="description-container">
                    <h4 class="capitalize text-subtitle">{{certificacion.title}}</h4>
                    <h6 class="text-caption text-grey2 text-light">{{certificacion.cantidad}}&nbsp;&nbsp;Cursos</h6>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>

import carreraImg1 from '~/assets/imagens/carreras-tab/img1.png'
import carreraImg2 from '~/assets/imagens/carreras-tab/img2.png'
import carreraImg3 from '~/assets/imagens/carreras-tab/img3.png'
import carreraImg4 from '~/assets/imagens/carreras-tab/img4.png'
import carreraImg5 from '~/assets/imagens/carreras-tab/img5.png'
import carreraImg6 from '~/assets/imagens/carreras-tab/img6.png'
import carreraImg7 from '~/assets/imagens/carreras-tab/img7.png'
import carreraImg8 from '~/assets/imagens/carreras-tab/img8.png'
import carreraImg9 from '~/assets/imagens/carreras-tab/img9.png'

export default {
    data() {
        return {
            certificaciones: [
                {
                img: carreraImg4,
                title: 'certificate enimacion 3d',
                cantidad: '10'
                },
                {
                img: carreraImg5,
                title: 'certificate enontend',
                cantidad: '9'
                },
                {
                img: carreraImg7,
                title: 'certificate enseño digital',
                cantidad: '10'
                },
                {
                img: carreraImg1,
                title: 'certificate entografia',
                cantidad: '12'
                },
                {
                img: carreraImg2,
                title: 'certificate enrketing digital',
                cantidad: '6'
                },
                {
                img: carreraImg9,
                title: 'certificate enseño grafico',
                cantidad: '11'
                },
                {
                img: carreraImg3,
                title: 'certificate enustracion',
                cantidad: '8'
                },
                {
                img: carreraImg8,
                title: 'certificate en retoque digital',
                cantidad: '5'
                },
                {
                img: carreraImg6,
                title: 'certificate en branding',
                cantidad: '8'
                },
            ]
        }
    }
}
</script>

<style lang="scss">
</style>
