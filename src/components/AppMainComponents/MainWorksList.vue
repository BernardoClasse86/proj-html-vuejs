<script>
export default {
    props: {
        workGoals: Object,
        required: true
    }
}

</script>

<template>
    <ul>
        <li class="work-list row" v-for="(ourWork, i) in workGoals" :key="i">
            <img :src="ourWork.workCheck" alt="">
            <p>{{ ourWork.workGoal }}</p>
        </li>
    </ul>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.work-list.row {
    align-items: center;
    gap: 1rem;
    margin-bottom: 1rem;
}
</style>