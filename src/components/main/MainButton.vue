<!-- JS  -->
<script>
// DICHIARO COSA VOGLIO ESPORTARE 
export default {
    // STRUTTURA CLASSICA DI VUE 
    data() {
        return {

        };
    },
};
</script>

<!-- HTML  -->
<template>
    <div class="button">
        LOAD MORE
    </div>
</template>

<!-- SCSS  -->
<style lang="scss" scoped >
@use 'src/styles/Variables.scss' as *;

.button {
    font-weight: bold;
    background-color: $my-blu;
    display: inline-block;
    padding: 20px 100px;

    &:hover {
        cursor: pointer;
        background-color: $my-secondary-blu;
    }
}
</style>