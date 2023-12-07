<!-- JS  -->
<script>
// DICHIARO COSA VOGLIO ESPORTARE 
export default {
    // STRUTTURA CLASSICA DI VUE 
    data() {
        return {
            menu: [
                {
                    logo: 'img/icons/buy-comics-digital-comics.png',
                    text: 'Digital Comics',
                    link: '#'
                },
                {
                    logo: 'img/icons/buy-comics-merchandise.png',
                    text: 'Dc mechandise',
                    link: '#'
                },
                {
                    logo: 'img/icons/buy-comics-subscriptions.png',
                    text: 'subiscription',
                    link: '#'
                },
                {
                    logo: 'img/icons/buy-comics-shop-locator.png',
                    text: 'comics shop locator',
                    link: '#'
                },
                {
                    logo: 'img/icons/buy-dc-power-visa.svg',
                    text: 'dc power visa',
                    link: '#'
                },
            ]
        }
    }
}
</script>

<!-- HTML  -->
<template>
    <nav class="container">
        <ul>
            <li v-for="element in menu">
                <a class="menu" href="">
                    <div class="imgContainer"><img :src="element.logo" alt=""></div>
                    <div class="text">{{ element.text }}</div>
                </a>
            </li>
        </ul>
    </nav>
</template>

<!-- SCSS  -->
<style lang="scss" scoped >
@use 'src/styles/Variables.scss' as *;

.container {
    background-color: $my-blu;
    ;

    ul {
        display: flex;
        max-width: $my-container-max-width;
        margin: auto;
        justify-content: space-around;
        align-items: center;


        li .menu {
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 50px 5px;

            .imgContainer {
                height: 60px;
                width: 60px;
            }

            img {
                width: 100%;
                height: 100%;
                object-fit: contain;
            }

            .text {
                text-transform: uppercase;
                color: $my-white;
                padding-left: 20px;
            }


            &:hover {
                background-color: $my-secondary-blu;
            }
        }
    }
}
</style>