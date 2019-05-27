<template>
  <div class="nav-wrapper">
    <div class="nav">
      <div class="top">
        <div class="v-line"></div>
        <div class="nav-name">{{title}}</div>
      </div>
      <div class="more">MORE</div>
    </div>
    <div class="nav-botline"></div>
  </div>
</template>

<script>
export default {
  name: "foot",
  props: ["title"]
};
</script>

<style scoped>
.nav-wrapper {
  display: flex;
  flex-direction: column;
  width: 100%;
  overflow: hidden;
  padding: 0 20px;
  box-sizing: border-box;
}
.nav {
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 30px;
  justify-content: space-between;
  width: 100%;
}
.nav-botline {
  width: 98%;
  height: 1px;
  background: rgba(237, 237, 237, 1);
}

.more {
  /* width: 21px; */
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

.more {
  height: 30px;
  font-size: 11px;
  font-family: MicrosoftYaHei;
  font-weight: 400;
  color: rgba(20, 121, 215, 1);
  line-height: 18px;
  padding-top: 10px;
}
</style>
