<script>
import MainWorksCard from './MainWorksCard.vue'
import MainWorksList from './MainWorksList.vue';

export default {
    components: {
        MainWorksCard,
        MainWorksList,
    },

    data() {
        return {
            workGoals: [
                {
                    workCheck: '/images/main-work_images/style_1.png',
                    workGoal: 'Comprehensive reporting on individual achievement'
                },
                {
                    workCheck: '/images/main-work_images/style_1.png',
                    workGoal: 'Educational field trips and school presentations'
                },
                {
                    workCheck: '/images/main-work_images/style_1.png',
                    workGoal: 'Individual attention in a small-class setting'
                },
                {
                    workCheck: '/images/main-work_images/style_1.png',
                    workGoal: 'Learning program with after-school care'
                },
                {
                    workCheck: '/images/main-work_images/style_1.png',
                    workGoal: 'Opportunities to carry out scientific investigations'
                },
                {
                    workCheck: '/images/main-work_images/style_1.png',
                    workGoal: 'Positive learning environment for your child'
                },
            ],

            workCards: [
                {
                    workCardImg: '/images/main-work_images/toy.png',
                    workCardTitle: 'Learning & Fun',
                    workCardText: 'Praesent modea est gravida node vehicula luctus.',
                },
                {
                    workCardImg: '/images/main-work_images/meal.png',
                    workCardTitle: 'Healty Meals',
                    workCardText: 'Terminal interdum a eleifend maecenas est morbi.',
                },
                {
                    workCardImg: '/images/main-work_images/school.png',
                    workCardTitle: 'Friendly Place',
                    workCardText: 'Terminal interdum a eleifend maecenas est morbi.',
                },
                {
                    workCardImg: '/images/main-work_images/shield.png',
                    workCardTitle: 'Children Safety',
                    workCardText: 'Praesent modea est gravida node vehicula luctus.',
                },
            ]
        }
    }
}

</script>

<template>
    <div class="container row">
        <div class="work-content column">

            <h3 class="work-content-title">We have been educating children for over fifteen years. Our goal is to create
                a place that engages each
                child.</h3>
            <p class="work-content-text">Praesent arcu gravida vehicula est node maecenas loareet morbi a dosis luctus.
                Urna eget lacinia eleifend
                praesent luctus a arcu quis facilisis venenatis aenean interdum.</p>

            <MainWorksList :workGoals="workGoals" />
        </div>

        <div class="work-content">
            <MainWorksCard :workCards="workCards" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.container.row {
    padding: 5rem 0;
    align-items: center;
    gap: 3rem;

    .work-content {
        flex-basis: 50%;

        .work-content-title {
            font-size: 1.75rem;
            color: $purple-color;
            font-weight: 400;
        }
    }

    .work-content.column {
        gap: 2.75rem;
    }
}
</style>