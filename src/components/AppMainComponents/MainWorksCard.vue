<script>
export default {
    props: {
        workCards: Object,
        required: true
    }
}

</script>

<template>
    <ul class="row">

        <li class="work-card-item column" v-for="(workCard, i) in workCards" :key="i">
            <figure class="work-card-thumb-style">
                <img class="work-card-thumb" :src="workCard.workCardImg" alt="">
            </figure>
            <h4 class="work-card-title">{{ workCard.workCardTitle }}</h4>
            <p class="work-card-text">{{ workCard.workCardText }}</p>
        </li>

    </ul>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.row {
    text-align: center;
    align-items: center;
    flex-wrap: wrap;
    gap: 48px;

    .work-card-item.column {
        flex-basis: calc(100% * (6/12) - 24px);
        gap: 1.5rem;

        .work-card-thumb-style {
            width: 80px;
            height: 80px;
            background-color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto;

            .work-card-thumb {
                width: 32px;
            }
        }

        .work-card-title {
            font-size: 1.5rem;
            font-weight: 400;
            color: $purple-color;
        }
    }
}
</style>