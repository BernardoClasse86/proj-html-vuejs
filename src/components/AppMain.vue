<script>
import MainHero from './MainHero.vue'

export default {
    components: {
        MainHero,
    }
}

</script>

<template>
    <section class="hero-section">
        <MainHero />
    </section>
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
</style>