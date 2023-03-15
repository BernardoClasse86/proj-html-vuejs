<script>
export default {
    data() {
        return {
            links: [
                '/images/footer-links_images/behance.png',
                '/images/footer-links_images/dribbble.png',
                '/images/footer-links_images/envato.png',
                '/images/footer-links_images/facebook.png',
                '/images/footer-links_images/twitter.png'
            ]
        }
    }
}
</script>

<template>
    <div class="container">
        <ul class="links row">
            <li v-for="link in links">
                <img class="btn btn-orange" :src="link" alt="">
            </li>
        </ul>

        <div class="product row">
            <p>&copy; Fable - Children Kindergarten WordPress Theme</p>
            <p>by</p>
            <p>QuanticaLabs</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.container {
    padding: 2rem 0;

    .links.row {
        align-items: center;
        justify-content: center;
        gap: 0.25rem;
        margin-bottom: 2rem;

        .btn {
            padding: 0.5rem;
        }

        .btn:hover {
            background-color: $purple-color;
        }
    }

    .product.row {
        justify-content: center;
        align-items: center;
        gap: 0.25rem;
        font-size: 0.875rem;
        color: rgba(0, 0, 0, 0.5);
    }
}
</style>