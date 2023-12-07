<!-- JS  -->
<script>
// IMPORTO I COMPONENTI  
import FooterButton from './FooterButton.vue';
import FooterSocial from './FooterSocial.vue';
// DICHIARO COSA VOGLIO ESPORTARE 
export default {
    // DICHIARO I COMPONENTI CHE VOGLIO UTILIZZARE 
    components: {
        FooterButton,
        FooterSocial
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
            <div class="button">
                <FooterButton></FooterButton>
            </div>
            <div class="social">
                <FooterSocial></FooterSocial>
            </div>
        </div>
    </div>
</template>

<!-- SCSS  -->
<style lang="scss" scoped >
@use 'src/styles/Variables.scss' as *;

.container {
    max-width: $my-container-max-width;
    margin: auto;

    .content {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 30px;
    }
}
</style>