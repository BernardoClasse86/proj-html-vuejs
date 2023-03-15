<script>
export default {

}
</script>

<template>
    <section class="container hero">
        <div class="column">
            <h3 class="hero-opening">learning & fun</h3>
            <h1 class="hero-title">learning program</h1>
            <h1 class="hero-subtitle">& after-school care</h1>
        </div>

        <div class="btn btn-orange" href="">buy this theme now</div>

        <img class="slide-img-1" src="/images/hero/slider_slide3_img1.png" alt="">
        <img class="slide-img-2" src="/images/hero/slider_slide3_img2.png" alt="">
        <img class="slide-img-3" src="/images/hero/slider_slide3_img3.png" alt="">
        <img class="slide-icon-10" src="/images/hero/slider_icon10.png" alt="">
        <img class="slide-icon-14" src="/images/hero/slider_icon14.png" alt="">
        <img class="slide-icon-15" src="/images/hero/slider_icon15.png" alt="">
        <img class="slide-icon-17" src="/images/hero/slider_icon17.png" alt="">
        <img class="slide-icon-18" src="/images/hero/slider_icon18.png" alt="">

        <div class="select-row">
            <div v-for="n in 3" class="solid-select"></div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.hero {
    padding: 9.5rem 0;
    position: relative;
}

.hero-opening {
    font-size: 2rem;
    text-transform: capitalize;
    color: $orange-color;
    margin-bottom: 1rem;
    font-family: 'Handlee', cursive;
}

.hero-title {
    font-size: 2.5rem;
    text-transform: capitalize;
    color: $purple-color;
}

.hero-subtitle {
    font-size: 2.5rem;
    text-transform: capitalize;
    color: $purple-color;
    font-weight: 300;
    margin-bottom: 2rem;
}

.btn.btn-orange {
    background-color: $orange-color;
    display: inline;
}

.btn:hover {
    background-color: $purple-color;
}

.slide-img-1 {
    position: absolute;
    bottom: 40px;
    right: 0;
}

.slide-img-2 {
    position: absolute;
    bottom: 40px;
    left: 30%;
}

.slide-img-3 {
    position: absolute;
    bottom: 40px;
    right: -50px;
}

.slide-icon-10 {
    position: absolute;
    top: 30px;
    left: 26%;
}

.slide-icon-14 {
    position: absolute;
    top: 150px;
    left: 28%;
}

.slide-icon-15 {
    position: absolute;
    top: 130px;
    left: 35%;
}

.slide-icon-17 {
    position: absolute;
    top: 50px;
    left: 44%;
}

.slide-icon-18 {
    position: absolute;
    top: 30px;
    right: 10%;
}

.select-row {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    bottom: 3%;

    .solid-select {
        border: 2px solid $orange-color;
        padding: 0.5rem 1.5rem;
        cursor: pointer;
    }

    .solid-select:hover {
        border: 2px solid $purple-color;
    }
}
</style>