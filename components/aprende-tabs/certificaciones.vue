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

export default {
    data() {
        return {
            certificaciones: [
                {
                img: 'https://i.imgur.com/ABVriPO.png',
                title: 'certificate enimacion 3d',
                cantidad: '10'
                },
                {
                img: 'https://i.imgur.com/7GaxfZs.png',
                title: 'certificate enontend',
                cantidad: '9'
                },
                {
                img: 'https://i.imgur.com/G9XI2vO.png',
                title: 'certificate enseño digital',
                cantidad: '10'
                },
                {
                img: 'https://i.imgur.com/ZOwppQH.png',
                title: 'certificate entografia',
                cantidad: '12'
                },
                {
                img: 'https://i.imgur.com/F54s31t.png',
                title: 'certificate enrketing digital',
                cantidad: '6'
                },
                {
                img: 'https://i.imgur.com/7GaxfZs.png',
                title: 'certificate enseño grafico',
                cantidad: '11'
                },
                {
                img: 'https://i.imgur.com/G9XI2vO.png',
                title: 'certificate enustracion',
                cantidad: '8'
                },
                {
                img: 'https://i.imgur.com/F54s31t.png',
                title: 'certificate en retoque digital',
                cantidad: '5'
                },
                {
                img: 'https://i.imgur.com/ZOwppQH.png',
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
