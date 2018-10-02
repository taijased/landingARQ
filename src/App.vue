<template>
  <!-- <div id="app"> -->
    <app-index></app-index>
  <!-- </div> -->
</template>

<script>
import AppIndex from "./components/Index";

export default {
  components: {
    AppIndex
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
@font-face {
  font-family: TT Norms Regular;
  src: url("../src/assets/fonts/TT_Norms/TTNorms-Regular.otf")
    format("opentype");
}
@font-face {
  font-family: TT Norms Medium;
  src: url("../src/assets/fonts/TT_Norms/TTNorms-Medium.otf") format("opentype");
}
@font-face {
  font-family: Avenir Next Cyr Demi;
  src: url("../src/assets/fonts/AvenirNextCyr/AvenirNextCyr-Demi.woff")
    format("woff");
}

body {
  height: 100%;
  width: 100%;
  position: relative;
  overflow: hidden;
}

</style>
