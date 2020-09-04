<template>
  <div id="mainview">
    <div class="img"></div>
    <el-row>
      <el-col :span="14">
        <div class="grid-content bg-purple">
          <div class="classify">
            <ul>
              <li
                v-for="(item,index) in classify"
                @click="selete(index)"
                :class="{'selete':num === index}"
                :key="index"
              >{{item}}</li>
            </ul>
          </div>
        </div>
      </el-col>
      <el-col :span="5">
        <div class="grid-content bg-purple-light">
          <div class="search-btn">全部类型</div>
        </div>
      </el-col>
      <el-col :span="5">
        <div class="grid-content bg-purple">
          <div class="search">
            <el-input placeholder="请输入内容">
              <i slot="prefix" suffix-icon="el-input__icon" class="el-input__icon el-icon-search"></i>
            </el-input>
          </div>
        </div>
      </el-col>
    </el-row>
    <div class="two-list">
      <ul>
        <li>
          <div class="list">
            <div class="one-list">
              <div class="icon">
                <i class="el-icon-upload"></i>
              </div>
              <span>免费发布需求</span>
            </div>
          </div>
        </li>
        <li v-for="(item,index) in list" :key="index">
          <img v-if="item.img" src="../images/aaaa.png" />
          <span class="one-span">{{item.category}}</span>
          <p>{{item.label}}</p>
          <span class="time">{{item.time}}小时前</span>
          <span class="number">
            <i class="el-icon-view"></i>
            {{item.number}}
          </span>
          <span class="filament"></span>
          <div class="usericon">
            <i class="el-icon-user-solid"></i>
          </div>
          <span class="company-name">{{item.companyname}}</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      classify: ["全部", "需求", "服务"],
      num: 0,
      list: [
        {
          category: "需求",
          time: 2,
          number: 232,
          companyname: "知道科技",
          label: "发的发生的方式发生的方式发生的方式发生地方",
          img: true,
        },
        {
          category: "需求",
          time: 4,
          number: 2322,
          companyname: "DD科技",
          label: "发送到发送到发送到共和国回到家大酒店附近",
          img: true,
        },
        {
          category: "需求",
          time: 5,
          number: 354,
          companyname: "公告科技",
          label: "讽德诵功电饭锅水电费公司电饭锅十多个",
          img: false,
        },
        {
          category: "需求",
          time: 5,
          number: 354,
          companyname: "公告科技",
          label: "讽德诵功电饭锅水电费公司电饭锅十多个",
          img: false,
        },
        {
          category: "需求",
          time: 5,
          number: 354,
          companyname: "公告科技",
          label: "讽德诵功电饭锅水电费公司电饭锅十多个",
          img: false,
        },
        {
          category: "需求",
          time: 5,
          number: 354,
          companyname: "公告科技",
          label: "讽德诵功电饭锅水电费公司电饭锅十多个",
          img: false,
        },
      ],
    };
  },
  methods: {
    selete(index) {
      this.num = index;
    },
  },
};
</script>

<style scoped>
#mainview {
  position: fixed;
  left: 60px;
  background-color: #f5f6fa;
  top: 56px;
  right: 0;
  bottom: 0;
  overflow: auto;
}
#mainview .search {
  position: absolute;
  right: 30px;
  height: 40px;
  width: 280px;
}
#mainview .list {
  width: 200px;
}
#mainview .img {
  height: 180px;
  background-color: red;
  margin: 15px 30px;
  border-radius: 25px;
  background-image: url("../images/main.png");
  background-size: 100% 100%;
}
#mainview .classify {
  display: inline-block;
  width: 248px;
  margin-left: 30px;
  background-color: #fff;
  border-radius: 25px;
  line-height: 42px;
  text-align: center;
  box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);
  cursor: pointer;
}
#mainview .classify li {
  display: inline;
  list-style-type: none;
  border-radius: 25px;
  color: #1f28cf;
  padding: 2px 10px;
  margin: auto 3px;
  cursor: pointer;
}
.selete {
  background-color: #1f28cf;
  color: #fff !important;
}
#mainview .search-btn {
  border-radius: 25px;
  color: #1f28cf;
  width: 100px;
  height: 42px;
  border-radius: 25px;
  background-color: #fff;
  text-align: center;
  line-height: 42px;
  box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);
  cursor: pointer;
}
#mainview .list .icon {
  width: 90px;
  height: 90px;
  border-radius: 50%;
  font-size: 55px;
  background-color: #1f28cf;
  color: #fff;
  text-align: center;
  line-height: 90px;
  margin: 10px auto;
}
#mainview span {
  font-size: 12px;
  color: #1f28cf;
}

#mainview .two-list li {
  display: inline-block;
  position: relative;
  margin-left: 30px;
  margin-top: 30px;
  width: 180px;
  height: 135px;
  border-radius: 10px;
  text-align: center;
  overflow: hidden;
  box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);
  transition: all 1s;
  cursor: pointer;
}
#mainview .two-list img {
  position: absolute;
  top: -1px;
  right: -2px;
}
#mainview .two-list .one-span {
  position: absolute;
  top: 10px;
  left: 10px;
  background-color: #1f28cf;
  color: #fff;
  border-radius: 10px;
  padding: 5px 15px;
}
#mainview .two-list p {
  font-size: 16px;
  position: absolute;
  top: 50px;
  left: 10px;
  width: 160px;
  height: 32px;
  color: #0a1633;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  text-align: left;
}
#mainview .two-list .time {
  position: absolute;
  left: 10px;
  bottom: 35px;
  font-size: 12px;
  color: #6c7a8e;
}
#mainview .two-list .number {
  position: absolute;
  bottom: 35px;
  right: 10px;
  color: #6c7a8e;
}
#mainview .two-list .filament {
  position: absolute;
  bottom: 27px;
  left: 10px;
  display: block;
  background-color: #6c7a8e;
  height: 1px;
  width: 160px;
}
#mainview .two-list .usericon {
  position: absolute;
  left: 10px;
  bottom: 5px;
  border-radius: 50%;
  background-color: #1f28cf;
  font-size: 18px;
  color: #fff;
}
#mainview .two-list .company-name {
  position: absolute;
  left: 45px;
  bottom: 8px;
  color: #6c7a8e;
}
#mainview .two-list li:hover {
  transform: translateY(-20px);
}
</style>
