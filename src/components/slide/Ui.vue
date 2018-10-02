<template>
  <div class="container">
    <div class="left-bar">
      <div class="my-collapse fade-in-left">
        <div class="my-collapse-item"  v-for="(item, index) in 3" :key="index">
          <div class="my-collapse-item-title" :class="{active: item == indexTitle }" @mouseover="setIndexTitle(item)">
            <div class="my-collapse-item-title-index">0{{index + 1}}</div>
            <transition name="border">
              <div class="my-collapse-item-title-border" v-show="item == indexTitle"></div>
            </transition>
            <h4>{{$t('ui.item-' + item +'.title')}}</h4>
          </div>
          <div class="my-collapse-item-description" :class="{'slide-in-top': item == indexTitle }"  v-show="item == indexTitle">
            <h6>{{$t('ui.item-'+ item +'.description')}}</h6>
          </div>
        </div>
      </div>
    </div>
    <div class="right-bar">
      <div class="right-bar-img fade-in-bl"></div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      indexTitle: 1
    };
  },
  methods: {
    setIndexTitle(indexTitle) {
      this.indexTitle = indexTitle;
    }
  }
};
</script>

<style lang="less" scoped>
@lb: 35%;
@rb: 65%;
@purple: rgba(61, 69, 238, 1);
@xs: ~"(max-width:576px)";
.container {
  display: flex;
  flex-direction: row;
  height: 100%;
  .left-bar {
    width: @lb;
    display: flex;
    flex-direction: column;
    justify-content: center;
    z-index: 1;
    @media @xs {
      width: 100%;
      justify-content: flex-start;
    }
    .my-collapse {
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      @media @xs {
        margin: 0;
        margin-top: 40px;
        margin-left: 20px;
        h4 {
          font-size: 20px;
        }
      }
      .my-collapse-item {
        cursor: pointer;
        .my-collapse-item-title {
          display: flex;
          flex-direction: row;
          align-items: flex-end;
          color: rgba(0, 0, 0, 0.3);
          transition: color 0.25s ease-in-out;
          margin-left: -15px;
          .my-collapse-item-title-index {
            position: relative;
            left: -12px;
            top: -3.5px;
            font-family: TT Norms Regular;
            color: rgba(0, 0, 0, 1);
            transition: color 0.25s ease-in;
            font-size: 12px;
            @media @xs {
              left: 0;
              top: 0;
              margin-right: 10px;
            }
          }
          @wb: 30px;
          .my-collapse-item-title-border {
            align-self: flex-end;
            width: @wb;
            height: 2px;
            margin-right: 12px;
            margin-bottom: 0.35rem;
            background: @purple;
          }
          .border-enter {
            width: 0;
          }
          .border-enter-active {
            transition: width 0.2s ease;
          }
          .border-enter-to {
            width: @wb;
          }
          .border-leave {
            width: @wb;
          }
          .border-leave-active {
            transition: width 0.2s ease;
          }
          .border-leave-to {
            width: 0;
            background: rgba(0, 0, 0, 0.3);
          }
        }
        .my-collapse-item-description {
          color: rgba(0, 0, 0, 1);
          padding: 0 12px;
          height: 60px;
          @media @xs {
            width: 85%;
            margin-bottom: 15px;
          }
        }
        .active {
          color: @purple;
          transition: color 0.5s ease-in;
        }
        .active-description {
          opacity: 1;
          transition: opacity 0.5s ease-in;
        }
      }
    }
  }
  .right-bar {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: @rb;
    z-index: 0;
    @media @xs {
      position: absolute;
      left: 35%;
      bottom: -45%;
      width: 240%;
      height: 100%;
    }
    .right-bar-img {
      position: absolute;
      width: 65%;
      height: 100%;
      background: url(/static/img/4.f9cc27a.png);
      background-repeat: no-repeat;
      background-size: 100%;
      left: 39%;
      @media @xs {
        position: absolute;
        top: 0;
        left: 0;
      }
    }
    img {
      width: 30%;
    }
  }
}
.fade-in-left {
  -webkit-animation: fade-in-left 1.6s cubic-bezier(0.39, 0.575, 0.565, 1) both;
  animation: fade-in-left 1.6s cubic-bezier(0.39, 0.575, 0.565, 1) both;
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
  -webkit-animation: fade-in-br 1.6s cubic-bezier(0.39, 0.575, 0.565, 1) both;
  animation: fade-in-br 1.6s cubic-bezier(0.39, 0.575, 0.565, 1) both;
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
.fade-in-fwd {
  -webkit-animation: fade-in-fwd 1s cubic-bezier(0.39, 0.575, 0.565, 1) both;
  animation: fade-in-fwd 1s cubic-bezier(0.39, 0.575, 0.565, 1) both;
}
@-webkit-keyframes fade-in-fwd {
  0% {
    -webkit-transform: translateZ(-80px);
    transform: translateZ(-80px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateZ(0);
    transform: translateZ(0);
    opacity: 1;
  }
}
@keyframes fade-in-fwd {
  0% {
    -webkit-transform: translateZ(-80px);
    transform: translateZ(-80px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateZ(0);
    transform: translateZ(0);
    opacity: 1;
  }
}
.slide-in-bottom {
  -webkit-animation: slide-in-bottom 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94)
    reverse both;
  animation: slide-in-bottom 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94) reverse
    both;
}
@-webkit-keyframes slide-in-bottom {
  0% {
    -webkit-transform: translateY(1000px);
    transform: translateY(1000px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    opacity: 1;
  }
}
@keyframes slide-in-bottom {
  0% {
    -webkit-transform: translateY(1000px);
    transform: translateY(1000px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    opacity: 1;
  }
}
.fade-in-bl {
  -webkit-animation: fade-in-bl 0.6s cubic-bezier(0.39, 0.575, 0.565, 1) both;
  animation: fade-in-bl 0.6s cubic-bezier(0.39, 0.575, 0.565, 1) both;
}
@-webkit-keyframes fade-in-bl {
  0% {
    -webkit-transform: translateX(-50px) translateY(50px);
    transform: translateX(-50px) translateY(50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateX(0) translateY(0);
    transform: translateX(0) translateY(0);
    opacity: 1;
  }
}
@keyframes fade-in-bl {
  0% {
    -webkit-transform: translateX(-50px) translateY(50px);
    transform: translateX(-50px) translateY(50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateX(0) translateY(0);
    transform: translateX(0) translateY(0);
    opacity: 1;
  }
}
.slide-in-top {
  -webkit-animation: slide-in-top 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94) both;
  animation: slide-in-top 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94) both;
}
@-webkit-keyframes slide-in-top {
  0% {
    -webkit-transform: translateY(-20px);
    transform: translateY(-20px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    opacity: 1;
  }
}
@keyframes slide-in-top {
  0% {
    -webkit-transform: translateY(-20px);
    transform: translateY(-20px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    opacity: 1;
  }
}
</style>
