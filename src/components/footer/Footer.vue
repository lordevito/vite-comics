<!-- JS  -->
<script>
// IMPORTO I SOTTOCOMPONENTI 
import FooterLogo from './FooterLogo.vue';
import FooterMenu from './FooterMenu.vue';
import FooterEnd from './FooterEnd.vue';
// DICHIARO COSA VOGLIO ESPORTARE 
export default {
    components: {
        FooterLogo,
        FooterMenu,
        FooterEnd,
    },
    // STRUTTURA CLASSICA DI VUE 
    data() {
        return {

        }
    }
}
</script>

<!-- HTML  -->
<template>
    <div class="container">
        <div class="content">
            <div class="menu">
                <FooterMenu></FooterMenu>
            </div>

            <div class="logo">
                <FooterLogo></FooterLogo>
            </div>
        </div>
        <div class="contacts">
            <FooterEnd></FooterEnd>
        </div>
    </div>
</template>

<!-- SCSS  -->
<style lang="scss" scoped >
@use 'src/styles/Variables.scss' as *;

.container {
    .content {
        max-width: $my-container-max-width;
        margin: auto;
        display: flex;
        position: relative;
        overflow: hidden;
        padding: 30px 0;

        .menu {
            z-index: 1;
        }

        .logo {
            position: absolute;
            right: 0;
            top: -40px;
        }
    }

    .contacts {
        background-color: $my-grey;
    }
}
</style>