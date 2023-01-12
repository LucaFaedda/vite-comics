<script>
    export default {
        name: 'CardDc',
        props:{
            fumetto: Object,
        }
    }
</script>
<template lang="">
    <div class="card-container">
        <div class="image-container">
            <img :src="fumetto.thumb">
        </div>
        <h4 class="card-title">{{fumetto.series}}</h4>
    </div>
</template>
<style lang="scss" scoped>
    .card-container{
        display: flex;
        flex-wrap: wrap;
        width: calc(100% / 6);
    }
</style>