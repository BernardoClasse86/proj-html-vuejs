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
import MainReview from './AppMainComponents/MainReview.vue';
import MainNews from './AppMainComponents/MainNews.vue';
import MainContact from './AppMainComponents/MainContact.vue';

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
        MainReview,
        MainNews,
        MainContact,
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

        <section>
            <MainIntro />
        </section>

        <section class="desc-section">
            <MainDescription />
        </section>

        <section class="numbers-section">
            <MainNumbers />
        </section>

        <section>
            <MainOurClasses />
        </section>

        <section class="work-section">
            <MainWorks />
        </section>

        <section>
            <MainGallery />
        </section>

        <section class="preintro-section">
            <MainPreOutro />
        </section>

        <section>
            <MainStaff />
        </section>

        <section class="reveiw-section">
            <MainReview />
        </section>

        <section>
            <MainNews />
        </section>

        <section>
            <iframe
                src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d1400.8393078831377!2d-75.67537263292701!3d45.395653500309!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4cce05eea825aaab%3A0x5d1d325426cfc369!2sFable%20Care%20Center!5e0!3m2!1sen!2sit!4v1678815142984!5m2!1sen!2sit"
                width="100%" height="400" style="border:0;" allowfullscreen="" loading="lazy"
                referrerpolicy="no-referrer-when-downgrade">
            </iframe>
        </section>

        <section>
            <MainContact />
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

.reveiw-section {
    background-position: center;
    background-size: cover;
    background-image: url(/images/main-reviews_images/parallax_02.jpg);
}
</style>