<template>
  <div>
    <transition name="fade">
      <div class="present" v-if="!isOpen">
        <div class="present-logo" @click="isOpen = !isOpen">
          <icon-base></icon-base>
        </div>
        <div class="present-title noselect">
          <h1>arq</h1>
          <h6>{{$t("blind.description")}}</h6>
          <div class="internationalization" @click="setLocalization()">{{$t("internationalization.title")}}</div>
        </div>
      </div>
    </transition>
    <app-main v-if="isOpen"></app-main>
  </div>
</template>

<script>
import IconBase from "./IconBase";
import AppMain from './Main'
export default {
  data() {
    return {
      isOpen: true
    };
  },
  methods: {
    setLocalization () {
      this.$i18n.locale = (this.$i18n.locale === 'ru') ? 'en' : 'ru'
    }
  },
  components: {
    IconBase,
    AppMain
  }
};
</script>

<style lang="less" scoped>
@xs: ~'(max-width:576px)';
.present {
  height: 100vh;
  position: relative;
  overflow: hidden;
  .present-logo {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    cursor: pointer;
  }
  .present-title {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(20%, -15%);
    width: 300px;
    @media @xs {
      width: 150px;
      transform: translate(0, 0);
    }
    .internationalization {
      font-family: TT Norms Regular;
      color: rgba(0, 0, 0, 0.3);
      transition: color 0.3s ease-in-out;
      font-size: 18px;
      cursor: pointer;
    }
    .internationalization:hover {
      color: rgba(0, 0, 0, 1);
      transition: color 0.3s ease-in-out;
    }
    h1 {
      text-transform: uppercase;
      font-family: Avenir Next Cyr Demi;
      line-height: normal;
    }
    h6 {
      font-family: TT Norms Regular;
      margin: 12px 0;
    }
  }
  .noselect {
    -moz-user-select: none;
    -webkit-user-select: none;
    -ms-user-select: none;
    -o-user-select: none;
    user-select: none;
  }
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
h4 {
  font-family: TT Norms Medium;
  font-size: 24px;
  line-height: 30px;
}
h6 {
  font-family: TT Norms Regular;
  font-size: 18px;
  line-height: 20px;
}
</style>

