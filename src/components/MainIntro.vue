<script>
import MainIntroCard from './MainIntroCard.vue';

export default {
    components: {
        MainIntroCard,
    },

    data() {
        return {
            introCards: [
                {
                    introCardImg: '/images/main-intro_images/schoolbag_alt.png',
                    introCardTitle: 'Morbi Etos',
                    introCardText: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quisquam, itaque ipsam consectetur voluptatum animi autem blanditiis.'
                },
                {
                    introCardImg: '/images/main-intro_images/stroller_alt.png',
                    introCardTitle: 'Congue Gravida',
                    introCardText: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quisquam, itaque ipsam consectetur voluptatum animi autem blanditiis.'
                },
                {
                    introCardImg: '/images/main-intro_images/globe_alt.png',
                    introCardTitle: 'Maecenas Node',
                    introCardText: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quisquam, itaque ipsam consectetur voluptatum animi autem blanditiis.'
                },
                {
                    introCardImg: '/images/main-intro_images/bell_alt.png',
                    introCardTitle: 'Praesent Morbi',
                    introCardText: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quisquam, itaque ipsam consectetur voluptatum animi autem blanditiis.'
                },
            ]
        }
    },

}
</script>

<template>
    <div class="container intro">
        <div class="column intro-content-title">
            <h1 class="intro-title">welcome to fable</h1>
            <p class="intro-text">Fable daycare, preschool, and kindergarten</p>
            <img class="divider-thumb" src="/images/main-intro_images/header_divider.png" alt="">
        </div>

        <div class="intro-content">
            <MainIntroCard :introCards="introCards" />
        </div>

    </div>
</template>

<style lang="scss" scoped>
@use '../style/generals.scss' as *;
@use '../style/partials/variables' as *;
@use '../style/partials/reset' as *;

.container.intro {
    padding: 4.5rem 0;
}

.intro-content-title {
    text-align: center;
    padding-bottom: 4rem;

    .intro-title {
        font-size: 2.5rem;
        font-weight: 400;
        margin-bottom: 1rem;
        text-transform: capitalize;
        color: $purple-color;
    }

    .intro-text {
        font-size: 1rem;
        margin-bottom: 2rem;
    }

    .divider-thumb {
        margin: 0 auto;
        width: 100px;
    }
}
</style>