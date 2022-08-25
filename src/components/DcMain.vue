<template>
    <main>
        <DcJumbo />
        <CardsSection />
    </main>
</template>

<script>
import DcJumbo from '../components/sections/DcJumbo.vue'
import CardsSection from '../components/sections/CardsSection.vue'


export default {
    name: 'DcMain',
    components: {
        DcJumbo,
        CardsSection
    }
}
</script>

<style scoped lang="scss">
    @import '../style/common.scss';
</style>