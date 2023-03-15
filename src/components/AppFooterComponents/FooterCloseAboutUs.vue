<script>
export default {

}
</script>

<template>
    <div class="about-us column">
        <h3 class="about-us-title">About Us</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia nisi cumque, repudiandae obcaecati debitis
            provident odio.</p>
        <img class="about-us-thumb" src="/images/footer-close_images/logo_footer.png" alt="">
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.about-us.column {
    gap: 1rem;

    .about-us-thumb {
        width: 190px;
    }
}
</style>