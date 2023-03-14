<script>
import MainStaffCard from './MainStaffCard.vue';

export default {
    components: {
        MainStaffCard,
    },

    data() {
        return {
            staffCards: [
                {
                    staffImg: '/images/main-staff_images/team_04.jpg',
                    staffName: 'Ruth Richie',
                    staffRole: 'Teacher',
                    staffOverview: 'I have just finished my studies in Early Childhood Education, and I am also the kid’s yoga teacher here at Fable. I enjoy cooking, swimming and bike riding in my free time.',
                    staffLinkOne: '/images/main-staff_images/mail.png',
                    staffLinkTwo: '/images/main-staff_images/facebook.png',
                    staffLinkThree: '/images/main-staff_images/pinterest.png',
                },
                {
                    staffImg: '/images/main-staff_images/team_03.jpg',
                    staffName: 'Katie Willmore',
                    staffRole: 'Assistant Teacher',
                    staffOverview: 'My name is Katie. I grew up and studied in Canada. This is my second year at Fable and love every minute of it, making the children’s learning experience fun.',
                    staffLinkOne: '/images/main-staff_images/dribbble.png',
                    staffLinkTwo: '/images/main-staff_images/stumbleupon.png',
                    staffLinkThree: '/images/main-staff_images/instagram.png',
                },
                {
                    staffImg: '/images/main-staff_images/team_02.jpg',
                    staffName: 'Angelica Watson',
                    staffRole: 'Lead Teacher',
                    staffOverview: 'I hold a degree in Early Childhood Education and an advanced English language certificate. I have been working as a kindergarten teacher since 2002.',
                    staffLinkOne: '/images/main-staff_images/bing.png',
                    staffLinkTwo: '/images/main-staff_images/skype.png',
                    staffLinkThree: '/images/main-staff_images/linkedin.png',
                },
                {
                    staffImg: '/images/main-staff_images/team_01.jpg',
                    staffName: 'Angela Lynn',
                    staffRole: 'Teacher',
                    staffOverview: 'I have completed a Graduate Diploma in Early Childhood Teaching. I have worked with children aged from six weeks to eight years. This is my second year at Fable.',
                    staffLinkOne: '/images/main-staff_images/youtube.png',
                    staffLinkTwo: '/images/main-staff_images/twitter.png',
                    staffLinkThree: '/images/main-staff_images/googleplus.png',
                },
            ]
        }
    }

}
</script>

<template>
    <div class="container our-staff">
        <div class="column our-staff-content-title">
            <h1 class="our-staff-title">meet out staff</h1>
            <p class="our-staff-text">With education and experience in early childhood care</p>
            <img class="divider-thumb" src="/images/main-intro_images/header_divider.png" alt="">
        </div>

        <div class="our-staff-row">
            <h2 class="our-staff-subtitle">Our staff consists of three teachers and one assistant with experience in early
                childhood care.</h2>
            <p class="our-staff-subtext">Praesent arcu gravida vehicula est node maecenas loareet morbi a dosis luctus. Urna
                eget lacinia eleifend praesent luctus a arcu quis facilisis venenatis. Aenean interdum, nibh vitae sodales,
                magna ante feugiat elit maecenas.</p>
        </div>

        <div>
            <MainStaffCard :staffCards="staffCards" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../style/generals.scss' as *;
@use '../../style/partials/variables' as *;
@use '../../style/partials/reset' as *;

.container.our-staff {
    padding: 4.5rem 0;
}

.our-staff-content-title {
    text-align: center;
    padding-bottom: 4rem;

    .our-staff-title {
        font-size: 2.5rem;
        font-weight: 400;
        margin-bottom: 1rem;
        text-transform: capitalize;
        color: $purple-color;
    }

    .our-staff-text {
        font-size: 1rem;
        margin-bottom: 2rem;
    }

    .divider-thumb {
        margin: 0 auto;
        width: 100px;
    }
}

.our-staff-row {
    display: flex;
    align-items: center;
    gap: 3rem;
    margin-bottom: 4rem;

    .our-staff-subtitle {
        flex-basis: 50%;
        font-size: 1.5rem;
        color: $purple-color;
        font-weight: 400;
    }

    .our-staff-subtext {
        flex-basis: 50%;
    }
}
</style>