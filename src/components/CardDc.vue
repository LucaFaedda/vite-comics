<script>
    export default {
        name: 'CardDc',
        props:{
            fumetto: Object,
        }
    }
</script>
<template lang="">
    <div class="card">
            <div class="image-container">
                <img :src="fumetto.thumb">
            </div>
            <h5 class="card-title">{{fumetto.series}}</h5>
    </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partials/variabiles' as *;

        .card{
            width: calc(100% / 6 - 6px);
            margin: 3px;
            .image-container{
                width: 250px;
                height: 250px;
                position: relative;
                overflow: hidden;
                img{
                    position: absolute;
                    width: 70%;
                    left:0;
                    top: 50%;
                    transform: translateY(-20%);
                }
            }
            .card-title{
                color: $colorwhite;
                margin-top:1rem;
            }
        }

</style>