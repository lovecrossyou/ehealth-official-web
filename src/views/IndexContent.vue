<template>
  <div class="main_content">
    <div class="index_content">
      <div>
        <div class="main-left">
          <!-- 左侧面板 ------------------------------->
          <div class="content_left">
            <!-- 媒体聚焦 -->
            <div>
              <NaviTitle title="媒体聚焦"></NaviTitle>
            </div>

            <div class="meiti-items">
              <div
                href="/cxcyds/jdxw/201905/ded81ead002d442d9049064693551016.shtml"
                target="_blank"
              >
                <div class="gg1 gg">
                  <img
                    src="http://www.cxcyds.com/cxcyds/jdxw//201905/ded81ead002d442d9049064693551016/images/9c9b727727754478a843d7e8919bf0b7.png"
                  >
                  <div class="meiti-item-desc">2019第八届中国创新创业大赛国际第 三代半导体专业正式启动</div>
                </div>
              </div>
              <div
                href="/cxcyds/jdxw/201905/ded81ead002d442d9049064693551016.shtml"
                target="_blank"
              >
                <div class="gg1 gg">
                  <img
                    src="http://www.cxcyds.com/cxcyds/jdxw//201905/ded81ead002d442d9049064693551016/images/9c9b727727754478a843d7e8919bf0b7.png"
                  >
                  <div class="meiti-item-desc">2019第八届中国创新创业大赛国际第 三代半导体专业正式启动</div>
                </div>
              </div>
            </div>

            <div style="padding:20px 0 15px 0;">
              <NaviTitle title="大赛公告"></NaviTitle>
            </div>
            <div>
              <el-timeline :reverse="reverse">
                <el-timeline-item
                  v-for="(activity, index) in activities"
                  :key="index"
                  :size="normal"
                  :color="activity.color"
                  :timestamp="activity.timestamp"
                >{{activity.content}}</el-timeline-item>
              </el-timeline>
            </div>

            <!-- 全国行业总决赛 专业赛事-->
            <el-tabs v-model="activeName" @tab-click="handleClick" type="card">
              <el-tab-pane label="全国行业总决赛" name="first">
                <div class="quanguo-game-wrapper">
                  <div class="quanguo-game-item">生物医药</div>
                  <div class="quanguo-game-item">电子信息</div>
                  <div class="quanguo-game-item">新能源及节能环保</div>
                  <div class="quanguo-game-item">互联网</div>
                  <div class="quanguo-game-item">新材料</div>
                  <div class="quanguo-game-item">先进制造</div>
                </div>
              </el-tab-pane>
              <el-tab-pane label="专业赛事" name="second">
                <div class="quanguo-game-wrapper">
                  <div class="quanguo-game-item">生物医药</div>
                  <div class="quanguo-game-item">电子信息</div>
                  <div class="quanguo-game-item">新能源及节能环保</div>
                  <div class="quanguo-game-item">互联网</div>
                  <div class="quanguo-game-item">新材料</div>
                  <div class="quanguo-game-item">先进制造</div>
                </div>
              </el-tab-pane>
            </el-tabs>

            <!-- 大企业需求对接 -->
            <div style="padding-top:20px;">
              <NaviTitle title="大企业需求对接"></NaviTitle>
            </div>

            <div class="big-business">
              <div class="big-business-item"></div>
              <div class="big-business-item"></div>
              <div class="big-business-item"></div>
              <div class="big-business-item"></div>
            </div>
          </div>
          <!-- 中间内容 ------------------------------->
          <div class="center_content">
            <!-- 大赛新闻 -->
            <NaviTitle title="大赛新闻"></NaviTitle>
            <div class="top-news">
              <div class="top-news-image"></div>
              <div style="padding-left:13px;">
                <div class="news-title">江阴|2019年中国江阴（高新区）创新 创业大赛总决赛即将</div>
                <div class="news-desc">以特钢新材料及制品、微电子集成电路、现代中药和生物医药、机械智能制造等高层次产.....</div>
                <div class="news-footer">
                  <div class="news-footer-source">来源：江阴高新区</div>
                  <div class="news-footer-time">2019-05-22</div>
                </div>
              </div>
            </div>
            <div class="short-news">
              <div class="short-news-item">广西|第八届中国创新创业大赛广西赛区暨2019年广西创新创业大赛正式启动</div>
              <div class="short-news-item">第八届中国创新创业大赛江苏赛区</div>
              <div class="short-news-item">广州|第八届中国创新创业大赛（广东﹒广州赛区）正式启航，大湾区科技创新服....</div>
              <div class="short-news-item">大连|吹响创新创业创投集结号，第八届中国创新创业大赛（大连赛区）暨第......</div>
              <div class="short-news-item">河北|第八届中国创新创业大赛（河北赛区）暨第七届河北省创新创业大赛正式启动</div>
            </div>
            <!-- 地方赛动态 -->
            <div style="padding-top:20px;">
              <NaviTitle title="地方赛动态"></NaviTitle>
            </div>
            <div class="top-news">
              <div class="top-news-image"></div>
              <div style="padding-left:13px;">
                <div class="news-title">江阴|2019年中国江阴（高新区）创新 创业大赛总决赛即将</div>
                <div class="news-desc">以特钢新材料及制品、微电子集成电路、现代中药和生物医药、机械智能制造等高层次产.....</div>
                <div class="news-footer">
                  <div class="news-footer-source">来源：江阴高新区</div>
                  <div class="news-footer-time">2019-05-22</div>
                </div>
              </div>
            </div>
            <div class="short-news">
              <div class="short-news-item">广西|第八届中国创新创业大赛广西赛区暨2019年广西创新创业大赛正式启动</div>
            </div>

            <!-- 赛友捷报 -->
            <div style="padding-top:20px;">
              <NaviTitle title="赛友捷报"></NaviTitle>
            </div>
            <div class="top-news">
              <div class="top-news-image"></div>
              <div style="padding-left:13px;">
                <div class="news-title">江阴|2019年中国江阴（高新区）创新 创业大赛总决赛即将</div>
                <div class="news-desc">以特钢新材料及制品、微电子集成电路、现代中药和生物医药、机械智能制造等高层次产.....</div>
                <div class="news-footer">
                  <div class="news-footer-source">来源：江阴高新区</div>
                  <div class="news-footer-time">2019-05-22</div>
                </div>
              </div>
            </div>
            <div class="short-news">
              <div class="short-news-item">广西|第八届中国创新创业大赛广西赛区暨2019年广西创新创业大赛正式启动</div>
            </div>
          </div>
        </div>
        <div style="padding-top:20px;padding-right:20px;">
          <NaviTitle title="项目直通车 "></NaviTitle>
        </div>
        <div class="project-items">
          <div class="project-item">
            <img class="project-item-logo" src="http://qnimage.xiteng.com/p_7@2x.png">
            <div class="project-item-title">“花开花落”创意有限责任公司</div>
          </div>
          <div class="project-item">
            <img class="project-item-logo" src="http://qnimage.xiteng.com/p_7@2x.png">
            <div class="project-item-title">第三创意人力资源有限公司</div>
          </div>
          <div class="project-item">
            <img class="project-item-logo" src="http://qnimage.xiteng.com/p_7@2x.png">
            <div class="project-item-title">”濠江映画“特色手工画舫商 业计划书</div>
          </div>
          <div class="project-item">
            <img class="project-item-logo" src="http://qnimage.xiteng.com/p_7@2x.png">
            <div class="project-item-title">”濠江映画“特色手工画舫商 业计划书</div>
          </div>
        </div>
      </div>

      <!-- 右侧内容 ------------------------------->
      <div class="right_list">
        <div class="login-wrapper">
          <!-- 参赛登录 -->
          <div class="game_login">参赛登录</div>
          <!-- 工作登录 -->
          <div class="game_login">工作登录</div>

          <!-- 报名热线 -->
          <div class="login-desc-wrapper">
            <div class="login-desc">报名热线</div>
            <div class="login-desc">010-88656381/6382/6219</div>
            <div class="login-desc">技术支持</div>
            <div class="login-desc">010-88656381/6382/6219</div>
            <div class="login-desc-blue">联系我们</div>
            <div class="login-desc-blue">地方赛事咨询方式</div>
            <div class="login-desc-blue">常见问题解答</div>
          </div>
        </div>
        <NaviTitle title="众扶平台"></NaviTitle>

        <div class="fuzhong-items">
          <img src="http://qnimage.xiteng.com/P_10@2x.png" alt>
          <img src="http://qnimage.xiteng.com/P_10@2x.png" alt>
          <img src="http://qnimage.xiteng.com/P_10@2x.png" alt>
          <img src="http://qnimage.xiteng.com/P_10@2x.png" alt>
        </div>

        <!-- 合作伙伴 -->
        <div style="padding-top:20px;padding-right:20px;">
          <NaviTitle title="合作伙伴 "></NaviTitle>
        </div>
        <div class="partners">
          <img src="http://qnimage.xiteng.com/logo_7@2x.png" alt>
          <img src="http://qnimage.xiteng.com/logo_8@2x.png" alt>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import NaviTitle from "@/components/common/NaviTitle.vue";
