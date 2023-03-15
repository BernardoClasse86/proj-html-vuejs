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
            <li class="list-row" v-for="(listItem, i) in featuresList" :key="i">
                <img :src="listItem.listImg" alt="">
                <p class="list-text">{{ listItem.listText }}</p>
            </li>
        </ul>

    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.features.column {
    gap: 2rem;
    color: rgba(255, 255, 255, 0.5);

    .features-title {
        font-size: 1.25rem;
        text-transform: uppercase;
        font-weight: 400;
        color: white;
    }

    .features-title::after {
        content: "";
        display: block;
        padding: 0.5rem 2rem;
        width: 10px;
        border-bottom: 1px solid white;
    }

}

.list-row {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    font-size: 0.875rem;

    .list-text {
        margin-bottom: 0.5rem;
    }
}
</style>