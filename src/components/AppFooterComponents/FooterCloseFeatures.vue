<script>
export default {
    props: {
        featuresList: Object,
        required: true,
    }
}
</script>

<template>
    <div class="features column">
        <h3 class="features-title">Our Features</h3>
        <p class="features-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi optio veniam corporis
            aperiam, provident rerum?
        </p>

        <ul>
            <li class="row" v-for="(listItem, i) in featuresList" :key="i">
                <img :src="listItem.listImg" alt="">
                <p>{{ listItem.listText }}</p>
            </li>
        </ul>

    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.features.column {
    gap: 1rem;
}
</style>