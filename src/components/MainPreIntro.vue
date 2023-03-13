<script>
export default {

}

</script>

<template>
    <div class="container row preintro">
        <p class="preintro-title">how to enroll your child to a class?</p>
        <a class="btn btn-transparent" href="">learn more <font-awesome-icon icon="fa-solid fa-chevron-right" /></a>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/generals.scss' as *;
@use '../style/partials/variables' as *;
@use '../style/partials/reset' as *;

.row.preintro {
    padding: 3rem 0;
    align-items: center;
    justify-content: space-between;

    .preintro-title {
        font-size: 2.5rem;
        font-weight: 300;
        color: white;
        text-transform: capitalize;
    }
}
</style>