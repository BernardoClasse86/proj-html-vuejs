<script>
import FooterClose from './AppFooterComponents/FooterClose.vue';
import FooterLinks from './AppFooterComponents/FooterLinks.vue';

export default {
    components: {
        FooterClose,
        FooterLinks
    }
}
</script>

<template>
    <footer>
        <section class="main-footer">
            <FooterClose />
        </section>

        <section>
            <FooterLinks />
        </section>
    </footer>
</template>

<style lang="scss" scoped>
@use '../style/generals.scss' as *;
@use '../style/partials/variables' as *;
@use '../style/partials/reset' as *;

.main-footer {
    background-image: url(/images/footer-close_images/pattern.png);
}
</style>