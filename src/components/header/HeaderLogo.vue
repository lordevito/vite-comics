<!-- JS  -->
<script>
// DICHIARO COSA VOGLIO ESPORTARE 
export default {
    // STRUTTURA CLASSICA DI VUE 
    data() {
        return {
            logoSrc: "img/logos/dc-logo.png",
            logoAlt: "CD",
            logoLink: "#"
        }
    }
}
</script>

<!-- HTML  -->
<template>
    <div>
        <a :href="logoLink"><img :src="logoSrc" :alt="logoAlt"></a>
    </div>
</template>

<!-- SCSS  -->
<style lang="scss" scoped >
div {
    height: 100px;
    width: 100px;

    img {
        width: 100%;
    }
}
</style>