<template>
    <div class="teacher-card-img">
        <div class="teacher-card-img__img">
            <img :src="dataObject.img" alt="teacher image" class="center">
        </div>
        <div class="teacher-card-img__content">
            <p class="teacher-card-img__content--title capitalize text-medium">{{dataObject.title}}</p>
            <p class="teacher-card-img__content--description text-regular">
                {{dataObject.description}}
            </p>
            <div class="teacher-card-img__content--hidden-text text-medium">
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
</style>
