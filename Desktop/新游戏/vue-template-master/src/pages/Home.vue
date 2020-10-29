<template>
  <div class="box">
    <!--规则-->
    <the-rules></the-rules>
<!--    <div class="big-wheel-box-c">-->
<!--      <div class="big-wheel-box roteinit">-->
<!--        <big-wheel-->
<!--            width="3.6rem"-->
<!--            height="3.6rem"-->
<!--            ref="bigWheel"-->
<!--            :prizeList="prizeList"-->
<!--            @over="over">-->
<!--          <template v-slot:item="{ item }">-->
<!--            <img class="prize-img" :src="item.img">-->
<!--          </template>-->
<!--        </big-wheel>-->
<!--        <div class="big-wheel-lump"></div>-->
<!--      </div>-->
<!--      &lt;!&ndash; 开始按钮 &ndash;&gt;-->
<!--      <img class="btn-go" @click="go" src="https://interactive-oss.oss-cn-beijing.aliyuncs.com/1591603002317_1589522216079_jiakao_btn_start.png" />-->
<!--    </div>-->
  </div>
</template>

<script>
import TheRules from '@/components/TheRules'

export default {
  data() {
    return {
      prizeList: [
        {
          img: 'https://interactive-oss.oss-cn-beijing.aliyuncs.com/1591603004022_1589522317831_p4-1.png'
        },
        {
          img: 'https://interactive-oss.oss-cn-beijing.aliyuncs.com/1591603004254_1589522337287_p4-2.png'
        },
        {
          img: 'https://interactive-oss.oss-cn-beijing.aliyuncs.com/1591603004483_1589881483975_p5-3.png'
        },
        {
          img: 'https://interactive-oss.oss-cn-beijing.aliyuncs.com/1591603004702_1589881506548_p5-4.png'
        },
        {
          img: 'https://interactive-oss.oss-cn-beijing.aliyuncs.com/1591603004908_1589881529133_p5-5.png'
        },
        {
          img: 'https://interactive-oss.oss-cn-beijing.aliyuncs.com/1591603005169_1589881548425_p5-6.png'
        }
      ],
      valve: false, // 防止连续点击
    }
  },
  methods: {

  },
  components: {
    // BigWheel
    TheRules
  }
}
</script>

<style lang="scss">
@-webkit-keyframes circleMove{
  0% {
    -webkit-transform: rotate(0);
    transform: rotate(0)
  }
  to {
    -webkit-transform: rotate(1turn);
    transform: rotate(1turn)
  }
}
@keyframes circleMove{
  0% {
    -webkit-transform: rotate(0);
    transform: rotate(0)
  }
  to {
    -webkit-transform: rotate(1turn);
    transform: rotate(1turn)
  }
}
@-webkit-keyframes blinc{
  0% {
    opacity: 1
  }
  to {
    opacity: .2
  }
}
@keyframes blinc{
  0% {
    opacity: 1
  }
  to {
    opacity: .2
  }
}
.box {
  position: relative;
  overflow: hidden;
  width: 100vw;
  min-height: 100vh;
  background-image: url('https://interactive-oss.oss-cn-beijing.aliyuncs.com/1603337636670_1603268890693_95a5f7c64ff14181efff54b9047f541.jpg');
  background-repeat: no-repeat;
  background-position: center top;
  background-size: 100%;
  .roteinit{
    /*animation: circleMove 20s linear infinite;*/
    /*-webkit-animation: circleMove 201s linear infinite;*/
  }
  /* 大转盘css*/
  //.big-wheel-box-c{
  //  position: relative;
  //  top: 2.3rem;
  //  left: 52%;
  //  .big-wheel-lump{
  //    width: 100%;
  //    height: 100%;
  //    z-index: 999;
  //    position: absolute;
  //    top: 0;
  //    left: 0;
  //    right: auto;
  //    bottom: auto;
  //    margin-left: -2px;
  //    background-size: 100% 100%;
  //    background-repeat: no-repeat;
  //    background-position: center;
  //    -webkit-animation: blinc .5s linear .5s infinite normal;
  //    animation: blinc .5s linear .5s infinite normal;
  //    background-image: url(https://interactive-oss.oss-cn-beijing.aliyuncs.com/1591603003144_1589522289494_jiakao_dian.png);
  //  }
  //  .big-wheel-box {
  //    position: absolute;
  //    transform: translateX(-50%);
  //    text-align: center;
  //    font-size: 0;
  //    /*background-image: url('https://interactive-oss.oss-cn-beijing.aliyuncs.com/1591603003350_1589524215983_jiakao_pan.png');*/
  //    background-repeat: no-repeat;
  //    background-position: center;
  //    background-size: 100%;
  //    .prize-name {
  //      position: absolute;
  //      left: .13rem;
  //      right: .13rem;
  //      top: .2rem;
  //      font-size: .14rem;
  //      text-align: center;
  //      color: #7D2A00;
  //    }
  //    .prize-img {
  //      position: absolute;
  //      bottom: .42rem;
  //      transform: translateX(-50%);
  //      width: 1rem;
  //      height: 1rem;
  //    }
  //
  //  }
  //  .btn-go {
  //    position: absolute;
  //    top: 1.20rem;
  //    transform: translateX(-50%);
  //    width: .8rem;
  //  }
  //}

}
</style>
