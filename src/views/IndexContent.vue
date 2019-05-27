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

        <div style="padding:10px 0;">
          <NaviTitle title="大赛公告"></NaviTitle>
        </div>
        <div style="height: 100px;">
          <el-steps direction="vertical" :active="1" space="20">
            <el-step title="科技部关于举办第八届中国创新创业大赛的通知  " icon="el-icon-loading"></el-step>
            <el-step title="科技部火炬中心关于组织第七届中国创新创业大赛优秀企业" icon="el-icon-loading"></el-step>
            <el-step title="关于对第七届中国创新创业大赛优秀组织单位进行表彰的通知  " description icon="el-icon-loading"></el-step>
            <el-step title="第七届中国创新创业大赛新材料行业总决赛获奖及优秀企业名单公示" icon="el-icon-loading"></el-step>
            <el-step title="第七届中国创新创业大赛生物医药行业总决赛获奖及优秀企业名单公示" icon="el-icon-loading"></el-step>
            <el-step title="第七届中国创新创业大赛生物医药行业总决赛获奖及优秀企业名单公示" icon="el-icon-loading"></el-step>
          </el-steps>
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
          <div>报名热线</div>
          <div>010</div>

          <div>报名热线</div>
          <div>报名热线</div>
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
}

.index_content {
  display: flex;
  flex-direction: row;
  width: 100%;
}

.content_left {
  flex: 1;
  /* background-color: blue; */
}

.meiti-items {
  display: flex;
  flex-direction: row;
}

.center_content {
  flex: 1;
  /* background-color: aqua; */
  height: 300px;
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
</style>
