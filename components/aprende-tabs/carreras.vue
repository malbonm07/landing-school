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

export default {
    data() {
        return {
            carreras: [
                {
                img: 'https://i.imgur.com/7GaxfZs.png',
                title: 'carrera animacion 3d',
                cantidad: '10'
                },
                {
                img: 'https://i.imgur.com/G9XI2vO.png',
                title: 'carrera frontend',
                cantidad: '9'
                },
                {
                img: 'https://i.imgur.com/ZOwppQH.png',
                title: 'carrera diseño digital',
                cantidad: '10'
                },
                {
                img: 'https://i.imgur.com/F54s31t.png',
                title: 'carrera fotografia',
                cantidad: '12'
                },
                {
                img: 'https://i.imgur.com/ABVriPO.png',
                title: 'carrera marketing digital',
                cantidad: '6'
                },
                {
                img: 'https://i.imgur.com/88CtEhX.png',
                title: 'carrera diseño grafico',
                cantidad: '11'
                },
                {
                img: 'https://i.imgur.com/2dyntA3.png',
                title: 'carrera ilustracion',
                cantidad: '8'
                },
                {
                img: 'https://i.imgur.com/VbHY3Og.png',
                title: 'carrera de retoque digital',
                cantidad: '5'
                },
                {
                img: 'https://i.imgur.com/X39ga4h.png',
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
