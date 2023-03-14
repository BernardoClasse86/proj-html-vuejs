<script>
export default {

}
</script>

<template>
    <div class="container contacts">
        <div class="column contacts-title">
            <h1 class="contacts-content-title">what's new</h1>
            <p class="contacts-content-text">Keep up to date with the latest news</p>
            <img class="divider-thumb" src="/images/main-intro_images/header_divider.png" alt="">
        </div>

        <div class="contact-cards row">
            <div class="card column">
                <figure>
                    <img src="/images/main-contact_images/envelope.png" alt="">
                </figure>

                <div>
                    <h3 class="contacts-details-title">Postal Address</h3>
                    <p class="contacts-details-text">Fable Care Center</p>
                    <p class="contacts-details-text">85 Fentiman Ave</p>
                    <p>Ottawa, ON K15 0T7</p>
                </div>
            </div>

            <div class="card column">
                <figure>
                    <img src="/images/main-contact_images/mobile.png" alt="">
                </figure>

                <div>
                    <h3 class="contacts-details-title">Phone & E-mail</h3>
                    <p class="contacts-details-text">Phone: 1-800-64-38</p>
                    <p class="contacts-details-text">Fax: 1-800-64-39</p>
                    <a class="contacst-details-emails">office@fable.com</a>
                </div>
            </div>

            <div class="card column">
                <figure>
                    <img src="/images/main-contact_images/clock.png" alt="">
                </figure>

                <div>
                    <h3 class="contacts-details-title">Business Hours</h3>
                    <p class="contacts-details-text">Monday - Friday</p>
                    <p class="contacts-details-text">8.00 am - 5.00 pm</p>
                    <p>Weekend Closed</p>
                </div>
            </div>

            <div class="card column">
                <figure>
                    <img src="/images/main-contact_images/document.png" alt="">
                </figure>

                <div>
                    <h3 class="contacts-details-title">Sessions</h3>
                    <p class="contacts-details-text">Mornings, 8 am - 12 noon</p>
                    <p class="contacts-details-text">Afternoons, 1 pm - 5 pm</p>
                    <p>Full Day, 8 am -5 pm</p>
                </div>
            </div>

        </div>

        <div class="text row">
            <div class="text column">
                <input class="my-input" type="text" placeholder="Your Name *">
                <input class="my-input" type="text" placeholder="Your E-mail *">
                <input class="my-input" type="text" placeholder="Subject">
            </div>

            <div class="text column">
                <textarea class="my-textaera" name="" id="" cols="30" rows="10" placeholder="Your Message *"></textarea>
            </div>

        </div>

        <div class="row">
            <div class="btn btn-orange">
                <p>send message</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.container.contacts {
    padding: 4.5rem 0;
}

.contacts-title {
    text-align: center;
    padding-bottom: 4rem;

    .contacts-content-title {
        font-size: 2.5rem;
        font-weight: 400;
        margin-bottom: 1rem;
        text-transform: capitalize;
        color: $purple-color;
    }

    .contacts-content-text {
        font-size: 1rem;
        margin-bottom: 2rem;
    }

    .divider-thumb {
        margin: 0 auto;
        width: 100px;
    }
}

.contact-cards.row {
    align-items: center;
    text-align: center;
    justify-content: center;
    gap: 7rem;
    margin-bottom: 2rem;

    .card.column {
        gap: 2rem;

        .contacts-details-title {
            font-size: 1.5rem;
            font-weight: 400;
            color: $purple-color;
            margin-bottom: 2rem;
        }

        .contacts-details-text {
            margin-bottom: 0.5rem;
        }

        .contacst-details-emails {
            text-decoration: underline;
            color: $purple-color;
            cursor: pointer;
        }
    }
}

.text.row {
    display: flex;
    gap: 2rem;
    padding: 2rem;

    justify-content: space-between;

    .text.column {
        gap: 2rem;
        flex-basis: 50%;
    }

    .my-input {
        flex-grow: 1;
        padding: 1rem;
        font-size: 1rem;
        border: 1px solid lightgray;
    }

    .my-textaera {
        flex-grow: 1;
        padding: 1rem;
        font-size: 1rem;
        border: 1px solid lightgray;
    }
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
</style>