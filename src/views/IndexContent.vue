<template>
  <div class="main_content">
    <div class="index_content">
      <!-- 左侧面板 -->
      <div class="content_left">
        <!-- 媒体聚焦 -->
        <NaviTitle></NaviTitle>
      </div>

      <!-- 中间内容 -->
      <div class="center"></div>

      <!-- 右侧内容 -->
      <div class="right_list"></div>
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
.header {
  width: 100%;
  height: 90px;
  background: #42b9bd;
}
.index_content {
  display: flex;
  flex-direction: row;
  width: 1048px;
}

.content_left {
  flex: 1;
}

.content_contact {
  width: 260px;
  background: #f4f4f4;
  padding: 48px 0 48px 20px;
  margin-bottom: 30px;
}

.center {
  flex: 1;
}
.right_list {
  width: 300px;
  display: flex;
  flex-direction: columns;
  background: #ffffff;
  /* height: 100%; */
}

.btn_login {
  width: 280px;
  height: 60px;
  border-radius: 5px;
  background: #4268bd;
  line-height: 60px;
  text-align: center;
  color: #fff;
  font-size: 22px;
  margin-bottom: 15px;
  box-shadow: 0px 0px 3px #4268bd;
}

.btn_work_login {
  margin-top: 30px;
  width: 280px;
  height: 60px;
  border-radius: 5px;
  background: #42b9bd;
  line-height: 60px;
  text-align: center;
  color: #fff;
  font-size: 22px;
  margin-bottom: 15px;
  box-shadow: 0px 0px 3px #42b9bd;
}

