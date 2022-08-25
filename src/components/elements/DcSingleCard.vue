<template>
    <div>
        <div class="img-wrapper">
            <img :src="DcThumb" :alt="DcThumb">
        </div>
        <p>{{DcSeries}}</p>
    </div>
</template>

<script>
export default {
    name: 'DcSingleCard',
    props: {
        DcThumb: String,
        DcSeries: String
    }
}
</script>

<style scoped lang="scss">
    @import '@/style/common.scss';

    .img-wrapper {
        width: 100%;
        aspect-ratio: 1 / 1;
        overflow: hidden;
    }

    img {
        object-fit: contain;
    }

    p {
        margin-top: 10px
    }
</style>