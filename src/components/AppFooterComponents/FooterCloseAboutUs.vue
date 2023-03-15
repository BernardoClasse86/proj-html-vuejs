<script>
export default {

}
</script>

<template>
    <div class="about-us column">
        <h3 class="about-us-title">About Us</h3>
        <p class="about-us-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia nisi cumque, repudiandae
            obcaecati debitis
            provident odio.</p>
        <img class="about-us-thumb" src="/images/footer-close_images/logo_footer.png" alt="">
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.about-us.column {
    gap: 2rem;
    color: white;

    .about-us-thumb {
        width: 190px;

    }

    .about-us-title {
        font-size: 1.25rem;
        text-transform: uppercase;
        font-weight: 400;
    }

    .about-us-title::after {
        content: "";
        display: block;
        padding: 0.5rem 2rem;
        width: 10px;
        border-bottom: 1px solid white;
    }

    .about-us-text {
        font-size: 1rem;
    }
}
</style>