<script>
import MainHero from './MainHero.vue'
import MainPreIntro from './MainPreIntro.vue';
import MainIntro from './MainIntro.vue';
import MainDescription from './MainDescription.vue';

export default {
    components: {
        MainHero,
        MainPreIntro,
        MainIntro,
        MainDescription,
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
</style>