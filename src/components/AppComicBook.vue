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
    <!-- contenitore dell'intera card -->
    <div class="card">
        <!-- immagine della card riferita al fumetto -- src interpolato con vue (:src) in cui viene assegnato la proprietà 'image' che a sua volta prende il valore in stringa dal documento padre 'AppContent.vue' -->
        <img :src="image" alt="" class="image-comic-book">
        <!-- titolo della card riferita al fumetto -- innerText interpolato con vue (tramite 'baffi') in cui viene assegnato la proprietà 'title' che a sua volta prende il valore in stringa dal documento padre 'AppContent.vue' -->
        <span class="title-comic-book"> {{ title }} </span>

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
        .image-comic-book {
            max-width: 100%;
            max-height: 80%;

        }
        .title-comic-book {
            text-transform: uppercase;
            color: white;
            font-weight: bold;
        }
    }

</style>