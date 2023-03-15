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
        <div class="post-row" v-for="(post, i) in recentPosts" :key="i">
            <figure class="post-thumb">
                <img :src="post.postImg" alt="">
            </figure>

            <div class="post-column">
                <h4 class="post-title">{{ post.postTitle }}</h4>

                <div class="date-row">
                    <img class="post-date-icon" :src="post.postIcon" alt="">
                    <p class="post-date">{{ post.postDate }}</p>
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
    gap: 2rem;
    color: white;

    .recent-post-title {
        font-size: 1.25rem;
        text-transform: uppercase;
        font-weight: 400;
    }

    .recent-post-title::after {
        content: "";
        display: block;
        padding: 0.5rem 2rem;
        width: 10px;
        border-bottom: 1px solid white;
    }
}

.post-row {
    display: flex;
    align-items: center;
    gap: 0.5rem;

    .post-thumb {
        width: 80px;
        flex-shrink: 0;
    }

    .post-column {
        display: flex;
        flex-direction: column;
        gap: 0.5rem;

        .post-title {
            font-weight: 400;
            font-size: 1.125rem;
        }

        .date-row {
            display: flex;
            gap: 0.5rem;
        }

        .post-date-icon {
            width: 16px;
            height: 16px;
        }
    }
}
</style>