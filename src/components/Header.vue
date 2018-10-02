<template>
  <div class="container fade-in-top">
    <div class="header-logo">
      <a href="/" ><img src="../assets/img/arq-logo.png"></a>
      <div class="header-logo-title noselect">arq</div>
    </div>
    <div class="internationalization noselect">
      <div @click="setLocalization()">{{$t("internationalization.title")}}</div>
    </div>
  </div>
</template>
<script>
import IconBase from "./IconBase";

export default {
  components: {
    IconBase
  },
  methods: {
    setLocalization() {
      this.$i18n.locale = this.$i18n.locale === "ru" ? "en" : "ru";
    }
  }
};
</script>

<style lang="less" scoped>
@ml: 20px;
@xs: ~"(max-width:576px)";
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  color: rgba(0, 0, 0, 1);
  font-family: TT Norms Medium;
  padding: 0 8%;
  .header-logo {
    display: flex;
    flex-direction: row;
    align-items: center;
    cursor: pointer;
    img {
      width: 50px;
      height: 50px;
    }
    .header-logo-title {
      margin-left: @ml;
      text-transform: uppercase;
      font-family: Avenir Next Cyr Demi;
      font-size: 22px;
      @media @xs {
        font-size: 20px;
      }
    }
  }
  .internationalization {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    color: rgba(0, 0, 0, 0.3);
    transition: color 0.6s ease-in-out;
    font-size: 14px;
  }
  .internationalization:hover {
    color: rgba(0, 0, 0, 1);
    transition: color 0.6s ease-in-out;
  }
  .noselect {
    -moz-user-select: none;
    -webkit-user-select: none;
    -ms-user-select: none;
    -o-user-select: none;
    user-select: none;
  }
}
.fade-in-top {
  -webkit-animation: fade-in-top 1.6s cubic-bezier(0.39, 0.575, 0.565, 1) both;
  animation: fade-in-top 1.6s cubic-bezier(0.39, 0.575, 0.565, 1) both;
}
@-webkit-keyframes fade-in-top {
  0% {
    -webkit-transform: translateY(-50px);
    transform: translateY(-50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    opacity: 1;
  }
}
@keyframes fade-in-top {
  0% {
    -webkit-transform: translateY(-50px);
    transform: translateY(-50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    opacity: 1;
  }
}
</style>
