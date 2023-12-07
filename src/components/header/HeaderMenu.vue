<!-- JS  -->
<script>
// DICHIARO COSA VOGLIO ESPORTARE 
export default {
    // STRUTTURA CLASSICA DI VUE 
    data() {
        return {
            menu: [
                {
                    text: 'Characters',
                    link: '#',
                    target: '_self'
                },
                {
                    text: 'Comics',
                    link: '#',
                    target: '_self'
                },
                {
                    text: 'Movies',
                    link: '#',
                    target: '_self'
                },
                {
                    text: 'TV',
                    link: '#',
                    target: '_self'
                },
                {
                    text: 'Games',
                    link: '#',
                    target: '_self'
                },
                {
                    text: 'Collectibles',
                    link: '#',
                    target: '_self'
                },
                {
                    text: 'Videos',
                    link: '#',
                    target: '_self'
                },
                {
                    text: 'Fans',
                    link: '#',
                    target: '_self'
                },
                {
                    text: 'News',
                    link: '#',
                    target: '_self'
                },
                {
                    text: 'Shop',
                    link: '#',
                    target: '_self'
                },
            ]
        }
    }
}
</script>

<!-- HTML  -->
<template>
    <nav>
        <ul>
            <li v-for="element in menu"><a :href="element.link" :target="element.target">{{ element.text }}</a></li>
        </ul>
    </nav>
</template>

<!-- SCSS  -->
<style lang="scss" scoped >
@use 'src/styles/Variables.scss' as *;

nav {
    ul {
        display: flex;

        li {
            text-transform: uppercase;
            display: inline-block;
            padding: 50px 20px;

            &:hover {
                cursor: pointer;
                background: linear-gradient(180deg, $my-white 95%, $my-blu 5%);
            }

            &:hover a {
                color: $my-blu;
            }
        }
    }
}
</style>