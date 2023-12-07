<!-- JS  -->
<script>
// DICHIARO COSA VOGLIO ESPORTARE 
export default {
    // STRUTTURA CLASSICA DI VUE 
    data() {
        return {
            menu: [
                {
                    sectionName: 'Dc comics',
                    content: [
                        {
                            text: 'Characters',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'Comics',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'Movies',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'TV',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'Games',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'Videos',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'News',
                            link: '#',
                            target: '_blank'
                        }
                    ]
                },
                {
                    sectionName: 'Shop',
                    content: [
                        {
                            text: 'Shop DC',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'Shop DC collectibles',
                            link: '#',
                            target: '_blank'
                        }
                    ]
                },
                {
                    sectionName: 'Dc comics',
                    content: [
                        {
                            text: 'Characters',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'Comics',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'Movies',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'TV',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'Games',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'Videos',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'News',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'TV',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'Games',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'Videos',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'News',
                            link: '#',
                            target: '_blank'
                        }
                    ]
                }, {
                    sectionName: 'Dc comics',
                    content: [
                        {
                            text: 'Characters',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'Comics',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'Movies',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'TV',
                            link: '#',
                            target: '_blank'
                        },
                        {
                            text: 'Games',
                            link: '#',
                            target: '_blank'
                        }
                    ]
                }
            ]
        }
    }
}
</script>

<!-- HTML  -->
<template>
    <div class="container">
        <nav>
            <ul v-for="element in menu">
                <li class="liHeader">{{ element.sectionName }}</li>
                <li class="lilinks" v-for="listItem in element.content"><a :href="listItem.link"
                        :target="listItem.target">{{ listItem.text }}</a>
                </li>
            </ul>
        </nav>
    </div>
</template>

<!-- SCSS  -->
<style lang="scss" scoped >
@use 'src/styles/Variables.scss' as *;

nav {
    color: $my-white;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    max-height: 500px;
    font-size: 23px;
    padding-top: 20px;
    padding-bottom: 40px;

    ul {
        padding: 20px;

        .liHeader {
            font-size: 23px;
            text-transform: uppercase;
            font-weight: bold;
            padding-bottom: 8px;
        }

        .lilinks a {
            font-size: 19px;
            color: $my-secondary-grey;

            &:hover {
                text-decoration: underline;
            }
        }
    }
}
</style>