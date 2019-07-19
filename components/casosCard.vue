<template>
    <div class="casoCard">
        <div class="casoCard__img">
            <img :src="casoObject.img" alt="Caso de exito" width="100%">
        </div>
        <div class="casoCard__content">
            <div class="text-left" style="color: #5CCBD1;">
                <font-awesome-icon class="text-left text-h5" :icon="['fa', 'quote-left']"/>
            </div>
            <div>
                <p class="text-body1 mt-1 mb-1 line-height1 text-grey2 text-light">{{casoObject.text}}</p>
                <h5 class="capitalize text-grey3 text-medium relativ">
                    <span class="guion"></span>
                    <span style="margin-left:20px;">{{casoObject.name}}</span>
                </h5>
            </div>
            <!-- <h3 class="text-subtitle1 text-center mt-1 mb-1">{{courseObject.title}}</h3>
            <p class="text-grey2 text-body1 capitalize"><span></span>{{courseObject.nivel}}</p>
            <p class="line-height3">
                <span style="color: red;" class="text-h6">S/&nbsp;</span>
                <span style="color: red;" class="text-h6">{{courseObject.precio}}</span>
                <strike style="margin-left: 10px;">S/199.99</strike>
            </p>
            <button class="btn--content text-body1 text-medium">
                <span><font-awesome-icon :icon="['fas', 'shopping-cart']"/></span>
                Añadir al carrito
            </button> -->
        </div>
    </div>
</template>

<script>
export default {
    props: {
        casoObject: {
            type: Object,
            required: true,
        }
    }

}
</script>

<style lang="scss">
.casoCard {
    &__img {
        position: relative;
    }
    &__content {
        transform: translateY(-25px);
        background: #F5F5F5;
        margin: 0 15px 0 15px;
        padding: 15px;
    }
}
.guion {
    display: block;
    position: absolute;
    &:before {
        content: "";
        display: block;
        background: $text-grey3;
        width: 15px;
        height: 1px;
        position: absoulte;
        transform: translateY(8px)
    }
}
</style>