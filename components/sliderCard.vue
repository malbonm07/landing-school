<template>
    <div class="sliderCard">
        <div class="sliderCard__img">
            <img :src="courseObject.img" alt="card of course" width="100%">
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
            <button class="btn--content text-body1 text-medium">
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
        }
    }

}
</script>

<style lang="scss">
.sliderCard {
    &__img {
        @include tablet {
            width: 100%;
        }
        position: relative;
        &--description {
            position: absolute;
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 90%;
            bottom: 7%;
            left: 5%;
            color: white;
            font-size: 12px;
            font-weight: $text-regular;
            &--bg {
                background: rgba(0,0,0,0.6);
                padding: 0 9px 0 9px;
                height: 25px;
                display: flex;
                justify-content: center;
                align-items: center;
            }
            span {
                font-size: 9px;
                margin-right: 5px;
            }
        }
    }
    // @include desktop {
    //     width: 350px;
    // }
    &__content {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 5px;
    }
}
.btn--content {
    @include btn-outline(80%, #4B22F4, #4B22F4);
    color: #4B22F4;
    transition: .2s;
    margin-top: 2rem;
    span {
        margin-right: 5px;
    }
    &:hover {
        background: #4B22F4;
        color: $text-white;
    }
}
</style>
