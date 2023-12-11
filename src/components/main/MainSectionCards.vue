<!-- JS  -->
<script>
import Card from './Card.vue';
import MainButton from './MainButton.vue'
// DICHIARO COSA VOGLIO ESPORTARE 
export default {
    // DICHIARO I COMPONENTI CHE VOGLIO UTILIZZARE 
    components: {
        Card,
        MainButton,
    },
    // STRUTTURA CLASSICA DI VUE 
    data() {
        return {
            cardsData: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                },
            ],
        };
    },
};
</script>

<!-- HTML  -->
<template>
    <div class="sectionContainer">
        <div class="content">
            <h3 class="title">CURRENT SERIES</h3>
            <div class="cards">
                <card v-for="card in cardsData" :image="card.thumb" :title="card.series" />
            </div>
            <div class="loadMore">
                <MainButton></MainButton>
            </div>
        </div>
    </div>
</template>

<!-- SCSS  -->
<style lang="scss" scoped >
@use 'src/styles/Variables.scss' as *;

.sectionContainer {
    color: $my-white;
    background-color: $my-black;


    .content {
        max-width: $my-container-max-width;
        margin: auto;
        padding: 50px 0;
        position: relative;

        .title {
            position: absolute;
            top: -25px;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 50px;
            width: 250px;
            font-size: 24px;
            background-color: $my-blu;
        }

        .cards {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            margin: auto;

            :deep(.card) {
                margin: 10px;
                flex-basis: calc(100% / 6 - 20px);
                display: flex;
                flex-direction: column;

                .text {
                    padding-top: 5px;
                    width: 100%;
                }
            }
        }

        .loadMore {
            display: flex;
            justify-content: center;
        }
    }
}
</style>