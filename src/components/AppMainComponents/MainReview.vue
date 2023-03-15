<script>
export default {

    data() {
        return {
            reviews: [
                {
                    reviewText: 'Fable Kindergarten is a great place for my daughter to start her schooling experience. It’s welcoming and safe and my daughter loves being there.',
                    reviewAuthor: 'Matthew D. Campbell',
                    reviewIndex: ''
                },
                {
                    reviewText: 'I have a 1 year old and a 5 year old who have been attending for a year now. I can not tell you how much I adore and appreciate all of the wonderful staff.',
                    reviewAuthor: 'Kennth M.Garcia',
                    reviewIndex: ''
                },
                {
                    reviewText: 'I have to say that I have 2 children ages 5 and 2 and have used various daycare’s in Kindergartens and this is by far the very best I have ever used.',
                    reviewAuthor: 'Cecil J. Kirk',
                    reviewIndex: ''
                },
                {
                    reviewText: 'Fable Kindergarten is a great place for my daughter to start her schooling experience. It’s welcoming and safe and my daughter loves being there.',
                    reviewAuthor: 'Joe R. Hamblen',
                    reviewIndex: ''
                },
                {
                    reviewText: 'This letter is to recognize you and your staff for doing an excellent job teaching my son. His skill level is significantly better since attending Fable.',
                    reviewAuthor: 'Toni I. Robinette',
                    reviewIndex: ''
                },
                {
                    reviewText: 'I have to say that I have 2 children ages 5 and 2 and have used various daycare’s in Kindergartens and this is by far the very best I have ever used.',
                    reviewAuthor: 'Emma E. Shook',
                    reviewIndex: ''
                }
            ],

            reviewsCounter: 0
        }
    },
    methods: {
        changeActiveReview(index) {

            this.reviewsCounter = index

        }
    }

}
</script>

<template>
    <div class="container">
        <div v-for="(review, i) in reviews" :key="i" class="column off-review"
            :class="i === reviewsCounter ? 'on-review' : ''">
            <figure class="quote-thumb-style">
                <img src="/images/main-reviews_images/quote_alt.png" alt="">
            </figure>
            <p class="review-text">{{ review.reviewText }}</p>
            <p class="review-author">{{ review.reviewAuthor }}</p>
        </div>

        <div class="select-row">
            <div v-for="(n, i) in 6" :key="i" class="solid-select" :class="i === reviewsCounter ? 'move-up' : ''"
                @click="changeActiveReview(i)"></div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.container {
    padding: 4.5rem;

    .off-review {
        display: none;
    }

    .on-review {
        display: block;
    }

    .column {
        text-align: center;

        .quote-thumb-style {
            width: 80px;
            height: 80px;
            border: 2px solid white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto;
        }

        .review-text {
            margin-top: 2rem;
            font-size: 2rem;
            color: white;
            font-weight: 300;
        }

        .review-text::after {
            content: "";
            padding: 2rem 1rem;
            display: block;
            margin: 0 auto;
            width: 10px;
            height: 1px;
            border-bottom: 1px solid white;
        }

        .review-author {
            margin-top: 2rem;
            margin-bottom: 4rem;
            color: white;
            font-size: 0.75rem;
        }
    }
}

.select-row {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1rem;

    .move-up {
        margin-bottom: 1rem;
    }

    .solid-select {
        border: 2px solid white;
        padding: 0.25rem 1rem;
        cursor: pointer;
    }

    .solid-select:hover {
        border: 2px solid rgba(255, 255, 255, 0.5);
    }
}
</style>