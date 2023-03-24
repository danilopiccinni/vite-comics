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
            <img src="/img/dc-logo-bg.png" alt="">
        </div>

    </footer>
</template>

<style scoped lang="scss">

    footer {
        display: flex;
        justify-content: space-between;


        padding: 25px 100px;

        background-image: url(/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;


        .footer-sx {
            display: flex;
            gap: 50px;
        }
        .column {
            display: flex;
            flex-direction: column;

            span {
                text-transform: uppercase;
                color: white;
                font-size: 15px;
            }

            li {
                color: #959595;
                font-size: 10px;
            }

        }

        .logo { 

            img {
                width: 200px;
            }

        }
    }

</style>