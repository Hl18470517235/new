<template>
  <div id="nav">
    <img class="logo" src="../images/logo.png" alt />
    <div class="nav-icon">
      <el-menu
        default-active="0"
        boolean:false
        @open="handleOpen"
        @close="handleClose"
        class="el-menu-vertical-demo"
        background-color="#232a34"
        text-color="#fff"
        active-text-color="#fff"
      >
        <el-menu-item
          v-for="(item,id) in navitem"
          :key="id"
          @click="selete(id)"
          :index="id + ''"
        >
          <div :class="{'triangle':num === id}"></div>
          <i :class="item.icon"></i>
          <span class="title">{{item.title}}</span>
        </el-menu-item>
      </el-menu>
      <span class="span"></span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 0,
      navitem: [
        {
          icon: "el-icon-setting",
          title: "大厅",
        },
        {
          icon: "el-icon-user",
          title: "关注",
        },
        {
          icon: "el-icon-user",
          title: "发布",
        },
        {
          icon: "el-icon-help",
          title: "入驻",
        },
        {
          icon: "el-icon-setting",
          title: "客服",
        },
      ],
    };
  },
  methods: {
    selete(id) {
      this.num = id;
    },
    handleOpen() {},
    handleClose() {},
  },
};
</script>

<style scoped>
#nav {
  position: fixed;
  top: 0;
  left: 0;
  height: 100vh;
  width: 60px;
  background-color: #232a34;
}
#nav .logo {
  height: 55px;
  width: 60px;
  background-color: #fff;
}
#nav .nav-icon {
  margin-top: 35px;
}
.nav-icon li {
  background-color: #232a34;
}
.nav-icon li i {
  display: block;
  padding-top: 5px;
}
.nav-icon li span {
  color: #424a57;
}
#nav .span {
  position: absolute;
  display: block;
  top: 60px;
  left: 59px;
  height: 100vh;
  width: 1px;
  background-color: #232a34;
}
#nav .triangle {
  display: block;
  position: absolute;
  top: 15px;
  left: 60px;
  border-top: 10px solid transparent;
  border-right: 10px solid transparent;
  border-bottom: 10px solid transparent;
  border-left: 10px solid #232a34;
}
#nav .title {
  position: absolute;
  top: 5px;
  font-size: 12px;
}
</style>