export default {
  data() {
    return {
      activeName: "first",
      reverse: true,
      activities: [
        {
          timestamp: "科技部关于举办第八届中国创新创业大赛的通知",
          color: "#AFC3D4"
        },
        {
          timestamp: "科技部火炬中心关于组织第七届中国创新创业大赛优秀企业",
          color: "#AFC3D4"
        },
        {
          timestamp: "关于对第七届中国创新创业大赛优秀组织单位进行表彰的通知",
          color: "#AFC3D4"
        },
        {
          timestamp: "科技部火炬中心关于组织第七届中国创新创业大赛优秀企业",
          color: "#AFC3D4"
        },
        {
          timestamp: "关于对第七届中国创新创业大赛优秀组织单位进行表彰的通知",

          color: "#1479D7"
        },
        {
          timestamp: "科技部火炬中心关于组织第七届中国创新创业大赛优秀企业",

          color: "#AFC3D4"
        }
      ]
    };
  },
  components: {
    NaviTitle
  }
};
</script>

<style scoped>
.main_content {
  width: 1048px;
  display: flex;
  flex-direction: row;
  margin: auto;
  padding-top: 15px;
}

.index_content {
  display: flex;
  flex-direction: row;
  width: 1048px;
  /* height: 845px; */
}

.fuzhong-items > img {
  width: 196px;
  height: 98px;
  margin-top: 10px;
}

