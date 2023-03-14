<script>
export default {
    props: {
        staffCards: Object,
        required: true,
    }
}

</script>

<template>
    <ul class="staff-card row">

        <li class="staff-row staff-card-item" v-for="(staffCard, i) in staffCards" :key="i">

            <figure class="staff-card-desc column">
                <img class="staff-card-thumb" :src="staffCard.staffImg" alt="">
                <h5 class="staff-card-name">{{ staffCard.staffName }}</h5>
                <p class="staff-card-role">{{ staffCard.staffRole }}</p>
            </figure>

            <div class="staff-card-desc">
                <div class="card-details column">
                    <figure class="staff-quote-style">
                        <img class="staff-quote" src="/images/main-staff_images/quote.png" alt="">
                    </figure>
                    <p class="card-staff-overview">{{ staffCard.staffOverview }}</p>

                    <div class="links-row">
                        <div class="btn btn-orange">
                            <img :src="staffCard.staffLinkOne" alt="">
                        </div>
                        <div class="btn btn-orange">
                            <img :src="staffCard.staffLinkTwo" alt="">
                        </div>
                        <div class="btn btn-orange">
                            <img :src="staffCard.staffLinkThree" alt="">
                        </div>
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

.staff-card.row {
    flex-wrap: wrap;
    gap: 40px;

    .staff-card-item {
        flex-basis: calc(100% * (6/12) - 20px);
    }

    .staff-row {
        display: flex;
        gap: 2rem;

        .staff-card-desc.column {
            gap: 1rem;
            flex-shrink: 0;
            text-align: center;
            flex-basis: 50%;
            color: black;

            .staff-card-name {
                font-size: 1rem;
                color: $purple-color;
                font-weight: 400;
            }

            .staff-card-role {
                font-size: 0.75rem;
            }
        }

        .card-details.column {
            gap: 1.75rem;
            position: relative;

            .staff-quote-style {
                width: 115px;
                height: 54px;
                padding: 0 1rem;
                border: 2px solid $orange-color;
                display: flex;
                align-items: center;
                justify-content: flex-end;
                position: absolute;
                right: 180px;
                top: 30px;
            }

            .card-staff-overview {
                margin-top: 7rem;
            }
        }
    }
}

.links-row {
    display: flex;
    align-items: center;
    gap: 0.125rem;
}

.btn.btn-orange {
    line-height: 1rem;
    padding: 0.25rem;
}
</style>