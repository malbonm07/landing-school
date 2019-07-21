<template>
    <div class="carreras-tabContainer">
        <ul class="carreras-tabContainer__grid">
            <li class="carreras-tabContainer__grid-item" v-for="(carrera, i) in carreras" :key="i">
                <div class="img-container">
                    <img :src="carrera.img" alt="carrera imagen" width="80px">
                </div>
                <div class="description-container">
                    <h4 class="capitalize text-subtitle">{{carrera.title}}</h4>
                    <h6 class="text-caption text-grey2 text-light">{{carrera.cantidad}}&nbsp;&nbsp;Cursos</h6>
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
            carreras: [
                {
                img: carreraImg1,
                title: 'carrera animacion 3d',
                cantidad: '10'
                },
                {
                img: carreraImg2,
                title: 'carrera frontend',
                cantidad: '9'
                },
                {
                img: carreraImg3,
                title: 'carrera diseño digital',
                cantidad: '10'
                },
                {
                img: carreraImg4,
                title: 'carrera fotografia',
                cantidad: '12'
                },
                {
                img: carreraImg5,
                title: 'carrera marketing digital',
                cantidad: '6'
                },
                {
                img: carreraImg6,
                title: 'carrera diseño grafico',
                cantidad: '11'
                },
                {
                img: carreraImg7,
                title: 'carrera ilustracion',
                cantidad: '8'
                },
                {
                img: carreraImg8,
                title: 'carrera de retoque digital',
                cantidad: '5'
                },
                {
                img: carreraImg9,
                title: 'carrera de branding',
                cantidad: '8'
                },
            ]
        }
    }
}
</script>

<style>

</style>
