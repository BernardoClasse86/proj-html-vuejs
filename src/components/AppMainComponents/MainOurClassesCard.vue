<script>
export default {
    props: {
        classesCards: Object,
        required: true,
    }
}

</script>

<template>
    <ul class="class-card row">

        <li class="class-row class-card-item" v-for="(classesCard, i) in classesCards" :key="i">

            <div class="class-card-desc">
                <div class="card-intro column">
                    <h4 class="card-intro-title">{{ classesCard.className }}</h4>
                    <p class="card-intro-text">{{ classesCard.classNameInfo }}</p>
                </div>

                <div class="card-content row">

                    <div class="class-card-content line column">
                        <h5 class="card-content-title">{{ classesCard.classAge }}</h5>
                        <p class="card-content-text">{{ classesCard.classAgeInfo }}</p>
                    </div>

                    <div class="class-card-content column">
                        <h5 class="card-content-title">{{ classesCard.classSize }}</h5>
                        <p class="card-content-text">{{ classesCard.classSizeInfo }}</p>
                    </div>

                </div>
            </div>

            <figure class="class-card-desc">
                <img class="class-card-thumb" :src="classesCard.classThumb" alt="">
                <div class="btn btn-orange">
                    <p>Read More</p>
                    <font-awesome-icon icon="fa-solid fa-chevron-right" />
                </div>
            </figure>
        </li>

    </ul>
</template>


<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.class-card.row {
    flex-wrap: wrap;
    gap: 30px;

    .class-card-item {
        flex-basis: calc(100% * (6/12) - 15px);
        background-color: $purple-color;
    }

    .class-row {
        display: flex;

        .class-card-desc {
            flex-basis: 50%;
            position: relative;
            color: white;

            .card-intro.column {
                padding: 1.25rem;
                margin-bottom: 1rem;
                gap: 0.75rem;

                .card-intro-title {
                    font-size: 1.25rem;
                    font-weight: 400;
                }

                .card-intro-text {
                    font-size: 0.75rem;
                }
            }

            .card-content.row {
                align-items: center;
                justify-content: center;
                text-align: center;
                padding: 1.25rem;

                .class-card-content.column {
                    gap: 0.5rem;
                    flex-basis: 50%;

                    .card-content-title {
                        font-size: 1rem;
                        font-weight: 400;
                    }

                    .card-content-text {
                        font-size: 0.75rem;
                    }
                }

                .line {
                    border-right: 1px solid white;
                }
            }

            .class-card-thumb {
                width: 100%;
                height: 100%;
            }

            .btn {
                display: flex;
                align-items: center;
                gap: 1rem;
                position: absolute;
                bottom: 0;
                right: 0;
            }

            .btn:hover {
                background-color: $purple-color;
            }
        }
    }

}
</style>