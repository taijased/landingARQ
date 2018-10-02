<template>
  <div>
    <div class="container">
      <div class="left-bar fade-in-left">
        <h4 v-html="$t('head.title')"></h4>
        <h6 v-html=" $t('head.subtitle')"></h6>
        <div class="buttons">
          <div class="btn-main">
            <svg width="20px" height="20px" viewBox="0 0 77 77" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                <!-- Generator: Sketch 49.3 (51167) - http://www.bohemiancoding.com/sketch -->
                <title>apple-logo</title>
                <desc>Created with Sketch.</desc>
                <defs></defs>
                <g id="apple-logo" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                    <path d="M10.251195,28.3054399 C13.6785905,22.3514449 19.8954207,18.5918243 26.4747057,18.4951325 C26.54017,18.4938702 26.6066453,18.4931128 26.6741316,18.4931128 C29.5037549,18.4931128 32.1766684,19.5524311 34.5348985,20.4872871 C36.2983895,21.1860938 37.8212551,21.7897235 38.9948095,21.7897235 C40.0392046,21.7897235 41.5534764,21.1934151 43.3066044,20.5029395 C45.8463145,19.5026967 49.0075561,18.2578209 52.3075616,18.2578209 C52.7301726,18.2578209 53.1510143,18.2782701 53.5587126,18.318916 C56.3683681,18.4395915 63.3470103,19.4426114 67.9001889,26.0979377 C67.9962369,26.238305 68.0316229,26.4119968 67.9977534,26.5788723 C67.9638839,26.7460002 67.8640445,26.892174 67.7207309,26.9843215 L67.659058,27.0226953 C66.3361238,27.8401578 59.7396513,32.3503393 59.8243251,40.8672989 C59.9155707,51.3504098 68.5957783,55.1966239 69.585325,55.6008109 C69.593666,55.6043453 69.6234914,55.6167158 69.6315797,55.6205027 C69.9250315,55.7550634 70.0696089,56.0888143 69.967242,56.3945422 L69.9455048,56.4629586 C69.407889,58.1832148 67.814504,62.6848127 64.638097,67.3212237 C61.5941351,71.7617265 58.1439914,76.7952557 52.5246805,76.8997737 C49.8980217,76.9490033 48.1203763,76.1774883 46.3945462,75.4317242 C44.6434403,74.6748519 42.8326836,73.8919762 39.9952247,73.8919762 C37.012683,73.8919762 35.1111862,74.7011076 33.2726261,75.4837308 C31.6350085,76.1802654 29.9412786,76.901036 27.5974557,76.9944459 C27.5009023,76.9982328 27.4066236,77 27.3125977,77 C22.3239175,77 18.6816779,72.3353136 15.0841765,67.1386958 C7.87704118,56.7444505 3.73383569,39.6017215 10.251195,28.3054399 Z M53.564526,0.000485083702 C53.8915946,-0.0123903295 54.1820133,0.23249498 54.2184104,0.56220654 C54.6804516,4.76968959 53.1530364,9.46694326 50.1323282,13.127095 C47.2622636,16.5933582 43.05966,18.7460768 39.1639044,18.7460768 C38.8904205,18.7458243 38.6159255,18.7352211 38.3469913,18.714267 C38.0494954,18.6912932 37.80887,18.4633226 37.7696925,18.1679455 C37.1448753,13.4469607 39.5165015,8.7633398 41.94424,5.9542276 C44.8009084,2.61217428 49.5803052,0.162563814 53.564526,0.000485083702 Z" fill="#FFFFFF" fill-rule="nonzero"></path>
                </g>
            </svg>
            <div class="btn-title">{{ $t("head.buttons-title") }}</div>
          </div>
          <div class="btn-main">
          <svg width="20px" height="20px" viewBox="0 0 77 77" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                <!-- Generator: Sketch 49.3 (51167) - http://www.bohemiancoding.com/sketch -->
                <title>play-market-logo</title>
                <desc>Created with Sketch.</desc>
                <defs></defs>
                <g id="play-market-logo" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                    <path d="M69.2433083,30.4698156 L17.1659204,1.24591523 C14.1178573,-0.462100016 10.5065652,-0.41398691 7.51056536,1.39025455 C4.68495411,3.08864718 3,6.03798055 3,9.28080387 L3,67.7189819 C3,70.9666166 4.68968713,73.9159499 7.51529838,75.6143426 C9.05352896,76.5381142 10.7526821,77 12.4565683,77 C14.0705272,77 15.684486,76.5862273 17.1706534,75.7490593 L69.2480413,46.5347815 C72.2251091,44.8604455 74.0047236,41.8581877 73.9999906,38.4950816 C73.9999906,35.1367868 72.2203761,32.1393403 69.2433083,30.4698156 Z M66.952528,42.3248848 L14.8798731,71.5391625 C13.3132444,72.414821 11.4579017,72.3907645 9.9196711,71.4669929 C8.52816406,70.6346361 7.73301717,69.2682239 7.73301717,67.7189819 L7.73301717,9.28080387 C7.73301717,7.73156187 8.52816406,6.36514967 9.91020507,5.53279294 C10.705352,5.0564732 11.5809601,4.82071898 12.4565683,4.82071898 C13.2848463,4.82071898 14.1131243,5.03241664 14.8751401,5.45581197 L66.957261,34.6845236 C68.3960983,35.4928238 69.2622404,36.921783 69.2622404,38.4998929 C69.2622404,40.0780028 68.4008313,41.5117733 66.952528,42.3248848 Z M58.5845537,48.9067576 L9.17185439,2.56902564 C8.21105191,1.67412187 6.71541848,1.7318576 5.82561125,2.70855364 C4.94053704,3.68524969 4.99733325,5.20562382 5.95813573,6.1053389 L55.370835,52.4382596 C55.8252046,52.8664662 56.4026327,53.0781639 56.9753278,53.0781639 C57.6142851,53.0781639 58.2485094,52.8231644 58.7170781,52.3035429 C59.6068854,51.3268469 59.5453561,49.8064727 58.5845537,48.9067576 Z M55.9482631,23.1421896 C55.0253247,22.203984 53.5249583,22.203984 52.60202,23.1421896 L5.74514996,70.7693528 C4.82221161,71.7075584 4.82221161,73.2327438 5.74514996,74.1709494 C6.20898564,74.6376465 6.81481184,74.8734007 7.42063804,74.8734007 C8.02646424,74.8734007 8.63229043,74.6376465 9.0913931,74.1709494 L55.9482631,26.5437862 C56.8712014,25.6055806 56.8712014,24.0803952 55.9482631,23.1421896 Z" id="Shape" fill="#FFFFFF" fill-rule="nonzero"></path>
                </g>
            </svg>
            <div class="btn-title">{{ $t("head.buttons-title") }}</div>
          </div>
        </div>
      </div>
      <div class="right-bar" >
        <div class="right-bar-img fade-in-br"></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>

