<template>
  <div class="bottom-navigation fade-in">
    <div class="mouse">
      <div class="mouse-scroll shake-vertical"></div>
    </div>
    <!-- <div class="shake-vertical" v-show="activeIndex === 4">
      <svg width="25" height="35" viewBox="0 0 44 62" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M22 2V62M22 2L2 22M22 2L42 22" stroke="rgba(0, 0, 0, 0.3)" stroke-width="4" stroke-linejoin="round"/>
      </svg>
    </div> -->
    <div class="svg-label">{{$t("scroll.down")}}</div>
    <!-- <div class="svg-label" v-show="activeIndex === 4">{{$t("scroll.up")}}</div> -->
  </div>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
.bottom-navigation {
  display: flex;
  flex-direction: row;
  align-items: flex-end;
  justify-content: flex-start;
  cursor: pointer;
  .mouse {
    width: 25px;
    height: 35px;
    border: 2px solid rgba(0, 0, 0, 0.3);
    transition: border 0.3s ease-in;
    box-sizing: border-box;
    border-radius: 20px;
    .mouse-scroll {
      width: 2px;
      height: 6px;
      margin-left: 10px;
      margin-top: 5px;
      background: rgba(0, 0, 0, 0.3);
      transition: background 0.3s ease-in;
    }
  }
  .svg-label {
    font-family: TT Norms Medium;
    color: rgba(0, 0, 0, 0.3);
    transition: color 0.3s ease-in;
    margin-left: 10px;
  }
  .shake-vertical {
    -webkit-animation: shake-vertical 4s cubic-bezier(0.455, 0.03, 0.515, 0.955)
      infinite both;
    animation: shake-vertical 4s cubic-bezier(0.455, 0.03, 0.515, 0.955)
      infinite both;
  }
}
.bottom-navigation:hover {
  .svg-label {
    color: rgba(0, 0, 0, 1);
    transition: color 0.3s ease-in;
  }
  .mouse {
    border: 2px solid rgba(0, 0, 0, 1);
    transition: border 0.3s ease-in;
    .mouse-scroll {
      background: rgba(0, 0, 0, 1);
      transition: background 0.3s ease-in;
    }
  }
}
@-webkit-keyframes shake-vertical {
  0%,
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }
  10%,
  30%,
  50%,
  70% {
    -webkit-transform: translateY(-2px);
    transform: translateY(-2px);
  }
  20%,
  40%,
  60% {
    -webkit-transform: translateY(2px);
    transform: translateY(2px);
  }
  80% {
    -webkit-transform: translateY(1px);
    transform: translateY(1px);
  }
  90% {
    -webkit-transform: translateY(-1px);
    transform: translateY(-1px);
  }
}
@keyframes shake-vertical {
  0%,
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }
  10%,
  30%,
  50%,
  70% {
    -webkit-transform: translateY(-2px);
    transform: translateY(-2px);
  }
  20%,
  40%,
  60% {
    -webkit-transform: translateY(2px);
    transform: translateY(2px);
  }
  80% {
    -webkit-transform: translateY(1px);
    transform: translateY(1px);
  }
  90% {
    -webkit-transform: translateY(-1px);
    transform: translateY(-1px);
  }
}
</style>
