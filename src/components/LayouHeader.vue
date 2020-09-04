<template>
  <div id="header">
    <img class="left-img" src="../images/header.png" alt />
    <div class="right">
      <span class="font-color">加入会员</span>
      <i class="el-icon-star-on one-icon"></i>
      <span class="two-span font-color">认证企业</span>
      <i class="el-icon-phone-outline two-icon"></i>
        <i class="el-icon-user-solid usericon"></i>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
#header {
  position: fixed;
  height: 55px;
  background-color: #ffffff;
  top: 0;
  left: 60px;
  right: 0;
  line-height: 55px;
   box-shadow: 0 2px 12px 0 rgba(0, 0, 0, .4);
}
#header .one-icon {
  color: #fbf7a9;
}
#header .left-img {
  width: 140px;
  height: 33px;
  background-image: url("../images/header.png");
  background-size: 100% 100%;
  margin-left: 30px;
  margin-top: 12px;
}
.right {
  display: inline-block;
  position: fixed;
  top: 0;
  right: 30px;
}
#header .one-icon {
  height: 20px;
  width: 20px;
}
#header .two-icon {
  height: 30px;
  width: 30px;
}
#header .two-icon {
  margin: auto 10px;
  font-size: 20px;
}
.two-span {
  margin-left: 30px;
}
.font-color {
  color: #1f28cf;
  font-weight: 700px;
}
#header .usericon {
  border-radius: 50%;
  background-color: #1f28cf;
  font-size: 18px;
  color: #fff;
  margin-right: 30px;
}
</style>