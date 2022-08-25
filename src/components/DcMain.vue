<template>
    <main>
        <DcJumbo />

        <div class="container">
            
        </div>
    </main>
</template>

<script>
import DcJumbo from '../components/sections/DcJumbo.vue'
import DCCards from '../assets/data/dc-comics.json'

export default {
    name: 'DcMain',
    components: {
        DcJumbo
    },
    data() {
        return {
            dcComicsCard: DCCards
        }
    }
}
</script>

<style scoped lang="scss">
    @import '../style/common.scss';


    main {
        background-color: $black-variant;
        color: #ffffff;
    }
</style>