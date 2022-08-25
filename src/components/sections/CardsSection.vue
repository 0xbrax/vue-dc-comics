<template>
    <section>
        <div class="container up-case">
            <div class="button alt-btn spec-btn">
                Current series
            </div>

            <div class="cards-container flex wrap">
                <DcSingleCard class="card" v-for="(card, cardIndex) in cardsDcComics" :key="cardIndex" :DcThumb="card.thumb" :DcSeries="card.series" />
            </div>

            <div class="flex just-sp-ctr">
                <div class="button alt-btn">
                Load more
            </div>
            </div>
        </div>
    </section>
</template>

<script>
import DcCards from '@/assets/data/dc-comics.json'
import DcSingleCard from '@/components/elements/DcSingleCard.vue'


export default {
    name: 'CardsSection',
    components: {
        DcSingleCard
    },
    data() {
        return {
            cardsDcComics: DcCards
        }
    }
}
</script>

<style scoped lang="scss">
    @import '@/style/common.scss';
    @import '@/style/utility.scss';


    section {
        background-color: $black-variant;
        color: #ffffff;
    }

    .container {
        position: relative;
        padding: 20px;
    }

    .card {
        width: calc(100% / 6);
        padding: 20px 10px;
        font-size: 14px;
    }

    .spec-btn {
        position: absolute;
        left: 0;
        top: -19px;
    }
</style>