<script>
import ProductCard from './ProductCard.vue';

export default {
    data() {
        return {
            comics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "prezzo": "$ 19,99",
                    "serie": "Fumetti d'azione",
                    "tipo": "fumetto"
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "prezzo": "$ 3,99",
                    "serie": "American Vampire 1976",
                    "tipo": "fumetto"
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "prezzo": "$ 16,99",
                    "serie": "Aquaman",
                    "tipo": "romanzo grafico"
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "prezzo": "$ 2,99",
                    "serie": "Batgirl",
                    "tipo": "fumetto"
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "prezzo": "$ 3,99",
                    "serie": "Batman",
                    "tipo": "fumetto"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "prezzo": "$ 2,99",
                    "serie": "Batman oltre",
                    "tipo": "fumetto"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "prezzo": "$ 3,99",
                    "serie": "Batman/Superman",
                    "tipo": "fumetto"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "prezzo": "$ 4,99",
                    "serie": "Annuario Batman/Superman",
                    "tipo": "fumetto"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "prezzo": "$ 5,99",
                    "serie": "Batman: The Joker War Zone",
                    "tipo": "fumetto"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "prezzo": "$ 6,99",
                    "serie": "Batman: Tre Joker",
                    "tipo": "fumetto"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "prezzo": "$ 4,99",
                    "serie": "Batman: Il Cavaliere Bianco presenta: Harley Quinn",
                    "tipo": "fumetto"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "prezzo": "$ 16,99",
                    "serie": "Catwoman",
                    "tipo": "romanzo grafico"
                }
            ]

        }
    },
    components: { ProductCard },

}
</script>

<template>
    
    <div class="jumbotron">
        <button>CURRENT SERIES</button>
    </div>
   
    <div class="wrapper">

        <div class="container">

            <div class="row">
                <div class="col" v-for="( item, index ) in comics" :key="index">
                    <ProductCard :title="item.serie" :image="item.thumb"/>
                </div>
            </div>

        </div>

    </div>

</template>


<style scoped lang="scss">
@use "../style/partials/variables" as *;


.jumbotron{
    background-image: url("../assets/img/jumbotron.jpg");
    

}
.wrapper {
    text-align: center;
    padding: 2rem;
    background-color: $black;

    .container {

        .row{
            display: flex;
            justify-content: center; 
            flex-direction: row;
            flex-wrap: wrap;
            

            .col{
                width: calc(100% / 6 - 20px );
                margin: 10px;

                h3 {
                  color: $white;
                  font-size: .8rem;
                }

            }

        }
      
        
    }

}
</style>