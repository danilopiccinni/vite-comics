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
    <div class="container">
        <div class="section-sx">
            <button>SIGN-UP NOW!</button>
        </div>
        
        <div class="section-dx">
            <span>FOLLOW US</span>
            <ul>
                <li v-for="link in links">
                    <img :src='link' alt="">
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
            button {
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

            span {
                color: #0085ff;
                font-weight: bold;
            }

            ul {
                display: flex;
                gap: 20px;
            }
        }


    }


</style>