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
            <a class="list-link__text" href="">{{ navItem.navText }}</a>
        </li>

    </ul>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.list-item {
    gap: 1rem;
    padding: 0 1.5rem;
    cursor: pointer;

    .list-link__thumb {
        aspect-ratio: 1;
        margin: 0 auto;
        width: 32px;
    }

    .list-link__text {
        text-align: center;
        color: $purple-color;
        text-transform: capitalize;
    }
}
</style>