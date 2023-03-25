<script>
    export default {
        data() {
            return {
                links : [
                    {
                        image : '/img/buy-comics-digital-comics.png',
                        title : 'digital comics'
                    },
                    {
                        image : '/img/buy-comics-merchandise.png',
                        title : 'dc merchandise'
                    },
                    {
                        image : '/img/buy-comics-subscriptions.png',
                        title : 'subscription'
                    },
                    {
                        image : '/img/buy-comics-shop-locator.png',
                        title : 'comic shop locator'
                    },
                    {
                        image : '/img/buy-dc-power-visa.png',
                        title : 'dc power visa'
                    },

                ]
            }
        }
    }
</script>


<template>
    <!-- contenitore generale di AppBuy -->
    <div class="container">
        <!-- listanon ordinata dei link -->
        <ul class="link-list">
            <!-- list item generati con un v-for per visualizzare ogni oggetto dell'array 'links' presente in 'data' -->
            <li v-for="link in links" class="link">
                <!-- contenitore interno che racchiude l'insieme dei valori riferiti a ogni oggetto dell'array -->
                <div class="int-cont-link">
                    <!-- immagine da visualizzare dell'oggetto corrente (link)---(src specificato tramite vue (:src) che prende il valore 'image' del link(oggetto) corrente -->
                    <img :src="link.image" :alt="`immagine ${link.title}`"  class="link-image">
                    <!-- titolo da visualizzare dell'oggetto corrente (link)---innerhtml del tag riempito tramite vue che prende il valore 'title' del link(oggetto) corrente -->
                    <span class="title-link">{{ link.title }}</span>   
                </div>
            </li>
        </ul>

    </div>

</template>

<style scoped lang="scss">
    .container {
        padding: 25px 100px;
        background-color: #0282f9;
        .link-list {
            display: flex;
            align-items: center;
            justify-content: space-around;
            .int-cont-link {
                display: flex;
                align-items: center;
                gap: 12px;
                .title-link {
                    color: white;
                }
                .link-image {
                    max-width: 50%;
                    max-height: 50px;
                }
            }
        }
    }
</style>
    
    
    
