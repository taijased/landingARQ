<template>
  <div class="container">
    <div class="left-bar fade-in-left">
      <h4>{{$t("contacts.title")}}</h4>
      <h6>{{$t("contacts.description")}}</h6>
      <div class="buttons">
        <input type="text" placeholder="Ваш e-mail" class="buttons-input">
        <div class="btn-main">
          <div class="btn-title">{{$t("contacts.subscribe")}}</div>
        </div>
      </div>
    </div>
    <div class="right-bar">
    </div>
    <div class="email fade-in-fwd">hello@arq.su</div>
  </div>
</template>
<script>
export default {

}
</script>

<style lang="less" scoped>
@lb: 30%;
@rb: 70%;
@xs: ~'(max-width:576px)';
@time: 1s;

.container {
  display: flex;
  flex-direction: row;
  .left-bar {
    width: @lb;
    display: flex;
    flex-direction: column;
    justify-content: center;
    @media @xs {
      width: 100%;
    }
    h4,
    h6 {
      margin-bottom: 20px;
    }
    .buttons {
      display: flex;
      flex-direction: row;
      align-items: center;
      font-family: TT Norms Regular;
      @media @xs {
        font-size: 14px;
      }
      .buttons-input {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        border-radius: 50px;
        outline: none;
        border: none;
        box-shadow: 0 0 10px rgba(0,0,0,0.2);
        transition: box-shadow @time ease-in;
        margin-right: 15px;
        height: 37px;
        padding-left: 15px;
        width: 500px;
        @media @xs {
          margin-right: 0;
        }
      }
      .buttons-input:hover {
        box-shadow: 0 0 10px rgba(0,0,0,0.5);
        transition: box-shadow @time ease-in;
        // color: rgba(0,0,0,1);
        // transition: color 0.5s ease-in;
      }
      .btn-main {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        background: rgba(61, 69, 238, 1);
        transition: background @time ease-in;
        border-radius: 50px;
        padding: 10px 20px;
        .btn-title {
          color: white;
          margin-left: 5px;
        }
        @media @xs {
          margin: 0;
          margin-left: 15px;
        }
      }
      .btn-main:hover {
        cursor: pointer;
        background: rgba(61, 69, 238, 0.7);
        transition: background @time ease-in;
      }
    }
  }
  .right-bar {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: @rb;
    @media @xs {
      display: none;
    }
  }
  .email {
    position: absolute;
    font-family: TT Norms Medium;
    top: 90%;
    right: 8%;
    color: rgba(0, 0, 0, 0.3);
    -webkit-transition: color @time ease-in;
    transition: color @time ease-in;
    font-size: 18px;
    cursor: pointer;
    margin-right: 8%;
    margin-bottom: 5%;
    @media @xs {
      margin-right: 0;
      right: 100px;
      font-size: 16px;
    }
  }
  .email:hover {
    color: rgba(0, 0, 0, 1);
    transition: color @time ease-in;
  }
}
.fade-in-left {
  -webkit-animation: fade-in-left @time cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
	animation: fade-in-left @time cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
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
.fade-in-fwd {
	-webkit-animation: fade-in-fwd 1s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
	        animation: fade-in-fwd 1s cubic-bezier(0.390, 0.575, 0.565, 1.000) both;
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
</style>
