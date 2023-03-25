<script>

    export default {
        data() {
            return {
                
                columns :[
                    {
                        head : 'dc comics',

                        links : [
                            'Characters',
                            'Comics',
                            'Movies',
                            'TV',
                            'Games',
                            'Videos',
                            'News',
                        ]
                    },

                    {
                        head : 'shop',

                        links : [
                            'Shop DC',
                            'Shop DC Collectibles',
                        ]
                    },

                    {
                        head : 'dc',

                        links : [
                            'Therms Of Use',
                            'Privacy policy (New)',
                            'Ad Choices',
                            'Advertising',
                            'Jobs',
                            'Subscriptions',
                            'Talent Workshop',
                            'CPSC Certificares',
                            'Ratings',
                            'Shop Help',
                            'Contact Us',
                        ]
                    },

                    {
                        head : 'sites',

                        links : [
                            'DC',
                            'MAD Magazine',
                            'DC Kids',
                            'DC Universe',
                            'DC Power Visa',
                        ]
                    }
                ] 
            }
        }
    }
</script>

<template>
    <!-- footer -->
    <footer class="footer">
        <!-- contenitore sinistro del footer -->
        <div class="cont-links">
            <!-- contenitore creato con il v-for per ogni oggetto('column') nell'array di 'columns'  -->
            <div v-for="column in columns" class="column">
                <!-- titolo dell'oggetto corrente ('column') -->
                <span class="link-title">{{ column.head }}</span>
                <!-- lista dei link riferita all'oggetto corrente -->
                <ul class="link-list">
                    <!-- 'li' creato con il v-for che cicla l'array di link presente in ogni oggetto ('column')  presente in 'columns'(array primario che contiene i vari oggetti)-->
                    <li v-for="link in column.links" class="link">
                        <!-- visualizza quindi il link corrente -->
                        {{  link }}
                    </li>
                </ul>
            </div>
        </div>
        
        <!-- contenitore 'vuoto' creato per usare un background da visualizzare in modo particolare(gestita per lo piu' tramite lo style) -->
        <div class="logo">
            <!-- lasciato vuoto perche serve la visualizazzione riguarda solo il background -->
        </div>
    </footer>
</template>

<style scoped lang="scss">

    .footer {
        display: flex;
        justify-content: space-between;

        height: 400px;

        padding: 0 100px;

        background-image: url(/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;


        .cont-links {
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;
            gap: 10px;

            padding: 25px 0;
            .column {
                display: flex;
                flex-direction: column;
                margin-right: 10px;
                .link-title {
                    text-transform: uppercase;
                    color: white;
                    font-size: 20px;
                    font-weight: bold;
                    margin-bottom: 10px;
                }
                .link-list {
                    display: flex;
                    flex-direction: column;
                    gap: 3px;
                    margin-bottom: 10px;                
                    .link {
                        color: #959595;
                        font-size: 15px;
                    }
                }
            }
        }
        .logo { 
            width: 600px;
            height: 100%;
            background-image: url(/img/dc-logo-bg.png);
            background-repeat: no-repeat;
            background-position: center;
            background-size: 100%;
        }
    }

</style>