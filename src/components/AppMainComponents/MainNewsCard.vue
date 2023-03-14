<script>
export default {
    props: {
        newsCards: Object,
        required: true
    }
}
</script>

<template>
    <ul class="news row">

        <li class="" v-for="(newsCard, i) in newsCards" :key="i">

            <div class="column">
                <p class="news-date">{{ newsCard.newsDate }}</p>

                <figure class="news-thumb-style">
                    <img class="news-thumb" :src="newsCard.newsImg" alt="">
                    <div class="btn btn-orange">
                        <p>{{ newsCard.newsVisitors }}</p>
                    </div>
                </figure>

                <div class="news-content">
                    <h4 class="news-content-title">{{ newsCard.newsTitle }}</h4>
                    <p class="news-content-text">{{ newsCard.newsComment }}</p>
                </div>

                <div class="news-details row">
                    <div class="news-details-content row">
                        <img class="news-icon" :src="newsCard.newsAuthorIcon" alt="">
                        <p class="news-details-text">{{ newsCard.newsAuthor }}</p>
                    </div>
                    <div class="news-details-content row">
                        <img class="news-icon" :src="newsCard.newsTypeIcon" alt="">
                        <p class="news-details-text">{{ newsCard.newsTypeOne }}, {{ newsCard.newsTypeTwo }}</p>
                    </div>
                </div>
            </div>

        </li>

    </ul>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.news.row {
    gap: 2rem;
    align-items: center;
}

.column {
    gap: 1.25rem;
}

.news-date {
    color: grey;
}

.news-thumb-style {
    position: relative;

    .news-thumb {
        width: 100%;
    }

    .btn {
        position: absolute;
        right: 0;
        bottom: 5px;
        padding: 0.125rem 0.5rem;
    }

    .btn:hover {
        background-color: $purple-color;
    }
}


.news-content {
    border-bottom: 1px solid lightgray;

    .news-content-title {
        color: $purple-color;
        font-size: 1.5rem;
        font-weight: 400;
        margin-bottom: 1.75rem;
        cursor: pointer;
    }

    .news-content-title:hover {
        text-decoration: underline;
    }

    .news-content-text {
        margin-bottom: 1.25rem;
    }
}

.news-details.row {
    gap: 1.5rem;

    .news-details-content.row {
        gap: 0.75rem;
        align-items: center;

        .news-icon {
            width: 16px;
            height: 16px;
        }

        .news-details-text {
            font-size: 0.875rem;
        }
    }
}
</style>