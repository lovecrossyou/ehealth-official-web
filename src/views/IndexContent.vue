<template>
  <div class="main_content">
    <div class="index_content">
      <!-- 左侧面板 -->
      <div class="content_left">
        <!-- 媒体聚焦 -->
        <div>
          <NaviTitle title="媒体聚焦"></NaviTitle>
        </div>

        <div class="meiti-items">
          <div href="/cxcyds/jdxw/201905/ded81ead002d442d9049064693551016.shtml" target="_blank">
            <div class="gg1 gg">
              <img
                src="http://www.cxcyds.com/cxcyds/jdxw//201905/ded81ead002d442d9049064693551016/images/9c9b727727754478a843d7e8919bf0b7.png"
              >
              <div class="meiti-item-desc">2019第八届中国创新创业大赛国际第 三代半导体专业正式启动</div>
            </div>
          </div>
          <div href="/cxcyds/jdxw/201905/ded81ead002d442d9049064693551016.shtml" target="_blank">
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
          <el-steps direction="vertical">
            <el-step title="科技部关于举办第八届中国创新创业大赛的通知  " icon="el-icon-loading"></el-step>
            <el-step title="科技部火炬中心关于组织第七届中国创新创业大赛优秀企业" icon="el-icon-loading"></el-step>
            <el-step title="关于对第七届中国创新创业大赛优秀组织单位进行表彰的通知  " description icon="el-icon-loading"></el-step>
            <el-step title="第七届中国创新创业大赛新材料行业总决赛获奖及优秀企业名单公示" icon="el-icon-loading"></el-step>
            <el-step title="第七届中国创新创业大赛生物医药行业总决赛获奖及优秀企业名单公示" icon="el-icon-loading"></el-step>
            <el-step title="第七届中国创新创业大赛生物医药行业总决赛获奖及优秀企业名单公示" icon="el-icon-loading"></el-step>
          </el-steps>
        </div>

        <!-- 全国行业总决赛 专业赛事-->
        <div class="quanguo-game-wrapper">
          <div class="quanguo-game-item">生物医药</div>
          <div class="quanguo-game-item">电子信息</div>
          <div class="quanguo-game-item">新能源及节能环保</div>
          <div class="quanguo-game-item">互联网</div>
          <div class="quanguo-game-item">新材料</div>
          <div class="quanguo-game-item">先进制造</div>
        </div>

        <!-- 大企业需求对接 -->
        <div style="padding-top:20px;">
          <NaviTitle title="大企业需求对接"></NaviTitle>
        </div>
      </div>

      <!-- 中间内容 -->
      <div class="center_content">
        <NaviTitle title="大赛新闻"></NaviTitle>
      </div>

      <!-- 右侧内容 -->
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
      </div>
    </div>
  </div>
</template>

<script>
import NaviTitle from "@/components/common/NaviTitle.vue";
export default {
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
  /* padding: 0 195px; */
}

.index_content {
  display: flex;
  flex-direction: row;
  width: 1048px;
}

.content_left {
  flex: 1;
  /* background-color: blue; */
}

.meiti-items {
  display: flex;
  flex-direction: row;
}

.quanguo-game-wrapper {
  width: 388px;
  height: 97px;

  border-top: solid 2px #53a8e8;
  border-left: solid 1px #c9dff2;
  border-right: solid 1px #c9dff2;
  border-bottom: solid 1px #c9dff2;

  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  /* justify-content: space-around; */
  padding: 6px 17px;
  box-sizing: border-box;
}

.quanguo-game-item {
  /* width: 86px; */
  height: 33px;
  background: rgba(238, 238, 238, 1);
  border-radius: 3px;
  color: #1f1f1f;
  font-size: 11px;
  text-align: center;
  padding: 10px 20px;
  box-sizing: border-box;
  margin: 4px 6px;
  /* line-height: 13px; */
}

.center_content {
  flex: 1;
  /* background-color: aqua; */
  height: 300px;
  padding: 0 30px;
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
