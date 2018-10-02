<template>
  <div class="container">
    <div class="left-bar fade-in-left">
      <h4>{{$t("about.title")}} <span>arq</span>?</h4>
      <h6 v-html="$t('about.description')"></h6>
    </div>
    <div class="right-bar">
      <div class="right-bar-img fade-in-br"></div>
    </div>
  </div>
</template>
<script>
export default {

}
</script>

<style lang="less" scoped>
@lb: 35%;
@rb: 65%;
@xs: ~'(max-width:576px)';

.container {
  display: flex;
  flex-direction: row;
  height: 100%;
  .left-bar {
    width: @lb;
    display: flex;
    flex-direction: column;
    justify-content: center;
    @media @xs {
      width: 75%;
    }
    h4 {
      span {
        color: rgba(61, 69, 238, 1);
        text-transform: uppercase;
      }
    }
    h6 {
      margin-bottom: 20px;
      margin-top: 12px;
    }

  }
  .right-bar {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: @rb;
     .right-bar-img {
      position: absolute;
      width: 29%;
      height: 100%;
      background: url(../../assets/img/2.png);
      background-repeat: no-repeat;
      background-size: cover;
      left: 50%;
      @media @xs {
        left: 50%;
        width: 75%;
        left: 65%;
        top: 30%;
        z-index: 0;
      }
    }
    img {
      width: 50%;
    }
    @media @xs {
      width: 15%;
    }
  }
}
.fade-in-left {
  -webkit-animation: fade-in-left 1s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
	animation: fade-in-left 1s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
}

@-webkit-keyframes fade-in-left {
  0% {
    -webkit-transform: translateX(-50px);
            transform: translateX(-50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateX(0);
            transform: translateX(0);
    opacity: 1;
  }
}
@keyframes fade-in-left {
  0% {
    -webkit-transform: translateX(-50px);
            transform: translateX(-50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateX(0);
            transform: translateX(0);
    opacity: 1;
  }
}
.fade-in-br {
	-webkit-animation: fade-in-br 1.6s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
	        animation: fade-in-br 1.6s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
}
@-webkit-keyframes fade-in-br {
  0% {
    -webkit-transform: translateX(50px) translateY(50px);
            transform: translateX(50px) translateY(50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateX(0) translateY(0);
            transform: translateX(0) translateY(0);
    opacity: 1;
  }
}
@keyframes fade-in-br {
  0% {
    -webkit-transform: translateX(50px) translateY(50px);
            transform: translateX(50px) translateY(50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateX(0) translateY(0);
            transform: translateX(0) translateY(0);
    opacity: 1;
  }
}
</style>