.main-left {
  display: flex;
  flex-direction: row;
}

.content_left {
  flex: 1;
  /* background-color: blue; */
}

.partners > img {
  width: 117px;
  height: 36px;
  margin-left: 38px;
  margin-top: 43px;
}

.meiti-items {
  display: flex;
  flex-direction: row;
}

.quanguo-game-wrapper {
  width: 388px;
  height: 140px;

  border-top: solid 2px #53a8e8;
  border-left: solid 1px #c9dff2;
  border-right: solid 1px #c9dff2;
  border-bottom: solid 1px #c9dff2;

  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  /* justify-content: space-around; */
  padding: 16px 17px;
  box-sizing: border-box;
}

.partners {
  width: 186px;
  height: 211px;
  background: rgba(255, 255, 255, 1);
  border: 1px solid rgba(237, 237, 237, 1);
  box-shadow: 0px 1px 5px 0px rgba(0, 0, 0, 0.07);
  border-radius: 3px;
}

.news-footer {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  padding-top: 10px;
  box-sizing: border-box;
}

.news-footer-source {
  /* width:83px;
height:11px; */
  font-size: 11px;
  font-family: SimSun;
  font-weight: 400;
  color: rgba(83, 168, 232, 1);
  /* line-height:18px; */
}

.news-footer-time {
  font-size: 11px;
  font-family: SimSun;
  font-weight: 400;
  color: rgba(153, 153, 153, 1);
  line-height: 18px;
}

