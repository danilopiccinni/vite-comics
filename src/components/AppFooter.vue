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
    <footer>
        <div class="footer-sx">
            
            <div v-for="column in columns" class="column">
                <span>{{ column.head }}</span>
                <ul>
                    <li v-for="link in column.links">
                        {{  link }}
                    </li>
                </ul>
    
            </div>

        </div>

        <div class="logo">
            <!-- <img src="/img/dc-logo-bg.png" alt=""> -->
        </div>

    </footer>
</template>

<style scoped lang="scss">

    footer {
        display: flex;
        justify-content: space-between;

        height: 300px;


        padding: 0px 100px;

        background-image: url(/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;


        .footer-sx {
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;
            gap: 10px;
            padding: 25px 0;
        }
        .column {
            display: flex;
            flex-direction: column;
            margin-right: 10px;


            span {
                text-transform: uppercase;
                color: white;
                font-size: 15px;
                margin-bottom: 10px;

            }

            li {
                color: #959595;
                font-size: 10px;

            }

        }

        .logo { 
            width: 600px;
            height: 100%;
            background-image: url(/img/dc-logo-bg.png);
            background-repeat: no-repeat;
            background-position: center;
            background-size: 80%;


            img {
                width: 500px;


            }

        }
    }

</style>