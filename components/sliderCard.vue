<template>
    <div class="sliderCard">
        <div class="sliderCard__img">
            <img :src="courseObject.img" alt="card of course" width="100%">
            <div v-if="promo" class="sliderCard__img--prom">
                <span>Nuevo</span>
            </div>
            <div class="sliderCard__img--description">
                <div class="sliderCard__img--description--bg">
                    <span><font-awesome-icon :icon="['fas', 'users']"/></span>
                    {{courseObject.students}} Alumnos
                </div>
                <div class="sliderCard__img--description--bg">
                    <span><font-awesome-icon :icon="['fa', 'clock']"/></span>
                    {{courseObject.time}}
                </div>
            </div>
        </div>
        <div class="sliderCard__content">
            <h3 class="text-subtitle1 text-center mt-1 mb-1">{{courseObject.title}}</h3>
            <p class="text-grey2 text-body1 capitalize"><span></span>{{courseObject.nivel}}</p>
            <p class="line-height3">
                <span style="color: red;" class="text-h6">S/&nbsp;</span>
                <span style="color: red;" class="text-h6">{{courseObject.precio}}</span>
                <strike style="margin-left: 10px;">S/199.99</strike>
            </p>
            <button class="sliderCard__content__btn--content text-body1 text-medium">
                <span><font-awesome-icon :icon="['fas', 'shopping-cart']"/></span>
                Añadir al carrito
            </button>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        courseObject: {
            type: Object,
            required: true,
        },
        promo: {
            type: Boolean,
            required: true
        }
    }

}
</script>

<style lang="scss">
</style>
