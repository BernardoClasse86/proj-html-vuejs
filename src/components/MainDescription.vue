<script>
export default {
    data() {
        return {
            descSlides: [
                {
                    image: '/images/main-desc_images/gallery_01-690x506.jpg'
                },
                {
                    image: '/images/main-desc_images/gallery_07-690x506.jpg'
                },
                {
                    image: '/images/main-desc_images/gallery_08-690x506.jpg'
                },
            ],

            slideCounter: 0
        }
    },
    methods: {
        nextSlide() {

            this.slideCounter++

            if (this.slideCounter === this.descSlides.length) {

                this.slideCounter = 0
            }

        },

        prevSlide() {

            this.slideCounter--

            if (this.slideCounter < 0) {

                this.slideCounter = this.descSlides.length - 1
            }

        },
    },
}

</script>

<template>
    <div class="container row">
        <div class="column">
            <div class="desc-row">
                <div class="btn btn-orange">
                    <p>overview</p>
                    <font-awesome-icon icon="fa-solid fa-caret-down" class="triangle icon" />
                </div>
                <div class="btn">
                    <p>our mission</p>
                    <font-awesome-icon icon="fa-solid fa-caret-down" class="triangle icon-2" />
                </div>
            </div>

            <div class="description-item">
                <h2 class="description-title">Our philosophy is learning through play as we offer a stimulating environment
                    for children.</h2>

                <div class="desc-item-row">
                    <figure class="desc-thumb-style">
                        <img class="desc-thumb" src="/images/main-desc_images/clock_alt.png" alt="">
                    </figure>

                    <div class="desc-item-style">
                        <h5 class="desc-item-title">full day session</h5>
                        <p class="desc-item-text">Pulvinar est metro ligula blandit maecenas retrum gravida cuprum.</p>
                    </div>
                </div>

                <div class="desc-item-row">
                    <figure class="desc-thumb-style">
                        <img class="desc-thumb" src="/images/main-desc_images/diagram_alt.png" alt="">
                    </figure>

                    <div>
                        <h5 class="desc-item-title">varied classes</h5>
                        <p class="desc-item-text">Pulvinar est metro ligula blandit maecenas retrum gravida cuprum. Maecenas
                            node estibulum.</p>
                    </div>
                </div>

            </div>

        </div>

        <div class="column">
            <div v-for="(descSlide, i) in descSlides" class="slider off-slide"
                :class="i === slideCounter ? 'on-slide' : ''">
                <img class="desc-main-slide" :src="descSlide.image" alt="">
                <font-awesome-icon icon="fa-solid fa-chevron-right" class="arrow right" @click="nextSlide" />
                <font-awesome-icon icon="fa-solid fa-chevron-left" class="arrow left" @click="prevSlide" />
            </div>

            <div class="slider-row">
                <figure class="desc-slide">
                    <img class="" src="/images/main-desc_images/gallery_01-690x506.jpg" alt="">
                </figure>

                <figure class="desc-slide">
                    <img class="" src="/images/main-desc_images/gallery_07-690x506.jpg" alt="">
                </figure>

                <figure class="desc-slide">
                    <img class="" src="/images/main-desc_images/gallery_08-690x506.jpg" alt="">
                </figure>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/generals.scss' as *;
@use '../style/partials/variables' as *;
@use '../style/partials/reset' as *;

.off-slide {
    display: none;
}

.on-slide {
    display: block;
}

.container.row {
    padding: 5rem 0;
    gap: 3.75rem;

    .column {
        flex-basis: 50%;
        gap: 0.5rem;

        .slider {
            flex-shrink: 0;
            position: relative;

            .arrow {
                background-color: $orange-color;
                padding: 1rem;
                color: white;
                cursor: pointer;
            }

            .arrow.left {
                position: absolute;
                top: 50%;
                transform: translateY(-50%);
                left: 0;
            }

            .arrow.right {
                position: absolute;
                top: 50%;
                transform: translateY(-50%);
                right: 0;
            }
        }

        .slider-row {
            flex-grow: 1;
            display: flex;
            align-items: center;
            gap: 1rem;

            .desc-slide {
                flex-basis: calc(100% / (4/12));
                padding-bottom: 0.5rem;
            }
        }
    }
}

.btn {
    position: relative;

    .triangle {
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        bottom: -14px;
        font-size: 1.5rem;

    }

    .triangle.icon {
        color: $orange-color;
    }

    .triangle.icon-2 {
        display: none;
    }
}

.btn:hover {
    color: white;
    background-color: $orange-color;
}

.btn:hover .icon-2 {
    display: block;
    color: $orange-color;
}

.arrow:hover {
    background-color: $purple-color !important;
}

.desc-row {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin-bottom: 3rem;

    .btn {
        padding: 0.5rem 1.5rem;
        cursor: pointer;
    }
}

.description-title {
    margin-bottom: 3rem;
    font-weight: 400;
    font-size: 1.75rem;
    color: $purple-color;
}

.desc-item-row {
    display: flex;
    align-items: center;
    gap: 2rem;
    margin-bottom: 2rem;

    .desc-thumb-style {
        width: 84px;
        height: 84px;
        border-radius: 50%;
        background-color: $orange-color;
        flex-shrink: 0;
        display: flex;
        justify-content: center;
        align-items: center;

        .desc-thumb {
            width: 32px;
        }
    }

    .desc-item-style {
        flex-grow: 1;
    }

    .desc-item-title {
        margin-bottom: 1.5rem;
        font-weight: 400;
        font-size: 1.5rem;
        color: $purple-color;
        text-transform: capitalize;
    }
}
</style>