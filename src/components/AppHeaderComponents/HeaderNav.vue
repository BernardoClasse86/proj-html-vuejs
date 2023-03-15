<script>
export default {
    props: {
        navItems: Object,
        required: true
    }
}
</script>

<template>
    <ul class="row">

        <li v-for="(navItem, i) in navItems" :key="i" class="column list-item">
            <img class="list-link__thumb" :src="navItem.navImg" alt="">
            <img class="list-link__thumb-off" :src="navItem.navAltImg" alt="">
            <a class="list-link__text" href="">{{ navItem.navText }}</a>
        </li>

    </ul>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.list-item:hover {
    background-color: $orange-color;
}

.list-item:hover a {
    color: white;
}

.list-item:hover .list-link__thumb {
    display: none;
}

.list-item:hover .list-link__thumb-off {
    display: block;
}


.list-item {
    gap: 1rem;
    padding: 2.5rem 1.5rem;
    cursor: pointer;

    .list-link__thumb {
        aspect-ratio: 1;
        margin: 0 auto;
        width: 32px;
    }

    .list-link__thumb-off {
        aspect-ratio: 1;
        margin: 0 auto;
        width: 32px;
        display: none;
    }

    .list-link__text {
        text-align: center;
        color: $purple-color;
        text-transform: capitalize;
    }
}
</style>