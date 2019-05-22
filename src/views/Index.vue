<template>
  <div class="wrapper">
    <div class="header">
      <div class="banner_bg"></div>
      <!--倒计时-->
      <div class="count_down">
        <div class="time_text">距第十一届报名截止还有</div>
        <div class="count_down_text">{{day}}</div>
        <div class="time_text">天</div>
        <div class="count_down_text">{{hr}}</div>
        <div class="time_text">时</div>
        <div class="count_down_text">{{hr}}</div>
        <div class="time_text">分</div>
        <div class="count_down_text">{{sec}}</div>
        <div class="time_text">秒</div>
      </div>
    </div>
    <IndexContent></IndexContent>
    <Foot></Foot>
  </div>
</template>

<script>
import Banner from "@/components/common/Banner";
import Foot from "@/components/common/foot";
import IndexContent from "./IndexContent";
export default {
  name: "index",
  data() {
    return {
      day: 0,
      hr: 0,
      minute: 0,
      sec: 0
    };
  },
  components: {
    Banner,
    Foot,
    IndexContent
  },
  mounted: function() {
    this.countTime();
  },
  methods: {
    countTime: function() {
      //获取当前时间
      var date = new Date();
      var now = date.getTime();
      //设置截止时间
      var endDate = new Date("2019-6-22 23:23:23");
      var end = endDate.getTime();
      //时间差
      var leftTime = end - now;
      //定义变量 d,h,m,s保存倒计时的时间
      if (leftTime >= 0) {
        this.day = Math.floor(leftTime / 1000 / 60 / 60 / 24);
        this.hr = Math.floor((leftTime / 1000 / 60 / 60) % 24);
        this.minute = Math.floor((leftTime / 1000 / 60) % 60);
        this.sec = Math.floor((leftTime / 1000) % 60);
      }
      //递归每秒调用countTime方法，显示动态时间效果
      setTimeout(this.countTime, 1000);
    }
  }
};
</script>

<style scoped>
.wrapper {
  width: 100%;
}
.header {
  width: 100%;
}
.count_down {
  display: flex;
  flex-direction: row;
  position: absolute;
  top: 230px;
  right: 50px;
}
.banner_bg {
  width: 100%;
  height: 440px;
  background: url("https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=2457415673,3693389573&fm=26&gp=0.jpg")
    no-repeat center center;
  background-size: 100%;
  position: relative;
}
.time_text {
  font-size: 24px;
}
.count_down_text {
  width: 56px;
  height: 45px;
  background-color: #fff;
  border-radius: 5px;
  font-size: 20px;
  line-height: 45px;
  text-align: center;
  margin: -10px 5px 0 5px;
}
</style>
