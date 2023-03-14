<script>
import MainOurClassesCard from './MainOurClassesCard.vue';

export default {
    components: {
        MainOurClassesCard,
    },

    data() {
        return {
            classesCards: [
                {
                    classThumb: '/images/main-class-card_images/class_01-690x506.jpg',
                    className: 'Little Lambs',
                    classNameInfo: 'Class Name',
                    classAge: '12-24',
                    classAgeInfo: 'Month olds',
                    classSize: '9',
                    classSizeInfo: 'Class size'
                },
                {
                    classThumb: '/images/main-class-card_images/class_02-690x506.jpg',
                    className: 'Bouncy Bears',
                    classNameInfo: 'Class Name',
                    classAge: '2-3',
                    classAgeInfo: 'Year olds',
                    classSize: '12',
                    classSizeInfo: 'Class size'
                },
                {
                    classThumb: '/images/main-class-card_images/class_03-690x506.jpg',
                    className: 'Tenderhearts',
                    classNameInfo: 'Class Name',
                    classAge: '3-4',
                    classAgeInfo: 'Year olds',
                    classSize: '15',
                    classSizeInfo: 'Class size'
                },
                {
                    classThumb: '/images/main-class-card_images/class_04-690x506.jpg',
                    className: 'Shining Stars',
                    classNameInfo: 'Class Name',
                    classAge: '4-5',
                    classAgeInfo: 'Year olds',
                    classSize: '20',
                    classSizeInfo: 'Class size'
                },

            ]
        }
    }
}

</script>

<template>
    <div class="container ourclasses">
        <div class="column ourclasses-content-title">
            <h1 class="ourclasses-title">our classes</h1>
            <p class="ourclasses-text">Our professional program has four dedicated classes</p>
            <img class="divider-thumb" src="/images/main-intro_images/header_divider.png" alt="">
        </div>

        <div class="ourclass-row">
            <h2 class="ourclass-subtitle">We provided four classes with nine to twenty children each aged twelve month to
                five years of age.</h2>
            <p class="ourclass-subtext">Praesent arcu gravida vehicula est node maecenas loareet morbi a dosis luctus. Urna
                eget lacinia eleifend
                praesent luctus a arcu quis facilisis venenatis. Aenean interdum, nibh vitae sodales, magna ante feugiat
                elit maecenas.</p>
        </div>

        <div class="ourclass-card-row">
            <MainOurClassesCard :classesCards="classesCards" />
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.container.ourclasses {
    padding: 4.5rem 0;
}

.ourclasses-content-title {
    text-align: center;
    padding-bottom: 4rem;

    .ourclasses-title {
        font-size: 2.5rem;
        font-weight: 400;
        margin-bottom: 1rem;
        text-transform: capitalize;
        color: $purple-color;
    }

    .ourclasses-text {
        font-size: 1rem;
        margin-bottom: 2rem;
    }

    .divider-thumb {
        margin: 0 auto;
        width: 100px;
    }

}

.ourclass-row {
    display: flex;
    align-items: center;
    gap: 3rem;
    margin-bottom: 4rem;

    .ourclass-subtitle {
        flex-basis: 50%;
        font-size: 1.5rem;
        color: $purple-color;
        font-weight: 400;
    }

    .ourclass-subtext {
        flex-basis: 50%;
    }
}
</style>