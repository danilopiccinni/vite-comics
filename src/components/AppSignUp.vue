<script>

    export default {
        data() {
            return {

                links : [
                    '/img/footer-facebook.png',
                    '/img/footer-twitter.png',
                    '/img/footer-youtube.png',
                    '/img/footer-pinterest.png',
                    '/img/footer-periscope.png',
                ]
            }
        }
    }
</script>

<template>
    <!-- contenitore intera sezione -->
    <div class="container">
        <!-- contenitore parte sinistra -->
        <div class="section-sx">
            <!-- bottone 'sign-up' che serve all'utente ad accedere -->
            <button class="button-sign-up">SIGN-UP NOW!</button>
        </div>
        <!-- contenitore parte destra -->
        <div class="section-dx">
            <!-- 'titolo' da visualizzare affianco alla lista dei link dedicati ai social -->
            <span class="title-social">FOLLOW US</span>
            <!-- lista dei link social -->
            <ul class="social-list">
                <!-- ciclo v-for che crea un 'li' per ogni link presente nell'array di link (links) -->
                <li v-for="link in links" class="link">
                    <!-- immagine del link corrente --- src gestito tramite vue (:src) assegnando il link corrispondente al link corrente -->
                    <img :src='link' alt="" class="image-link">
                </li>
            </ul>
        </div>   
    </div>
</template>

<style scoped lang="scss">

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;

        padding: 25px 100px;

        background-color: #303030;
        .section-sx {
            .button-sign-up {
                border: 2px solid #0085ff;
                padding: 0.5em;
                background-color: transparent;
                color: white;
                font-weight: bold;
            }
        }
        .section-dx{
            display: flex;
            align-items: center;
            gap: 50px;
            .title-social {
                color: #0085ff;
                font-weight: bold;
            }
            .social-list {
                display: flex;
                gap: 20px;
            }
        }
    }
</style>