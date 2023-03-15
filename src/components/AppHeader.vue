<script>
import HeaderNav from './AppHeaderComponents/HeaderNav.vue'
import HeaderLogo from './AppHeaderComponents/HeaderLogo.vue'

export default {
    components: {
        HeaderNav,
        HeaderLogo
    },

    data() {
        return {
            navMenu: [
                {
                    navImg: '/images/links-images/home.png',
                    navAltImg: '/images/links-images/home-2.png',
                    navText: 'home',
                },
                {
                    navImg: '/images/links-images/document.png',
                    navAltImg: '/images/links-images/document-2.png',
                    navText: 'pages',
                },
                {
                    navImg: '/images/links-images/printer.png',
                    navAltImg: '/images/links-images/printer-2.png',
                    navText: 'blog',
                },
                {
                    navImg: '/images/links-images/cart.png',
                    navAltImg: '/images/links-images/cart-2.png',
                    navText: 'shop',
                },
                {
                    navImg: '/images/links-images/lab.png',
                    navAltImg: '/images/links-images/lab-2.png',
                    navText: 'shortcodes',
                },
                {
                    navImg: '/images/links-images/chat.png',
                    navAltImg: '/images/links-images/chat-2.png',
                    navText: 'support',
                },
                {
                    navImg: '/images/links-images/envelope.png',
                    navAltImg: '/images/links-images/envelope-2.png',
                    navText: 'contact',
                }
            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="container row">
            <HeaderLogo />

            <HeaderNav :navItems="navMenu" />
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../style/generals.scss' as *;
@use '../style/partials/variables' as *;
@use '../style/partials/reset' as *;

.container.row {
    // padding: 1rem 0;
    align-items: center;
    justify-content: space-between;
}
</style>

