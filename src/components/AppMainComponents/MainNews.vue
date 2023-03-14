<script>
import MainNewsCard from './MainNewsCard.vue'
export default {

    components: {
        MainNewsCard,
    },

    data() {
        return {
            newsCards: [
                {
                    newsDate: 'October 03, 2014',
                    newsImg: '/images/main-news_images/blog_09-690x414.jpg',
                    newsTitle: 'Drawing and Painting Lessons',
                    newsComment: 'Magna est consectetur interdum modest dictum. Curabitur est faucibus, malesuada esttincidunt etos et mauris, nunc a libero govum est cuprum [...]',
                    newsVisitors: '42',
                    newsAuthorIcon: '/images/main-news_images/author.png',
                    newsAuthor: 'Anna Brown',
                    newsTypeIcon: '/images/main-news_images/category.png',
                    newsTypeOne: 'Events',
                    newsTypeTwo: 'Fun'
                },
                {
                    newsDate: 'October 03, 2014',
                    newsImg: '/images/main-news_images/blog_10-690x414.jpg',
                    newsTitle: 'Fall Parents Meeting Day',
                    newsComment: 'Magna est consectetur interdum modest dictum. Curabitur est faucibus, malesuada esttincidunt etos et mauris, nunc a libero govum est cuprum [...]',
                    newsVisitors: '19',
                    newsAuthorIcon: '/images/main-news_images/author.png',
                    newsAuthor: 'Anna Brown',
                    newsTypeIcon: '/images/main-news_images/category.png',
                    newsTypeOne: 'Dance',
                    newsTypeTwo: 'Education'
                },
                {
                    newsDate: 'September 20, 2014',
                    newsImg: '/images/main-news_images/blog_08-690x414.jpg',
                    newsTitle: 'Birthday in Kindergarten',
                    newsComment: 'Magna est consectetur interdum modest dictum. Curabitur est faucibus, malesuada esttincidunt etos et mauris, nunc a libero govum est cuprum [...]',
                    newsVisitors: '22',
                    newsAuthorIcon: '/images/main-news_images/author.png',
                    newsAuthor: 'Anna Brown',
                    newsTypeIcon: '/images/main-news_images/category.png',
                    newsTypeOne: 'Games',
                    newsTypeTwo: 'General'
                },
            ]
        }
    }

}
</script>

<template>
    <div class="container news">
        <div class="column news-content-title">
            <h1 class="news-title">what's new</h1>
            <p class="news-text">Keep up to date with the latest news</p>
            <img class="divider-thumb" src="/images/main-intro_images/header_divider.png" alt="">
        </div>

        <div class="news row">
            <MainNewsCard :newsCards="newsCards" />
        </div>

        <div class="row">
            <div class="btn btn-orange">
                <p>go to blog</p>
                <font-awesome-icon icon="fa-solid fa-chevron-right" />
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.container.news {
    padding: 4.5rem 0;
}

.news.row {
    padding-bottom: 2.75rem;
}

.btn {
    margin: 0 auto;
    display: flex;
    align-items: center;
    gap: 1rem;
}

.btn:hover {
    background-color: $purple-color;
}

.news-content-title {
    text-align: center;
    padding-bottom: 4rem;

    .news-title {
        font-size: 2.5rem;
        font-weight: 400;
        margin-bottom: 1rem;
        text-transform: capitalize;
        color: $purple-color;
    }

    .news-text {
        font-size: 1rem;
        margin-bottom: 2rem;
    }

    .divider-thumb {
        margin: 0 auto;
        width: 100px;
    }
}
</style>