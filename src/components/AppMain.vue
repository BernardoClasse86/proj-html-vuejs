<script>
import MainHero from './AppMainComponents/MainHero.vue'
import MainPreIntro from './AppMainComponents/MainPreIntro.vue';
import MainIntro from './AppMainComponents/MainIntro.vue';
import MainDescription from './AppMainComponents/MainDescription.vue';
import MainNumbers from './AppMainComponents/MainNumbers.vue';
import MainOurClasses from './AppMainComponents/MainOurClasses.vue';
import MainWorks from './AppMainComponents/MainWorks.vue';
import MainGallery from './AppMainComponents/MainGallery.vue';
import MainPreOutro from './AppMainComponents/MainPreOutro.vue';
import MainStaff from './AppMainComponents/MainStaff.vue';

export default {
    components: {
        MainHero,
        MainPreIntro,
        MainIntro,
        MainDescription,
        MainNumbers,
        MainOurClasses,
        MainWorks,
        MainGallery,
        MainPreOutro,
        MainStaff,
    },
}

</script>

<template>
    <main>
        <section class="hero-section">
            <MainHero />
        </section>

        <section class="preintro-section">
            <MainPreIntro />
        </section>

        <section class="intro-section">
            <MainIntro />
        </section>

        <section class="desc-section">
            <MainDescription />
        </section>

        <section class="numbers-section">
            <MainNumbers />
        </section>

        <section class="ourclass-section">
            <MainOurClasses />
        </section>

        <section class="work-section">
            <MainWorks />
        </section>

        <section class="gallery-container">
            <MainGallery />
        </section>

        <section class="preintro-section">
            <MainPreOutro />
        </section>

        <section class="staff-section">
            <MainStaff />
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use '../style/generals.scss' as *;
@use '../style/partials/variables' as *;
@use '../style/partials/reset' as *;

.hero-section {
    background-position: center;
    background-size: contain;
    background-image: url(/images/hero/slider_slide3_background.png);
}

.preintro-section {
    background-position: center;
    background-size: cover;
    background-image: url(/images/intro&gallery-bg/pattern.png);
}

.desc-section {
    background-color: $grey-bg;
}

.numbers-section {
    background-position: center;
    background-size: cover;
    background-image: url(/images/main-numb_images/parallax_01.jpg);
}

.work-section {
    background-color: $grey-bg;
}
</style>