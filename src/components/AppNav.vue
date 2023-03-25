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

                activeIndex: null,
            }
        }
    }
</script>

<template>
    <!-- nav -->
    <nav class="nav-bar">
        <!-- contenitore del immagine 'logo' -->
        <div class="logo">
            <!-- logo---src gestita con vue (:src) che prende dal 'data' il link riferito all'immagine -->
            <img :src="logo" alt="" class="logo">
        </div>

        <!-- contenitore della lista dei link -->
        <div class="cont-list">
            <!-- lista non ordinata in cui ci saranno i link da visualizzare -->
            <ul class="link-list">
                <!-- link generati con un v-for che crea un 'li' per ogni 'link' presente nell'array di 'links' -->
                                                <!-- evento click su ogni 'li' (link) che sincornizza il valore di 'activeIndex' con il valore dell'index(ricavato dal v-for) del link in questione che viene cliccato-->
                                                                                    <!-- classe gestita tramite vue (:class) che assegna tramite un controllo ternario l'assegnazione della classe 'active' al link che ha il suo index uguale all'active index (quindi al momento del click) -->
                <li v-for="(link , index) in links" @click="activeIndex=index" :class=" index == activeIndex ? 'active' : ''" class="link">
                    <!-- visualizza tramite vue il link corrente -->
                    {{ link }}
                </li>
            </ul>
        </div>
    </nav>
</template>

<style scoped lang="scss">

    .nav-bar {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding-left: 100px;
        padding-right: 100px;

        .logo {
            width: 80px;

            &:hover {
                cursor: pointer;
            }
        }
        .link-list {
            display: flex;
            flex-wrap: wrap;
            .link {
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

</style>