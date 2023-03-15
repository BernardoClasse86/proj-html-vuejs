<script>
export default {
    data() {
        return {
            ourNumbers: [
                {
                    ourNum: '507',
                    ourNumTitle: 'Our Pupils',
                    ourNumText: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit.'
                },
                {
                    ourNum: '235',
                    ourNumTitle: 'Teaching Hours',
                    ourNumText: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit.'
                },
                {
                    ourNum: '100%',
                    ourNumTitle: 'Satisfied Parents',
                    ourNumText: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit.'
                },
                {
                    ourNum: '1050',
                    ourNumTitle: 'Meals Per Year',
                    ourNumText: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit.'
                },
            ]
        }
    }
}
</script>

<template>
    <div class="container">
        <ul class="row">
            <li class="column" v-for="ourNumber in ourNumbers">
                <h2 class="numb-num">{{ ourNumber.ourNum }}</h2>
                <h4 class="numb-title">{{ ourNumber.ourNumTitle }}</h4>
                <p class="numb-text">{{ ourNumber.ourNumText }}</p>
            </li>
        </ul>

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
    padding: 4rem 0;

    .row {
        text-align: center;
        gap: 4rem;
        color: white;
        margin-bottom: 3.75rem;

        .column {
            justify-content: center;
            gap: 1.5rem;

            .numb-num {
                width: 180px;
                height: 180px;
                margin: 0 auto;
                padding: 1rem;
                border: 1px solid;
                border-radius: 50%;
                display: flex;
                align-items: center;
                justify-content: center;
                font-size: 2.5rem;
                font-weight: 400;
            }

            .numb-title {
                font-weight: 400;
                font-size: 1.5rem;
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
            cursor: pointer;
            padding: 0.25rem 1rem;
        }

        .solid-select:hover {
            border: 2px solid rgba(255, 255, 255, 0.5);
        }
    }

}
</style>