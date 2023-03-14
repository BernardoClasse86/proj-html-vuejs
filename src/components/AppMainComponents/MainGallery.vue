<script>
export default {
    data() {
        return {
            galleryImgs: [
                '/images/main-gallery_images/gallery_01.jpg',
                '/images/main-gallery_images/gallery_02.jpg',
                '/images/main-gallery_images/gallery_03.jpg',
                '/images/main-gallery_images/gallery_04.jpg',
            ]
        }
    }
}
</script>

<template>
    <div class="row">
        <img class="gallery-thumb" v-for="image in galleryImgs" :src="image" alt="">
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.gallery-thumb {
    width: 25%;
}
</style>