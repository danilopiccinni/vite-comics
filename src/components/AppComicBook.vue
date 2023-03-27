<script>
    export default {
        data() {
            return{

            }
        },

        props : {
            image : String,
            title : String
        }
    }
</script>

<template>

    <div class="card">
        <img :src="image" alt="">
        <span> {{ title }} </span>
    </div>

</template>

<style scoped lang="scss">

    .card {
        display: flex;
        flex-flow: column nowrap;
        gap: 15px;

        width: calc(100% / 6 - 20px);
        height: 400px;
        padding: 10px;

        border: 1px solid white;

        img {
            width: 100%;
            height: 80%;
            border: 1px solid white;
        }

        span {
            text-transform: uppercase;
            color: white;
            font-weight: bold;
        }
    }

</style>