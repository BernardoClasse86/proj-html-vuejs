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
    gap: 1rem;

    .archives-months {
        border: 1px solid white;
        padding: 0.5rem;
    }
}
</style>