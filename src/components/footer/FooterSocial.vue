<!-- JS  -->
<script>
// DICHIARO COSA VOGLIO ESPORTARE 
export default {
    // STRUTTURA CLASSICA DI VUE 
    data() {
        return {
            links: [
                {
                    name: 'Facebook',
                    link: '#',
                    logo: 'img/sicons/footer-facebook.png',
                    target: '_blank'

                },
                {
                    name: 'Twitter',
                    link: '#',
                    logo: 'img/sicons/footer-twitter.png',
                    target: '_blank'

                },
                {
                    name: 'You-tube',
                    link: '#',
                    logo: 'img/sicons/footer-youtube.png',
                    target: '_blank'

                },
                {
                    name: 'Pinterest',
                    link: '#',
                    logo: 'img/sicons/footer-pinterest.png',
                    target: '_blank'

                },
                {
                    name: 'Periscope',
                    link: '#',
                    logo: 'img/sicons/footer-periscope.png',
                    target: '_blank'

                }
            ]
        }
    }
}
</script>

<!-- HTML  -->
<template>
    <div class="container">
        <h3>FOLLOW US</h3>
        <nav>
            <ul>
                <li v-for="link in links">
                    <a :href="link.link" :target="link.target">
                        <img :src="links.logo" :alt="link.name">
                    </a>
                </li>
            </ul>
        </nav>
    </div>
</template>

<!-- SCSS  -->
<style lang="scss" scoped >
@use 'src/styles/Variables.scss' as *;

.container {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;

    h3 {
        color: $my-blu;
    }

    ul {
        display: flex;
        justify-content: center;
        align-items: center;

        li {
            padding: 0 6px;
        }
    }
}
</style>