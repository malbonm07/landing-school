<template>
    <div class="card-img">
        <div class="card-img__img">
            <img :src="dataObject.img" alt="Couse" class="center">
        </div>
        <div class="card-img__content">
            <p class="card-img__content--title capitalize text-medium">{{dataObject.title}}</p>
            <p class="card-img__content--description text-regular">
                {{dataObject.description}}
            </p>
            <div class="card-img__content--hidden-text text-medium">
                <a>Ver Cursos</a>
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
        transform: translateX(-15%);
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
            font-size: $text-subtitle1;
            margin-bottom: 1.5rem;
        }
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
