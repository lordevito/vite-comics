<!-- JS  -->
<script>
// IMPORTO I SOTTOCOMPONENTI 
import MainMenu from './MainMenu.vue';
import MainSectionCards from './MainSectionCards.vue';
// DICHIARO COSA VOGLIO ESPORTARE 
export default {
    components: {
        MainMenu,
        MainSectionCards
    },
    // STRUTTURA CLASSICA DI VUE 
    data() {
        return {

        };
    },
};
</script>

<!-- HTML  -->
<template>
    <section class="section">
        <MainSectionCards></MainSectionCards>
    </section>
    <section class="section MainMenu">
        <MainMenu></MainMenu>
    </section>
</template>

<!-- SCSS  -->
<style lang="scss" scoped ></style>