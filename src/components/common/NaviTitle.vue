<template>
  <div class="nav-wrapper">
    <div class="nav">
      <div class="top">
        <div class="v-line"></div>
        <div class="nav-name">大赛新闻</div>
      </div>
      <div class="more"></div>
    </div>
    <div class="nav-botline"></div>
  </div>
</template>

<script>
export default {
  name: "foot"
};
</script>

<style scoped>
.nav-wrapper {
  display: flex;
  flex-direction: column;
  width: 100%;
}
.nav {
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 30px;
}
.nav-botline {
  width: 260px;
  height: 1px;
  background: rgba(237, 237, 237, 1);
}

.more {
  width: 21px;
  height: 6px;
  font-size: 7px;
  font-family: MicrosoftYaHei;
  font-weight: 400;
  color: rgba(20, 121, 215, 1);
  line-height: 12px;
}

.top {
  display: flex;
  flex-direction: row;
  align-items: center;
}

.v-line {
  width: 3px;
  height: 11px;
  background: rgba(20, 121, 215, 1);
}

.nav-name {
  margin-left: 7px;
  height: 10px;
  font-size: 10px;
  font-family: MicrosoftYaHei;
  font-weight: 400;
  color: rgba(20, 121, 215, 1);
  line-height: 12px;
}
</style>
