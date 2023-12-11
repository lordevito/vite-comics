<!-- JS  -->
<script>
// DICHIARO COSA VOGLIO ESPORTARE 
export default {
    // DICIAMO QUALI SARANNO I DATI DINAMICI 
    props: {
        image: String,
        title: String,
        link: String
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
    <div class="card">
        <div class="img">
            <img :src="image" :alt="title">
        </div>
        <div class="text">{{ title }}</div>
    </div>
</template>

<!-- SCSS  -->
<style lang="scss" scoped >
.card:hover {
    cursor: pointer;
    text-decoration: underline;

    img {
        opacity: 0.5;
    }
}
</style>