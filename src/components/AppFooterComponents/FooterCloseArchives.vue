<script>
export default {
    props: {
        archivesMonths: Array,
        required: true,
    }
}
</script>

<template>
    <div class="archives column">
        <h3 class="archives-title">Archives</h3>
        <ul>
            <li v-for="(month, i) in archivesMonths" :key="i">
                <p class="archives-months">{{ month }}</p>
            </li>
        </ul>

    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.archives.column {
    gap: 2rem;
    color: rgba(255, 255, 255, 0.5);


    .archives-title {
        font-size: 1.25rem;
        text-transform: uppercase;
        font-weight: 400;
        color: white;
    }

    .archives-title::after {
        content: "";
        display: block;
        padding: 0.5rem 2rem;
        width: 10px;
        border-bottom: 1px solid white;
    }

    .archives-months {
        margin-bottom: 0.25rem;
        font-size: 0.75rem;
        color: rgba(255, 255, 255, 0.5);
        border: 1px solid rgba(255, 255, 255, 0.5);
        padding: 0.75rem;
        cursor: pointer;
        text-transform: uppercase;
    }

    .archives-months:hover {
        color: white;
        border: 2px solid white;
    }
}
</style>