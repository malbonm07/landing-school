<template>
    <div class="slider-card-img">
        <div class="slider-card-img__img">
            <img :src="dataObject.img" alt="Couse" class="center" style="display:block;">
        </div>
        <div class="slider-card-img__content">
            <p class="slider-card-img__content--title capitalize text-medium">{{dataObject.title}}</p>
            <p class="slider-card-img__content--description text-light">
                <span style="margin-right:7px;"><font-awesome-icon :icon="['fa', 'clock']"/></span>
                {{dataObject.description}}
            </p>
            <div class="slider-card-img__content--hidden-text text-medium">
                <a>Ver Detalles del Curso</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        dataObject: {
            type: Object,
            required: true
        }
    }
}
</script>

<style lang="scss">
</style>
