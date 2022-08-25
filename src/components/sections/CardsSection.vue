<template>
    <section>
        <div class="container">


            <div class="cards-container flex wrap">
                <DcSingleCard class="card" v-for="(card, cardIndex) in cardsDcComics" :key="cardIndex" :DcThumb="card.thumb" :DcSeries="card.series" />
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

    section {
        background-color: $black-variant;
        color: #ffffff;
    }

    .card {
        width: calc(100% / 6);
    }
</style>