<script>
    import AppComicBook from "./AppComicBook.vue"

    export default {
        data() {
            return {

                comicBooks :[
                    {
                        "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                        "price": "$19.99",
                        "series": "Action Comics",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                        "price": "$3.99",
                        "series": "American Vampire 1976",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                        "price": "$16.99",
                        "series": "Aquaman",
                        "type": "graphic novel"
                    },
                    {
                        "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                        "price": "$2.99",
                        "series": "Batgirl",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                        "price": "$3.99",
                        "series": "Batman",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                        "price": "$2.99",
                        "series": "Batman Beyond",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                        "price": "$3.99",
                        "series": "Batman/Superman",
                        "type": "comic book"
                    },
                    {
                      "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                      "price": "$4.99",
                      "series": "Batman/Superman Annual",
                      "type": "comic book"
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                        "price": "$5.99",
                        "series": "Batman: The Joker War Zone",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                        "price": "$6.99",
                        "series": "Batman: Three Jokers",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                        "price": "$4.99",
                        "series": "Batman: White Knight Presents: Harley Quinn",
                        "type": "comic book"
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                        "price": "$16.99",
                        "series": "Catwoman",
                        "type": "graphic novel"
                    }
                ]
            }
        },
            
        components : {
            AppComicBook,
        }
    }

</script>

<template>
    <!-- contenitore generale  -->
    <div class="general-container">
        <!-- contenitore jumbotron che contiene l'immagine in background da visualizzare -->
        <div class="jumbotron">
            <!-- lasciato vuoto perche il background viene gestito nello style -->
        </div>

        <!-- contenitore dedicato alla visualizazzione delle varie card(fumetti/riviste)  -->
        <div class="container-comic-books">
            <!-- bottone delle serie correnti -- da visualizzare in posizione assoluta  -->
            <button class="current-series-button">current series</button>

            <!-- tramite il v-for di vue crea per ogni oggetto dell'array 'comicBook' facendo riferimento all'array intero di 'comicBooks' -->
                                                        <!-- il ':title' passa alla proprietà dedicata al titolo l'attributo 'series' del fumetto corrente -->
                                                                                <!-- il :image passa alla proprietà dedicata l'attributo 'thumb' del fumetto corrente -->
            <AppComicBook v-for="comicBook in comicBooks" :title="comicBook.series" :image="comicBook.thumb"></AppComicBook>
    
        </div>
        <!-- bottone che serve a caricare ulteriori fumetti da visualizzare -->
        <button class="load-more-button">load more</button>

    </div>

</template>

<style scoped lang="scss">
    .general-container {
        display: flex;
        flex-direction: column;
        background-color: #1c1c1c;
        padding-bottom: 20px;

        .jumbotron {
            height: 400px;
            background-image: url(/img/jumbotron.jpg);
            background-position: top;
            background-repeat: no-repeat;
        }

        .container-comic-books {
            display: flex;
            flex-direction: row;
            align-items: center;
            flex-wrap: wrap;
            gap: 20px;
    
            align-items: center;
            padding: 40px 100px;
    
            position: relative;
    
    
            .current-series-button {
                position: absolute ;
                top: 0;
                transform: translateY(-50%);
    
                text-transform: uppercase;
                padding: 12px 25px;
                background-color: #1e76e2;
            }
    
        }
    
        .load-more-button {
            align-self: center;
            text-transform: uppercase;
            padding: 12px 25px;
            background-color: #1e76e2;
    
        }
    }

</style>