<script>
export default {

}

</script>

<template>
    <div class="container row">
        <div class="column">
            <div class="desc-row">
                <div class="btn btn-orange">
                    overview
                    <!-- <font-awesome-icon icon="fa-solid fa-caret-down" /> -->
                </div>
                <div class="btn">our mission</div>
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
                        <p class="desc-item-text">Pulvinar est metro ligula blandit maecenas retrum gravida cuprum.
                            Maecenas
                            node
                            estibulum.</p>
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
            <div class="slider">
                <font-awesome-icon icon="fa-solid fa-chevron-left" class="arrow left" />
                <img class="desc-main-slide" src="/images/main-desc_images/gallery_01-690x506.jpg" alt="">
                <font-awesome-icon icon="fa-solid fa-chevron-right" class="arrow right" />
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

        .slider-row figure:nth-child(2) {
            border-bottom: 2px solid $orange-color;
        }
    }
}

.btn:hover {
    background-color: $orange-color;
    color: white;
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