<template>
  <div class="bottom-navigation fade-in">
    <div class="mouse">
      <div class="mouse-scroll shake-vertical"></div>
    </div>
    <div class="finger shake-vertical">
      <svg width="20" height="22" viewBox="0 0 20 22" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path fill-rule="evenodd" clip-rule="evenodd" d="M18.7294 13.8323L17.1764 20.3239C17.1155 20.5782 16.8949 20.7546 16.6398 20.7546H8.3057C8.16036 20.7546 8.01807 20.6944 7.91542 20.5896L1.8051 14.3502C1.11194 13.6424 1.0286 12.507 1.6191 11.8189C1.94129 11.4432 2.39458 11.2367 2.89666 11.2367C3.35707 11.2367 3.78292 11.4183 4.10409 11.7545L6.98647 14.6968C7.16128 14.8753 7.4235 14.9282 7.65116 14.8317C7.87883 14.7362 8.02722 14.509 8.02722 14.2568V3.12604C8.02722 2.25323 8.57401 1.48315 9.32611 1.2953C9.9217 1.14689 10.5173 1.32021 10.9604 1.76129C11.2806 2.0882 11.4564 2.52513 11.4564 2.99423V7.94468C11.4564 8.6805 11.8863 9.33641 12.551 9.61662L17.7181 11.7992C18.5068 12.1313 18.9317 12.9875 18.7294 13.8323ZM18.1847 10.6482L13.0175 8.46567C12.8102 8.37849 12.676 8.17404 12.676 7.94468V2.99423C12.676 2.19303 12.3731 1.44268 11.8172 0.874982C11.0712 0.132934 10.0335 -0.160775 9.03645 0.0851906C7.74467 0.406918 6.80759 1.68657 6.80759 3.12604V12.7529L4.97205 10.8786C4.42526 10.3068 3.6884 9.99023 2.89666 9.99023C2.03886 9.99023 1.25931 10.3483 0.702352 10.998C-0.320101 12.1894 -0.2144 14.0482 0.942211 15.2303L7.05253 21.4697C7.38285 21.807 7.83919 22 8.3057 22H16.6398C17.459 22 18.1664 21.4323 18.3615 20.6207L19.9145 14.1281C20.2601 12.6813 19.5334 11.217 18.1847 10.6482Z" fill="#B3B3B3"/>
      </svg>
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
@xs: ~'(max-width:576px)';

.bottom-navigation {
  display: flex;
  flex-direction: row;
  align-items: flex-end;
  justify-content: flex-start;
  cursor: pointer;
  .finger {
    display: none;
  }
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
  @media @xs {
    .mouse {
      display: none;
    }
    .finger {
      display: block;
    }
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
