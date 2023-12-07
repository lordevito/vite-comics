<script>
// IMPORTO I SOTTOCOMPONENTI 
import Header from './components/header/Header.vue';
import Main from './components/main/MainMenu.vue';
import Footer from './components/footer/Footer.vue';
// DICHIARO COSA VOGLIO ESPORTARE 
export default {
  components: {
    Header,
    Main,
    Footer
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
  <div class="body">
      <header>
          <Header></Header>
      </header>

      <main>
          <Main></Main>
      </main>

      <footer>
          <Footer></Footer>
      </footer>

  </div>
</template>

<!-- SCSS  -->
<style lang="scss">
footer {
    background-image: url(img/background/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}
</style>
