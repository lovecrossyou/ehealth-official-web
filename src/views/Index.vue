<template>
  <div class="wrapper">
    <div class="header">
      <!--logo & 搜索框-->
      <div class="top_area">
        <div class="logo_img">
          <img src="http://qnimage.xiteng.com/logo@2x.png" alt>
        </div>
        <div class="search_box_area">
          <div class="magnifying_img">
            <img src="http://qnimage.xiteng.com/sousuo@2x.png" alt>
          </div>
          <input type="search" class="search_input">
          <button class="search_btn">搜索</button>
        </div>
      </div>
      <!--下拉导航-->
      <div class="wrapper_area">
        <div class="top_nav">
          <div
            class="nav_item"
            :class="{active: index === nowIndex}"
            v-for="(tabItem,index) in tabParams"
            @mouseover="tabToggle(index)"
            @mouseout="tabToggle_auto"
            :key="index"
          >
            <div :class="{dropdownBtn: index === 0}" @mouseover="dropdown">{{tabItem.title}}</div>
            <div class="dropdown_wrapper" v-show="index === needindex?true:false">
              <div
                v-for="(item,nedindex) in tabItem.child"
                :key="nedindex"
                :class="{sub_active: subIndex === nedindex}"
                class="dropdown_item"
                @mouseover="subItemOver(nedindex)"
              >{{item.title}}</div>
            </div>
          </div>
        </div>
      </div>
      <div class="banner_bg">
        <img src="http://qnimage.xiteng.com/banner_bk@2x.png" alt>
        <!--倒计时-->
        <div class="count_down">
          <div class="time_text">距报名截止还有</div>
          <div class="count_down_text">{{day}}</div>
          <div class="time_text">天</div>
          <div class="count_down_text">{{hr}}</div>
          <div class="time_text">时</div>
          <div class="count_down_text">{{minute}}</div>
          <div class="time_text">分</div>
          <div class="count_down_text">{{sec}}</div>
          <div class="time_text">秒</div>
        </div>
        <div class="apply_btn">报名参赛</div>
      </div>
    </div>
    <div>
      <IndexContent></IndexContent>
    </div>
    <!-- <Foot></Foot> -->
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
      needindex: 999,
      day: 0,
      hr: 0,
      minute: 0,
      sec: 0,
      nowIndex: 999,
      subIndex: -1,
      dropdownActive: true,
      tabParams: [
        { title: "大赛首页" },
        {
          title: "大赛公告",
          child: [
            { title: "大赛介绍" },
            { title: "领导关怀" },
            { title: "大赛方案" },
            { title: "往届大赛" }
          ]
        },
        { title: "企业风采" },
        { title: "产业新闻" },
        {
          title: "示范基地",
          child: [
            { title: "生物医药" },
            { title: "电子信息" },
            { title: "新能源及节能环保" },
            { title: "互联网" },
            { title: "新材料" },
            { title: "先进制造" }
          ]
        },
        { title: "产业平台" },
        {
          title: "在线留言",
          child: [
            { title: "军民融合" },
            { title: "大中小企业融通" },
            { title: "国际新能源及智能汽车" },
            { title: "第三代半导体" },
            { title: "港澳台赛" },
            { title: "创新方法" }
          ]
        },
        {
          title: "联系我们",
          child: [
            { title: "科技型中小企业评价" },
            { title: "优胜企业动态名录库" },
            { title: "“千鹰展翼“计划" },
            { title: "大企业对接" }
          ]
        }
      ]
    };
  },
  mounted: function() {
    this.countdown();
  },
  components: {
    Banner,
    Foot,
    IndexContent
  },
  methods: {
    subItemOver(index) {
      this.subIndex = index;
      console.log("xxxxx ", index);
    },
    tabToggle_auto() {
      this.needindex = 999;
      this.nowIndex = 999;
    },
    countdown: function() {
      const end = Date.parse(new Date("2019-8-28"));
      const now = Date.parse(new Date());
      const msec = end - now;
      let day = parseInt(msec / 1000 / 60 / 60 / 24);
      let hr = parseInt((msec / 1000 / 60 / 60) % 24);
      let minute = parseInt((msec / 1000 / 60) % 60);
      let sec = parseInt((msec / 1000) % 60);
      this.day = day;
      this.hr = hr > 9 ? hr : "0" + hr;
      this.minute = minute > 9 ? minute : "0" + minute;
      this.sec = sec > 9 ? sec : "0" + sec;
      const that = this;
      setTimeout(function() {
        that.countdown();
      }, 1000);
    },
    dropdown: function() {
      if (event.target.getAttribute("class") === "dropdownBtn") {
        this.dropdownActive = !this.dropdownActive;
      }
    },
    tabToggle: function(index) {
      this.needindex = index;
      this.nowIndex = index;
      if (index === 0) {
        return;
      } else {
        this.dropdownActive = false;
      }
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

.top_area {
  width: 1048px;
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 18px 0 21px 0;
  box-sizing: border-box;
}
.logo_img image {
  width: 255px;
  height: 44px;
}
.search_box_area {
  width: 369px;
  height: 24px;
  background: rgba(243, 246, 248, 1);
  border: 1px solid rgba(223, 223, 223, 1);
  border-radius: 12px;
  display: flex;
  flex-direction: row;
  padding-left: 10px;
  box-sizing: border-box;
}
.search_input {
  flex: 1;
  border: none;
  outline: none;
  background-color: rgba(243, 246, 248, 1);
  margin-left: 15px;
}
.search_btn {
  width: 81px;
  height: 24px;
  border-radius: 12px;
  background-color: #1479d7;
  font-size: 14px;
  color: #fff;
  text-align: center;
  line-height: 24px;
  border: none;
  outline: none;
  cursor: pointer;
}
.magnifying_img image {
  width: 14px;
  height: 15px;
}

.count_down {
  width: 600px;
  display: flex;
  flex-direction: row;
  margin: 0 auto;
  color: #fff;
  font-size: 18px;
  align-items: center;
  position: absolute;
  left: 27%;
}

.banner_bg {
  width: 100%;
  height: 409px;
  /* background: url("http://qnimage.xiteng.com/banner_bk@2x.png") no-repeat center */
  /* center; */
  /* background-size: 100%; */
  padding-top: 210px;
  box-sizing: border-box;
  position: relative;
}
.banner_bg > img {
  width: 100%;
  height: 409px;
  position: absolute;
  top: 0;
}

.time_text {
  font-size: 24px;
}

.count_down_text {
  width: 55px;
  height: 40px;
  background: rgba(255, 255, 255, 0.41);
  border: 1px solid rgba(255, 255, 255, 1);
  border-radius: 5px;
  font-size: 20px;
  line-height: 40px;
  text-align: center;
  margin: 0 13px;
}

.wrapper_area {
  width: 100%;
  height: 48px;
  background: #1479d7;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  z-index: 999;
}
.top_nav {
  width: 1180px;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 999;
  margin: 0 auto;
}

.dropdown_wrapper {
  font-size: 14px;
}

.dropdown_item {
  display: block;
  background-color: rgba(25, 121, 213, 0.5);
  color: #fff;
}

.nav_item {
  color: #fff;
  font-size: 14px;
  flex: 1;
  text-align: center;
  height: 48px;
  line-height: 48px;
  cursor: pointer;
}

.nav_item.active {
  background: #0058ad;
}

.dropdownBtn {
  display: inline-block;
  width: 100%;
  height: 100%;
}

.sub_active {
  color: #1479d7 !important;
  background-color: rgba(255, 255, 255, 0.8);
}
.apply_btn {
  width: 200px;
  height: 50px;
  background: linear-gradient(
    100deg,
    rgba(76, 191, 217, 1) 0%,
    rgba(84, 151, 210, 1) 100%
  );
  border-radius: 25px;
  box-shadow: 0px 5px 10px 0px #27618f;
  text-align: center;
  line-height: 50px;
  color: #fff;
  font-size: 18px;
  margin: 30px auto 0 auto;
  font-weight: bold;

   position: absolute;
  left: 40%;
  bottom: 60px;
}
</style>