.bmrx {
  width: 280px;
  background: #f4f4f4;
  padding: 48px 0 48px 20px;
  margin-bottom: 30px;
}
.bmrx span {
  display: block;
  color: #333333;
  font-size: 16px;
  line-height: 31px;
}
.bmrx .jiacu {
  font-weight: 600;
}
.bmrx .jiacu a {
  color: #333333;
  font-size: 16px;
}
.BT {
  display: block;
  width: 280px;
  height: 46px;
  line-height: 46px;
  background: url(http://www.cxcyds.com/cxcyds/xhtml/images/dsgg.png) no-repeat;
  background-size: 280px 46px;
  text-indent: 23px;
  font-size: 16px;
  color: #fff;
  margin-bottom: 20px;
  font-weight: 800;
}
.dsgg_nr {
  padding: 0px 24px;
  padding-top: 20px;
  border: 1px solid #e1e1e1;
  margin-bottom: 30px;
}
.ggnr img {
  display: inline-block;
  margin-bottom: 2px;
}

.dsgg_nr {
  padding: 0px 24px;
  padding-top: 20px;
  border: 1px solid #e1e1e1;
  margin-bottom: 30px;
}
.ggnr img {
  display: inline-block;
  margin-bottom: 2px;
}
.ggnr .hd {
  color: #5ea600;
}
.ggnr div {
  display: inline-block;
  width: 203px;
  float: right;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;
  overflow: hidden;
  margin-bottom: 20px;
  font-weight: 800;
  cursor: pointer;
  font-size: 14px;
  color: #333;
}

.ztc_wrapper {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  margin-bottom: 20px;
}

.ztc_des {
  color: #333;
}

.ztc_des span {
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.ztc {
  width: 120px;
  margin-left: 10px;
}

.ztc img {
  width: 120px;
  height: 160px;

  overflow: hidden;
}

.center .BTMAIN {
  position: relative;
  width: 574px;
  height: 40px;
  background: url(http://www.cxcyds.com/cxcyds/xhtml/images/BT_MAIN.png)
    no-repeat;
  background-size: 574px 40px;
  margin-bottom: 20px;
}
.BT_TEXT {
  font-size: 16px;
  color: #fff;
  position: absolute;
  top: 11px;
  left: 11px;
  font-weight: 800;
}
.BT_MORE {
  display: block;
  position: absolute;
  width: 43px;
  height: 10px;
  top: 13px;
  right: 0;
}

.gg1 {
  width: 280px;
  height: 191px;
  margin-right: 14px;
  display: inline-block;
  position: relative;
  float: left;
  cursor: pointer;
}
.gg1 img {
  display: block;
  width: 280px;
  height: 191px;
}
.wenzi1 {
  width: 242px;
  height: 33px;
  padding: 10px 19px;
  font-size: 12px;
  color: #fff;
  position: absolute;
  bottom: 0;
  line-height: 20px;
  background: #88bd42;
  opacity: 0.3;
}
.gg1 span {
  width: 242px;
  height: 33px;
  padding: 10px 19px;
  font-size: 12px;
  color: #fff;
  position: absolute;
  bottom: 0;
}
.gg2 {
  width: 280px;
  height: 191px;
  display: inline-block;
  position: relative;
  cursor: pointer;
}
.gg2 img {
  display: block;
  width: 280px;
  height: 191px;
}
.gg2 span {
  width: 242px;
  height: 33px;
  padding: 10px 19px;
  font-size: 12px;
  color: #fff;
  position: absolute;
  bottom: 0;
}
.wenzi2 {
  width: 242px;
  height: 33px;
  padding: 10px 19px;
  font-size: 12px;
  color: #fff;
  position: absolute;
  bottom: 0;
  line-height: 20px;
  background: #88bd42;
  opacity: 0.3;
}
.GGTP {
  margin-bottom: 20px;
}

.XINWEN_LIST {
  padding-bottom: 18px;
  border-bottom: 1px dashed #ccc;
  position: relative;
  margin-bottom: 20px;
  cursor: pointer;
}
.XINWEN_LIST2 {
  padding-bottom: 18px;
  border-bottom: 1px dashed #ccc;
  position: relative;
  margin-bottom: 20px;
  cursor: pointer;
  min-height: 167px;
}
.XINWEN_LIST3 {
  padding-bottom: 18px;
  border-bottom: 1px dashed #ccc;
  position: relative;
  margin-bottom: 20px;
  cursor: pointer;
}
.xinwen1 {
  display: inline-block;
  width: 138px;
  height: 106px;
  margin-bottom: 18px;
}
.xinwen_bt {
  font-size: 14px;
  color: #333333;
  display: inline-block;
  width: 390px;
  position: absolute;
  top: 0;
  right: 10px;
  line-height: 20px;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;
  overflow: hidden;
  font-weight: 800;
}
.xinwen_nr {
  line-height: 18px;
  display: inline-block;
  font-size: 12px;
  color: #999999;
  width: 390px;
  position: absolute;
  top: 50px;
  right: 10px;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;
  overflow: hidden;
}
.data {
  font-size: 12px;
  color: #cccccc;
  position: absolute;
  bottom: 18px;
  right: 0px;
}

.zan {
  font-size: 12px;
  color: #cccccc;
  margin-right: 15px;
}

.yan {
  font-size: 12px;
  color: #cccccc;
  margin-right: 15px;
}

.wenben {
  font-size: 12px;
  color: #cccccc;
}
.xinwen_caozuo {
}
.from span {
  font-size: 12px;
  display: inline-block;
}
.from {
  position: absolute;
  bottom: 18px;
  left: 363px;
}
.right_list {
  width: 280px;
  display: inline-block;
  float: right;
}
.right_bt {
  width: 280px;
  height: 46px;
  background: url(http://www.cxcyds.com/cxcyds/xhtml/images/280bk.png) no-repeat;
  background-size: 280px 46px;
  line-height: 46px;
  text-indent: 23px;
  font-size: 16px;
  color: #fff;
  margin-bottom: 22px;
  font-weight: 800;
}
.pt_list img {
  display: block;
  height: 148px;
  width: 280px;
  margin-bottom: 20px;
}
.xq_list img {
  display: block;
  height: 111px;
  width: 280px;
  margin-bottom: 20px;
}
.BT_MORE2 {
  display: inline-block;
  width: 43px;
  height: 10px;
  margin-left: 118px;
  top: 13px;
  right: 0;
}
.tab_hz_sb {
  display: block;
}

.tab_hz_sb li {
  width: 133px;
  height: 48px;
  float: left;
  margin-right: 5px;
  margin-bottom: 20px;
}

.tab_hz_sb li a img {
  display: block;
  width: 133px;
  height: 48px;
  border: 1px solid #ebebeb;
}
</style>
