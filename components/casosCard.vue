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
</style>