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
                ],

                activeIndex: 0,
            }
        }
    }
</script>

<template>

    <nav>

        <div class="logo">
            <img :src="logo" alt="">
        </div>

        <div>
            <ul>
                <li v-for="(link , index) in links" @click="activeIndex=index" :class=" index == activeIndex ? 'active' : ''">
                    {{ link }}
                </li>
            </ul>
        </div>

    </nav>


</template>

<style scoped lang="scss">

    .active::before {
        content: "";
        width: 50%;
        height: 5px;
        background-color: #0282f9;

        position: absolute;
        bottom: 3px;
        right: 50%;
        translate: 50% 50%;
                    
                }
    

    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding-left: 100px;
        padding-right: 100px;

        img {

            width: 80px;

            &:hover {
                cursor: pointer;
            }
        }

        ul {
            
            display: flex;
            flex-wrap: wrap;
            
            li {
                font-weight: bold;
                text-transform: uppercase;
                padding: 50px 15px;
                position: relative;

                &:hover{
                    background-color: #0282f93d;
                    cursor: pointer;
                }
            }
        }
        
    }

</style>