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

    <div class="container">

        <ul>
            <li v-for="link in links">
                <div>
                    <img :src="link.image" alt="">
                    <span>{{ link.title }}</span>   
                </div>
            </li>
        </ul>

    </div>

</template>

<style scoped lang="scss">

    .container {
        padding: 25px 100px;

        background-color: #0282f9;
    }

    ul {
        display: flex;
        align-items: center;
        justify-content: space-around;
        
        div {
            display: flex;
            align-items: center;
            gap: 12px;

            span {
                color: white;
            }

            img {
                max-width: 50%;
                max-height: 50px;
            }
        }
    }
</style>