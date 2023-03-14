<script>
export default {
    props: {
        introCards: Object,
        required: true,
    }
}

</script>

<template>
    <ul class="intro row">

        <li class="column intro-card-item" v-for="(introCard, i) in introCards" :key="i">
            <figure class="thumb-bg">
                <img class="intro-card-thumb" :src="introCard.introCardImg" alt="">
            </figure>
            <h4 class="intro-card-title">{{ introCard.introCardTitle }}</h4>
            <p class="intro-card-text">{{ introCard.introCardText }}</p>
        </li>

    </ul>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.intro.row {
    align-items: center;
    gap: 2rem;
    text-align: center;

    li:nth-child(even) figure {
        background-color: $purple-color;
    }

    li:nth-child(odd) figure {
        background-color: $orange-color;
    }

    .intro-card-item {
        gap: 1.5rem;

        .thumb-bg {
            margin: 0 auto;
            width: 180px;
            height: 180px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;

            .intro-card-thumb {
                width: 64px;
            }
        }

        .intro-card-title {
            font-size: 1.5rem;
            color: $purple-color;
            font-weight: 400;
        }
    }
}
</style>