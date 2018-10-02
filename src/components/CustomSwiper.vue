<template>
  <swiper :options="swiperOption">
    <swiper-slide>
      <app-head></app-head>
    </swiper-slide>
    <swiper-slide>
      <about></about>
    </swiper-slide>
    <swiper-slide>
      <features></features>
    </swiper-slide>
    <swiper-slide>
      <ui></ui>
    </swiper-slide>
    <swiper-slide>
      <contacts></contacts>
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>
<script>
import AppHead from "./slide/Head";
import About from "./slide/About";
import Features from "./slide/Features";
import Ui from "./slide/Ui";
import Contacts from "./slide/Contacts";

export default {
  data() {
    return {
      swiperOption: {
        direction: "vertical",
        effect: "fade",
        mousewheel: true,
        pagination: {
          el: ".swiper-pagination",
          clickable: true
        }
      }
    };
  },
  components: {
    AppHead,
    About,
    Features,
    Ui,
    Contacts
  }
};
</script>
<style lang="less">
@xs: ~'(max-width:576px)';
h4 {
  font-family: TT Norms Medium !important;
  font-size: 20px;
  line-height: 30px;
  @media @xs {
    font-size: 16px;
  }
}
h6 {
  font-family: TT Norms Regular !important;
  font-size: 16px;
  line-height: 20px;
  @media @xs {
    font-size: 12px;
    width: 90%;
  }
}

.swiper-container {
  height: 85vh;
}
.swiper-slide {
  background: white;
  padding-left: 8%;
}
.swiper-pagination-bullets {
  left: 0;
  top: 40% !important;
  width: 30px;
}
.swiper-pagination-bullet {
  width: 10px;
  height: 3px;
  border-radius: 0;
  background: rgba(0, 0, 0, 0.3);
  opacity: 1;
  transition: width 0.3s;
  margin: 10px 0 !important;
}
.swiper-pagination-bullet-active {
  width: 30px;
  background: #3d45ee;
  transition: width 0.3s;
}
.swiper-slide-active > .container {
  display: block !important;
}
.swiper-slide-prev > .container {
  display: none !important;
}
.swiper-slide-next > .container {
  display: none !important;
}
@media @xs {
  .swiper-pagination {
    display: none;
  }
}
</style>
