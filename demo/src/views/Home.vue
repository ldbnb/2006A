<template>
  <div class="home">
    <!-- 头 -->
    <div class="header">
      <div>
        <img src="" alt="" />
        <span class="ft">王明伟医生</span>
      </div>
      <div></div>
      <div class="code">二维码</div>
    </div>

    <!-- 绿盒子 -->
    <div class="box">
      <div class="label">
        <div>
          <p>已签约人数</p>
          <h2>1000</h2>
        </div>
        <div>
          <p>待签约人数</p>
          <h2>20</h2>
        </div>
        <div>
          <p>居民总数</p>
          <h2>1020</h2>
        </div>
      </div>
      <div class="label">
        <div>
          <p>待处理服务器</p>
          <h2>10</h2>
        </div>
        <div>
          <p>服务总量</p>
          <h2>100</h2>
        </div>
        <div>
          <p>服务评价</p>
          <h2>439</h2>
        </div>
      </div>
    </div>
    <!-- 标签头 -->
    <div class="box2">
      <div style="background-color: #0a71f2;" @click="archives">
        <div></div>
        <p>新建档案</p>
      </div>
      <div style="background-color: #fdd885;">
        <div></div>
        <p>签约管理</p>
      </div>
      <div style="background-color: #f47270;">
        <div></div>
        <p>服务管理</p>
      </div>
    </div>

    <div class="asd"></div>

    <!-- 签约申请 -->
    <div class="application">
      <h3>签约申请（3）</h3><span>查看全部></span></span>
    </div>

    <!-- 用户列表 -->
    <div class="user">
      <div class="user1">
        <div class="ft">王小明</div>
        <div class="aa">58岁</div>
        <img src="../assets/logo.png" alt="" class="aa">
        <div class="a2">待审核</div>
      </div>
      <div class="user2">
        <div>身份证号</div><span class="sp"></span>
        <div>123546465465456</div>
      </div>
      <div class="user2">
        <div>签约团队</div><span class="sp"></span>
        <div>李明明团队</div>
      </div>
      <div class="user2">
        <div>服务包</div><span class="sp"></span>
        <div>老年人服务包</div>
      </div>
    </div>

    <!-- 服务申请 -->
    <div class="application">
      <h3>服务申请（8）</h3><span>查看全部></span></span>
    </div>
    <div class="user">
      <div class="user1">
        <div class="ft">王小明</div>
        <div class="aa">58岁</div>
        <input type="button" value="机构门诊" class="jgmz">
        <div class="a3">待审核</div>
      </div>
      <div class="user2">
        <div>服务包</div><span class="sp"></span>
        <div>老年服务包</div>
      </div>
      <div class="user2">
        <div>服务项目</div><span class="sp"></span>
        <div>高血压健康随访</div>
      </div>
      <div class="user2">
        <div>申请时间</div><span class="sp"></span>
        <div>2020/09/09 10:09:09</div>
      </div>
    </div>






  </div>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  methods: {
    archives() {
      this.$router.push("/Archives")
    }
  },
};
</script>
<style lang="scss">
body {
  background-color: #f6f9fe;
}

.header {
  display: flex;

  div {
    flex: 1;
  }

  .code {
    text-align: center;
  }


}

.ft {
  font-weight: 900;
  font-size: 19px;
}

.box {
  width: 100%;
  height: 255px;
  background-color: #52d5b6;
  margin-top: 30px;
  border-radius: 30px;

  .label {
    display: flex;

    div {
      flex: 1;
      text-align: center;
      color: #fff;
    }
  }
}

.box2 {
  width: 100%;
  height: 175px;
  border-radius: 20px;
  position: relative;
  background-color: #ffffff;
  bottom: 50px;
  display: flex;

  div {
    margin: auto;
    border-radius: 19px;
    width: 64px;
    height: 64px;
  }
}

.asd {
  height: 25px;
  width: 100%;
  background-color: #fff;
  position: relative;
  bottom: 42px;
  height: 20px;
  width: 100%;
  background-color: #fff;
}

.application {
  background-color: #fff;
  bottom: 30px;
  position: relative;

  h3 {
    display: inline-block;

  }

  span {
    position: relative;
    left: 186px;
    color: #464646;
  }
}

.aa {
  margin-left: 17px;
  line-height: 30px;
}

.user {
  width: 100%;
  padding-top: 15px;
  height: 130px;
  background-color: #fff;
  position: relative;
  bottom: 40px;
  margin-top: 15px;


  .user1 {
    display: flex;
    width: 100%;

    h2 {
      display: inline-block;
    }

    img {
      width: 20px;
      height: 20px;
      margin-top: 5px;
    }

    .a2 {
      color: red;
      line-height: 30px;
      position: relative;
      left: 170px;
    }
  }

  .user2 {
    display: flex;
    line-height: 30px;
  }

}


.sp {
  width: 10px;
  height: 5px;
  ;
}

.jgmz {
  border: none;
  position: relative;
  background-color: #e2e4fd;
  color: #6c76f4;
  left: 15px;
}

.a3 {
  color: red;
  line-height: 30px;
  position: relative;
  left: 143px;
}
</style>
