<!-- JS  -->
<script>
// DICHIARO COSA VOGLIO ESPORTARE 
export default {
    // STRUTTURA CLASSICA DI VUE 
    data() {
        return {

        }
    }
}
</script>

<!-- HTML  -->
<template>
    <div class="button">
        <a href="#">SIGN-UP NOW!</a>
    </div>
</template>

<!-- SCSS  -->
<style lang="scss" scoped >
@use 'src/styles/Variables.scss' as *;

.button {
    padding: 12px;
    border: 2px solid $my-blu;

    a {
        color: $my-white;
    }

    &:hover {
        cursor: pointer;
        background-color: $my-blu;
    }
}
</style>