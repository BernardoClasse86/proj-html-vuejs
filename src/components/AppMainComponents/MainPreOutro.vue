<script>
export default {

}

</script>

<template>
    <div class="container row preintro">
        <p class="preintro-title">see our kindergarten photo gallery!</p>
        <div class="btn btn-transparent" href="">
            <p>learn more</p>
            <font-awesome-icon icon="fa-solid fa-chevron-right" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

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

    .btn {
        display: flex;
        align-items: center;
        gap: 1rem;
    }

    .btn:hover {
        background-color: white;
        color: $purple-color;
    }
}
</style>