.news-title {
  /* width:206px;
height:30px; */
  font-size: 12px;
  font-family: SimSun;
  font-weight: bold;
  color: rgba(50, 50, 50, 1);
  /* line-height:18px; */
}
.news-desc {
  font-size: 9px;
  font-family: SimSun;
  font-weight: 400;
  color: rgba(153, 153, 153, 1);
  margin-top: 16px;
}

.big-business {
  width: 388px;
  height: 129px;

  border-top: solid 2px #53a8e8;
  border-left: solid 1px #c9dff2;
  border-right: solid 1px #c9dff2;
  border-bottom: solid 1px #c9dff2;

  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.quanguo-game-item {
  /* width: 86px; */
  height: 33px;
  background: rgba(238, 238, 238, 1);
  border-radius: 3px;
  color: #1f1f1f;
  font-size: 11px;
  text-align: center;
  padding: 0px 20px;
  box-sizing: border-box;
  margin: 5px 6px;
  line-height: 33px;
}

.big-business {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  padding: 26px 16px;
  box-sizing: border-box;
}

.big-business-item {
  height: 30px;
  width: 87px;
  border: dashed 1px #333;
  margin-bottom: 16px;
  margin-right: 10px;
}

.center_content {
  flex: 1;
  /* background-color: aqua; */
  /* height: 300px; */
  padding: 0 30px;
}

.project-items {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding-top: 10px;
}

ul {
  padding-inline-start: 0px;
}

.project-item {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  width: 195px;
  height: 192px;
  margin-right: 14px;
}

.project-item-logo {
  width: 194px;
  height: 138px;
}
.project-item-title {
  font-size: 12px;
  font-family: MicrosoftYaHei;
  font-weight: 400;
  color: rgba(31, 31, 31, 1);
  padding-top: 19px;
  text-align: center;
  height: 30px;
}

.short-news {
  margin-top: 20px;
}

.short-news-item {
  /* width: 391px;
  height: 107px; */
  font-size: 11px;
  font-family: SimSun;
  font-weight: 400;
  color: rgba(50, 50, 50, 1);

  display: -webkit-box;

  -webkit-box-orient: vertical;

  -webkit-line-clamp: 1;

  overflow: hidden;
  line-height: 30px;
}

.top-news {
  display: flex;
  flex-direction: row;
  width: 100%;
  padding-top: 10px;
}

.top-news-image {
  width: 185px;
  height: 110px;
  background: url("http://qnimage.xiteng.com/p_2@2x.png") no-repeat center;
  background-size: 185px 110px;
}
.right_list {
  width: 200px;
  display: flex;
  flex-direction: column;
}

.gg1 {
  padding-right: 16px;
  box-sizing: border-box;
}

.gg1 img {
  width: 185px;
  height: 110px;
}

.meiti-item-desc {
  /* width:167px; */
  /* height:29px; */
  font-size: 11px;
  font-family: SimSun;
  font-weight: 400;
  color: rgba(50, 50, 50, 1);
  line-height: 18px;
}

.el-step__title {
  font-size: 12px;
}

.login-wrapper {
  width: 196px;
  height: 270px;

  border-top: solid 2px #53a8e8;
  border-left: solid 1px #c9dff2;
  border-right: solid 1px #c9dff2;
  border-bottom: solid 1px #c9dff2;
}

.game_login {
  width: 158px;
  height: 33px;
  background: rgba(83, 168, 232, 1);
  border-radius: 3px;
  color: #ffffff;
  text-align: center;
  line-height: 33px;

  margin-top: 13px;
  margin-left: 15px;
}

.login-desc-wrapper {
  padding: 16px;
  box-sizing: border-box;
}

.login-desc {
  color: #333333;
  font-size: 11px;
  margin-bottom: 8px;
}

.login-desc-blue {
  color: #53a8e8;
  font-size: 11px;
}
</style>
