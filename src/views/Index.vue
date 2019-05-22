<template>
  <div class="wrapper">
    <div class="header">
      <!--下拉导航-->
      <div class="wrapper_area">
        <div class="top_nav">
          <div class="nav_item" :class='{active: index === nowIndex}' v-for='(tabItem,index) in tabParams'
               @mouseover='tabToggle(index)' @mouseout="tabToggle_auto">
            <div :class='{dropdownBtn: index === 0}' @mouseover="dropdown">{{tabItem.title}}</div>
            <div class="dropdown_wrapper" v-show='index === needindex?true:false'>
              <div v-for='(item,nedindex) in tabItem.child' :key="nedindex" :class='{sub_active: subIndex === nedindex}' class="dropdown_item" @mouseover="subItemOver(nedindex)">{{item.title}}</div>
            </div>
          </div>
        </div>

      </div>
      <div class="banner_bg"></div>
      <!--倒计时-->
      <div class="count_down">
        <div class="time_text">距第十一届报名截止还有</div>
        <div class="count_down_text">{{day}}</div>
        <div class="time_text">天</div>
        <div class="count_down_text">{{hr}}</div>
        <div class="time_text">时</div>
        <div class="count_down_text">{{minute}}</div>
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
  import IndexContent from './IndexContent'

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
        subIndex:-1,
        dropdownActive: true,
        tabParams: [
          {title: "首页"},
          {
            title: "走进大赛",
            child: [
              {title: "大赛介绍"},
              {title: "领导关怀"},
              {title: "大赛方案"},
              {title: "往届大赛"},
            ]
          },
          {title: "通知公告"},
          {title: "新闻中心"},
          {
            title: "全国行业总决赛",
            child: [
              {title: "生物医药"},
              {title: "电子信息"},
              {title: "新能源及节能环保"},
              {title: "互联网"},
              {title: "新材料"},
              {title: "先进制造"},
            ]
          },
          {title: "地方赛事"},
          {
            title: "专业赛事",
            child: [
              {title: "军民融合"},
              {title: "大中小企业融通"},
              {title: "国际新能源及智能汽车"},
              {title: "第三代半导体"},
              {title: "港澳台赛"},
              {title: "创新方法"},
            ]
          },
          {
            title: "众扶平台",
            child: [
              {title: "科技型中小企业评价"},
              {title: "优胜企业动态名录库"},
              {title: "招商银行“千鹰展翼“计划"},
              {title: "大企业对接"}
            ]
          },
        ]
      };
    },
    mounted: function () {
      this.countdown();
    },
    components: {
      Banner,
      Foot,
      IndexContent
    },
    methods: {
      subItemOver(index){
        this.subIndex = index;
        console.log('xxxxx ', index);
      },
      tabToggle_auto() {
        this.needindex = 999;
        this.nowIndex = 999;
      },
      countdown: function () {
        const end = Date.parse(new Date('2019-12-01'));
        const now = Date.parse(new Date());
        const msec = end - now;
        let day = parseInt(msec / 1000 / 60 / 60 / 24);
        let hr = parseInt(msec / 1000 / 60 / 60 % 24);
        let minute = parseInt(msec / 1000 / 60 % 60);
        let sec = parseInt(msec / 1000 % 60);
        this.day = day;
        this.hr = hr > 9 ? hr : '0' + hr;
        this.minute = minute > 9 ? minute : '0' + minute;
        this.sec = sec > 9 ? sec : '0' + sec;
        const that = this;
        setTimeout(function () {
          that.countdown()
        }, 1000)
      },
      dropdown: function () {
        if (event.target.getAttribute('class') === 'dropdownBtn') {
          this.dropdownActive = !this.dropdownActive;
        }
      },
      tabToggle: function (index) {
        this.needindex = index;
        this.nowIndex = index;
        if (index === 0) {
          return
        } else {
          this.dropdownActive = false;
        }
      },
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
    background: url("https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=2457415673,3693389573&fm=26&gp=0.jpg") no-repeat center center;
    background-size: 100%;
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

  .wrapper_area {
    width: 100%;
    height: 48px;
    background: #5ea600;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    z-index: 999;
  }
  .top_nav{
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
    background-color:  rgba(94,166,0,0.5);
    color: #fff;
  }

  .nav_item {
    color: #fff;
    font-size: 16px;
    flex: 1;
    text-align: center;
    height: 48px;
    line-height: 48px;
    cursor: pointer;

  }

  .nav_item.active {
    background: #73B221;
  }

  .dropdownBtn {
    display: inline-block;
    width: 100%;
    height: 100%;
  }

  .sub_active{
    color: #5ea600 !important;
    background-color: rgba(255,255,255,0.8);
  }

</style>
