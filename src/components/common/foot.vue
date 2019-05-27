<template>
  <footer class="footer_wrapper">
    <div class="footer_area">
      <div class="left_cont">
        <div>邮编：100045</div>
        <div>传真：88656371</div>
        <div>地址：北京市西城区三里河二区</div>
      </div>
      <div class="center_cont">
        <div>投诉电话：010-88656219</div>
        <div>投诉邮箱：shoul1@ctp.gov.cn</div>
        <div>报名咨询邮箱：bmzx@ctp.gov.cn</div>
      </div>
      <div class="right_cont">
        <div class="qr_code_area">
          <img src alt class="qr_code_img">
          <div class="bottom_text">大赛微信二维码</div>
        </div>
        <div class="qr_code_area">
          <img src alt class="qr_code_img">
          <div class="bottom_text">大赛微信二维码</div>
        </div>
      </div>
    </div>
    <div class="border_line"></div>
    <div class="copyright_area">
      Copyright @ 2012-2019中国创新创业大赛组委会 保留一切权利 京ICP备05034026号 京公网安备 11010202007133号
      关于我们 | 版权声明 | 联系方式
    </div>
  </footer>
</template>

<script>
</script>

<style scoped>
.footer_wrapper {
  width: 100%;
  height: 327px;
  background-color: #323232;
  margin-top: 35px;
  display: flex;
  flex-direction: column;
}
.footer_area {
  width: 710px;
  height: 229px;
  padding: 45px 0 32px 0;
  box-sizing: border-box;
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
.left_cont,
.center_cont {
  height: 72px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  color: #B7B7B7;
  font-size: 12px;
}
.right_cont {
  display: flex;
  flex-direction: row;
}
.qr_code_area {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-left: 35px;
}
.qr_code_img {
  width: 115px;
  height: 115px;
  background-color: #fff;
}
.bottom_text {
  color: #B7B7B7;
  font-size: 16px;
  margin-top: 18px;
}
.border_line {
  width: 100%;
  height: 1px;
  background-color: #565656;
}
.copyright_area {
  width: 710px;
  height: 98px;
  margin: 0 auto;
  color: #B7B7B7;
  font-size: 12px;
  text-align: center;
  padding: 25px 0;
  box-sizing: border-box;
  line-height: 28px;
}
</style>
