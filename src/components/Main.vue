
<template>
  <div class="wrapper">
    <header>
     <app-header></app-header>
    </header>
    <main>
      <custom-swiper></custom-swiper>
    </main>
    <footer>
      <app-footer></app-footer>
    </footer>
  </div>
</template>

<script>
import AppHeader from "./Header";
import AppFooter from "./Footer";
import CustomSwiper from "./CustomSwiper";

export default {
  components: {
    AppHeader,
    AppFooter,
    CustomSwiper
  }
};
</script>

<style lang="less">
.wrapper {
  display: grid;
  height: 100vh;
  grid-template-rows: 15vh 85vh;
  grid-template-columns: 50vw 50vw;
  overflow: hidden;
  header {
    grid-row: 1;
    grid-column: ~"1 / 3";
    display: flex;
    flex-direction: row;
    align-items: center;
  }
  main {
    grid-row: 2;
    grid-column:  ~"1 / 3";
    .container > .left-bar{
      height: 75vh;
    }
  }
  footer {
    position: absolute;
    bottom: 0;
    left: 8%;
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    z-index: 999;
    height: 10vh;
  }
}
</style>
