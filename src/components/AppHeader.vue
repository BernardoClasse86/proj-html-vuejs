<script>
import HeaderNav from './HeaderNav.vue'
import HeaderLogo from './HeaderLogo.vue'

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
                    navText: 'home',
                },
                {
                    navImg: '/images/links-images/document.png',
                    navText: 'pages',
                },
                {
                    navImg: '/images/links-images/printer.png',
                    navText: 'blog',
                },
                {
                    navImg: '/images/links-images/cart.png',
                    navText: 'shop',
                },
                {
                    navImg: '/images/links-images/lab.png',
                    navText: 'shortcodes',
                },
                {
                    navImg: '/images/links-images/chat.png',
                    navText: 'support',
                },
                {
                    navImg: '/images/links-images/envelope.png',
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

