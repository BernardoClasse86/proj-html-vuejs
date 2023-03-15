<script>
import FooterCloseAboutUs from './FooterCloseAboutUs.vue'
import FooterCloseArchives from './FooterCloseArchives.vue';
import FooterCloseFeatures from './FooterCloseFeatures.vue';
import FooterCloseRecentPost from './FooterCloseRecentPost.vue';

export default {

    components: {
        FooterCloseAboutUs,
        FooterCloseArchives,
        FooterCloseFeatures,
        FooterCloseRecentPost,
    },

    data() {
        return {
            archivesMonths: [
                'October',
                'September',
                'August',
                'July',
                'June',
                'May',
            ],

            featuresList: [
                {
                    listImg: '/images/footer-close_images/style_4_alt.png',
                    listText: 'Friendly and welcoming place',
                },
                {
                    listImg: '/images/footer-close_images/style_4_alt.png',
                    listText: 'Science and art classes',
                },
                {
                    listImg: '/images/footer-close_images/style_4_alt.png',
                    listText: 'Positive learning environment',
                },
                {
                    listImg: '/images/footer-close_images/style_4_alt.png',
                    listText: 'Educational field trips',
                },
                {
                    listImg: '/images/footer-close_images/style_4_alt.png',
                    listText: 'Writing and reading classes',
                },
                {
                    listImg: '/images/footer-close_images/style_4_alt.png',
                    listText: 'Science and art classes',
                },
            ],

            recentPosts: [
                {
                    postImg: '/images/footer-close_images/blog_09-150x150.jpg',
                    postTitle: 'Drawing and Painting Lessons',
                    postIcon: '/images/footer-close_images/date_footer.png',
                    postDate: 'October 03, 2014',
                },
                {
                    postImg: '/images/footer-close_images/blog_10-150x150.jpg',
                    postTitle: 'Fall Parents Meeting Day',
                    postIcon: '/images/footer-close_images/date_footer.png',
                    postDate: 'October 03, 2014',
                },
                {
                    postImg: '/images/footer-close_images/blog_08-150x150.jpg',
                    postTitle: 'Birthday in Kindergarten',
                    postIcon: '/images/footer-close_images/date_footer.png',
                    postDate: 'September 20, 2014',
                },
            ]
        }
    }
}
</script>

<template>
    <div class="container row">
        <div class="footer-item">
            <FooterCloseAboutUs />
        </div>

        <div class="footer-item">
            <FooterCloseArchives :archivesMonths="archivesMonths" />
        </div>

        <div class="footer-item">
            <FooterCloseFeatures :featuresList="featuresList" />
        </div>

        <div class="footer-item">
            <FooterCloseRecentPost :recentPosts="recentPosts" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.container.row {
    padding: 3.5rem 0;
    justify-content: center;
    gap: 3rem;

    .footer-item {
        flex-basis: calc(100% * (3/12));
    }
}
</style>