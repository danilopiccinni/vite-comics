<script>

    export default {
        data() {
            return {
                logo : '/img/dc-logo.png',
                links : [
                    'characters',
                    'comics',
                    'movies',
                    'tv',
                    'games',
                    'collectibles',
                    'videos',
                    'fans',
                    'news',
                    'shop',
                ]
            }
        }
    }
</script>

<template>

    <nav>

        <div>
            <img :src="logo" alt="">
        </div>

        <div>
            <ul>
                <li v-for="link in links">
                    {{ link }}
                </li>
            </ul>
        </div>

    </nav>


</template>

<style scoped lang="scss">

    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding-top: 25px;
        padding-bottom: 25px;

        ul {
            
            display: flex;
            
            li {
                text-transform: uppercase;
                padding: 15px 15px;
            }
        }
        
    }

</style>