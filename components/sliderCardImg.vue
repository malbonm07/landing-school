<template>
    <div class="card-img">
        <div class="card-img__img">
            <img :src="dataObject.img" alt="Couse" class="center" style="display:block;">
        </div>
        <div class="card-img__content">
            <p class="card-img__content--title capitalize text-medium">{{dataObject.title}}</p>
            <p class="card-img__content--description text-light">
                <span style="margin-right:7px;"><font-awesome-icon :icon="['fa', 'clock']"/></span>
                {{dataObject.description}}
            </p>
            <div class="card-img__content--hidden-text text-medium">
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
.card-img {
    height: 400px;
    transition: 2s;
    overflow: hidden;
    &--img {
        position: relative;
    }
    .center {
        transition: transform 0.3s;
    }
    &__content {
        position: absolute;
        padding: 0 1rem 0 1rem;
        bottom: 5%;
        color: white;
        transition: transform .2s;
        transform: translateY(40px);
        &--title {
            font-size: $text-h6;
            margin-bottom: 0.5rem;
        }
        &--description {
            font-size: $text-caption;
            margin-bottom: 1.5rem;
        }
        // &--hidden-text {
        //     transform: translateY(50px);
        //     transition: transform .2s;
        // }
    }
    &:hover {
        cursor: pointer;
        .center {
            transform: translateX(-30%);
            transform: scale(1.2);
        }
        .card-img__content {
            transform: translateY(0);
        }
    }
}
</style>
