<!-- JS  -->
<script>
// IMPORTO I SOTTOCOMPONENTI 
import HeaderLogo from './HeaderLogo.vue';
import HeaderMenu from './HeaderMenu.vue';
// DICHIARO COSA VOGLIO ESPORTARE 
export default {
    components: {
        HeaderLogo,
        HeaderMenu,
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
    <div class="header">
        <div class="headerContainer">
            <div class="headerLogo">
                <HeaderLogo></HeaderLogo>
            </div>
            <div class="headerNav">
                <HeaderMenu></HeaderMenu>
            </div>
        </div>
    </div>
</template>

<!-- SCSS  -->
<style lang="scss" scoped >
@use 'src/styles/Variables.scss' as *;

.header {
    background-color: $my-white;

    .headerContainer {
        margin: 0 auto;
        max-width: $my-container-max-width;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

}
</style>