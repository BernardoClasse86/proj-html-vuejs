<script>
export default {

    data() {
        return {
            reviews: [
                {
                    reviewText: 'Fable Kindergarten is a great place for my daughter to start her schooling experience. It’s welcoming and safe and my daughter loves being there.',
                    reviewAuthor: 'Joe R. Hamblen'
                }
            ]
        }
    }

}
</script>

<template>
    <div class="container">
        <div v-for="review in reviews" class="column">
            <figure class="quote-thumb-style">
                <img src="/images/main-reviews_images/quote_alt.png" alt="">
            </figure>
            <p class="review-text">{{ review.reviewText }}</p>
            <p class="review-author">{{ review.reviewAuthor }}</p>
        </div>

        <div class="select-row">
            <div v-for="n in 6" class="solid-select"></div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.container {
    padding: 4.5rem;

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

    .solid-select {
        border: 2px solid white;
        padding: 0.40rem 1.25rem;
        cursor: pointer;
    }

    .solid-select:hover {
        border: 2px solid rgba(255, 255, 255, 0.5);
    }
}
</style>