<script>
export default {
    props: {
        recentPosts: Object,
        required: true
    }
}
</script>

<template>
    <div class="recent-post column">
        <h3 class="recent-post-title">Recent Posts</h3>
        <div v-for="(post, i) in recentPosts" :key="i" class="row">
            <figure>
                <img :src="post.postImg" alt="">
            </figure>

            <div>
                <h4>{{ post.postTitle }}</h4>

                <div class="row">
                    <img :src="post.postIcon" alt="">
                    <p class="">{{ post.postDate }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.recent-post.column {
    gap: 1rem;
}
</style>