<style lang="less" scoped>
@lb: 35%;
@rb: 65%;
@xs: ~"(max-width:576px)";
@time: 1s;
@time-description: .25s;
.container {
  display: flex;
  flex-direction: row;
  height: 100%;
  .left-bar {
    position: relative;
    width: @lb;
    display: flex;
    flex-direction: column;
    justify-content: center;
    @media @xs {
      width: 70%;
    }
    h6 {
      margin-bottom: 20px;
      margin-top: 12px;
      @media @xs {
        width: 100%;
      }
    }
    h4 {
      line-height: 22px;
    }
    .buttons {
      display: flex;
      flex-direction: row;
      align-items: center;
      font-family: TT Norms Regular;
      .btn-main {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        border-radius: 50px;
        padding: 10px 20px;
        margin-right: 20px;
        background: rgba(61, 69, 238, 1);
        transition: background @time-description ease-in;
        @media @xs {
          margin: 0;
          padding: 7px 15px;
          margin-right: 10px;
          font-size: 10px;
          svg {
            width: 12.5px;
            height: 12.5px;
          }
        }
        .btn-title {
          color: white;
          margin-left: 5px;
        }
      }
      .btn-main:hover {
        cursor: pointer;
        background: rgba(61, 69, 238, 0.7);
        transition: background @time-description ease-in;
      }
    }
  }
  .right-bar {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: @rb;

    .right-bar-img {
      position: absolute;
      width: 26%;
      height: 100%;
      background: url(../../assets/img/1.png);
      background-repeat: no-repeat;
      background-size: 100%;
      left: 50%;
      top: -1%;
      @media @xs {
        width: 75%;
        left: 51%;
        top: 10%;
        z-index: 2;
      }
    }
    img {
      width: 50%;
    }
  }
}
.fade-in-left {
  -webkit-animation: fade-in-left @time cubic-bezier(0.39, 0.575, 0.565, 1) both;
  animation: fade-in-left @time cubic-bezier(0.39, 0.575, 0.565, 1) both;
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
  -webkit-animation: fade-in-br @time cubic-bezier(0.39, 0.575, 0.565, 1) both;
  animation: fade-in-br @time cubic-bezier(0.39, 0.575, 0.565, 1) both;
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
