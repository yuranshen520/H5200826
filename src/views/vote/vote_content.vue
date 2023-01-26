<template>
   <div class="primary">
      <div class="order">投票2</div>
      <div class="title">投票名称：是否同意***成为预备党员？</div>
      <div class="tag">
        <el-tag type="info">多选</el-tag>
        <el-tag type="info">匿名</el-tag>
        <el-tag type="info">最少选{{min}}项，最多选{{max}}项</el-tag>
      </div>
      <div v-if="flag" class="content">
          <br>
          <el-checkbox-group v-model="checkedCities" :min="min" :max="max">
            <el-checkbox v-for="city in cities" :label="city" :key="city">{{city}}</el-checkbox>
          </el-checkbox-group>
          <!-- <div>选中的结果是：{{checkedCities}}</div> -->
          <el-button type="primary" class="cfm" @click="confirmate" >确认投票</el-button>
          <div class="success" v-if="success !== null">
            <div class="loader">
              <div class="loader__bar"></div>
              <div class="loader__bar"></div>
              <div class="loader__bar"></div>
              <div class="loader__bar"></div>
              <div class="loader__bar"></div>
              <div class="loader__ball"></div>
            </div>
          </div>
      </div>
      <div v-else>
          <!-- 数据传递过来后，可以添加div,并使用v-for进行遍历 -->
          <br>
          <span>选项1</span>
          <el-progress :percentage="35"></el-progress>
          <span>选项2</span>
          <el-progress :percentage="25"></el-progress>
          <span>选项3</span>
          <el-progress :percentage="10"></el-progress>
          <span>选项4</span>
          <el-progress :percentage="30"></el-progress>
      </div>
   </div>
   
</template>

<script>
const cityOptions = ['上海', '北京', '广州', '深圳'];
export default {
    data() {
        return {
            checkedCities: [], //勾选的选项
            cities: cityOptions, //全部选项
            min: 1, // 最少勾选几项
            max: 3, // 最多勾选几项
            flag:true,
            success:null
      };
    },
    methods: {
        confirmate(){
            // 提交成功
            this.success = true
            setTimeout(()=>{
                this.success = null
                this.flag = false
            },1500)
            // 提交不成功
            // this.success = false         
        }
    }
}
</script>

<style lang="scss" scoped>
    .primary{
        position: relative;
    }
    .order{
        text-align: center;
        margin-top: 5px;
        font-size: 16px;
        font-weight: 600;
    }
    .title{
        text-align: center;
        margin-left: 10px;
        font-size: 15px;
    }
    .tag .el-tag{
        margin-left: 10px;
        height: 20px;
        line-height: 20px;
    }
    .content{
        position: relative;
    }
    .el-button{
        position: absolute;
        left: 50%;
        bottom: -50%;
        transform:translateX(-50%);
        z-index: 1;
    }
    .el-checkbox{
        display: block;
    }
    .success{
        position: absolute;
        background-color: rgb(126, 123, 113);
        left: 0%;
        top: -70%;
        width: 100%;
        height: 500px;
        opacity: 0.85;
        z-index: 2;
    }
    .loader {
  position: absolute;
  width: 75px;
  height: 100px;
  top: 15%;
  left: 43%;
  z-index: 3;
}

.loader__bar {
  position: absolute;
  bottom: 0;
  width: 10px;
  height: 50%;
  background: rgb(0, 0, 0);
  transform-origin: center bottom;
  box-shadow: 1px 1px 0 rgba(0, 0, 0, 0.2);
}

.loader__bar:nth-child(1) {
  left: 0px;
  transform: scale(1, 0.2);
  -webkit-animation: barUp1 4s infinite;
  animation: barUp1 4s infinite;
}

.loader__bar:nth-child(2) {
  left: 15px;
  transform: scale(1, 0.4);
  -webkit-animation: barUp2 4s infinite;
  animation: barUp2 4s infinite;
}

.loader__bar:nth-child(3) {
  left: 30px;
  transform: scale(1, 0.6);
  -webkit-animation: barUp3 4s infinite;
  animation: barUp3 4s infinite;
}

.loader__bar:nth-child(4) {
  left: 45px;
  transform: scale(1, 0.8);
  -webkit-animation: barUp4 4s infinite;
  animation: barUp4 4s infinite;
}

.loader__bar:nth-child(5) {
  left: 60px;
  transform: scale(1, 1);
  -webkit-animation: barUp5 4s infinite;
  animation: barUp5 4s infinite;
}

.loader__ball {
  position: absolute;
  bottom: 10px;
  left: 0;
  width: 10px;
  height: 10px;
  background: rgb(44, 143, 255);
  border-radius: 50%;
  -webkit-animation: ball624 4s infinite;
  animation: ball624 4s infinite;
}

@keyframes ball624 {
  0% {
    transform: translate(0, 0);
  }

  5% {
    transform: translate(8px, -14px);
  }

  10% {
    transform: translate(15px, -10px);
  }

  17% {
    transform: translate(23px, -24px);
  }

  20% {
    transform: translate(30px, -20px);
  }

  27% {
    transform: translate(38px, -34px);
  }

  30% {
    transform: translate(45px, -30px);
  }

  37% {
    transform: translate(53px, -44px);
  }

  40% {
    transform: translate(60px, -40px);
  }

  50% {
    transform: translate(60px, 0);
  }

  57% {
    transform: translate(53px, -14px);
  }

  60% {
    transform: translate(45px, -10px);
  }

  67% {
    transform: translate(37px, -24px);
  }

  70% {
    transform: translate(30px, -20px);
  }

  77% {
    transform: translate(22px, -34px);
  }

  80% {
    transform: translate(15px, -30px);
  }

  87% {
    transform: translate(7px, -44px);
  }

  90% {
    transform: translate(0, -40px);
  }

  100% {
    transform: translate(0, 0);
  }
}

@-webkit-keyframes barUp1 {
  0% {
    transform: scale(1, 0.2);
  }

  40% {
    transform: scale(1, 0.2);
  }

  50% {
    transform: scale(1, 1);
  }

  90% {
    transform: scale(1, 1);
  }

  100% {
    transform: scale(1, 0.2);
  }
}

@keyframes barUp1 {
  0% {
    transform: scale(1, 0.2);
  }

  40% {
    transform: scale(1, 0.2);
  }

  50% {
    transform: scale(1, 1);
  }

  90% {
    transform: scale(1, 1);
  }

  100% {
    transform: scale(1, 0.2);
  }
}

@-webkit-keyframes barUp2 {
  0% {
    transform: scale(1, 0.4);
  }

  40% {
    transform: scale(1, 0.4);
  }

  50% {
    transform: scale(1, 0.8);
  }

  90% {
    transform: scale(1, 0.8);
  }

  100% {
    transform: scale(1, 0.4);
  }
}

@keyframes barUp2 {
  0% {
    transform: scale(1, 0.4);
  }

  40% {
    transform: scale(1, 0.4);
  }

  50% {
    transform: scale(1, 0.8);
  }

  90% {
    transform: scale(1, 0.8);
  }

  100% {
    transform: scale(1, 0.4);
  }
}

@-webkit-keyframes barUp3 {
  0% {
    transform: scale(1, 0.6);
  }

  100% {
    transform: scale(1, 0.6);
  }
}

@keyframes barUp3 {
  0% {
    transform: scale(1, 0.6);
  }

  100% {
    transform: scale(1, 0.6);
  }
}

@-webkit-keyframes barUp4 {
  0% {
    transform: scale(1, 0.8);
  }

  40% {
    transform: scale(1, 0.8);
  }

  50% {
    transform: scale(1, 0.4);
  }

  90% {
    transform: scale(1, 0.4);
  }

  100% {
    transform: scale(1, 0.8);
  }
}

@keyframes barUp4 {
  0% {
    transform: scale(1, 0.8);
  }

  40% {
    transform: scale(1, 0.8);
  }

  50% {
    transform: scale(1, 0.4);
  }

  90% {
    transform: scale(1, 0.4);
  }

  100% {
    transform: scale(1, 0.8);
  }
}

@-webkit-keyframes barUp5 {
  0% {
    transform: scale(1, 1);
  }

  40% {
    transform: scale(1, 1);
  }

  50% {
    transform: scale(1, 0.2);
  }

  90% {
    transform: scale(1, 0.2);
  }

  100% {
    transform: scale(1, 1);
  }
}

@keyframes barUp5 {
  0% {
    transform: scale(1, 1);
  }

  40% {
    transform: scale(1, 1);
  }

  50% {
    transform: scale(1, 0.2);
  }

  90% {
    transform: scale(1, 0.2);
  }

  100% {
    transform: scale(1, 1);
  }
}
</style>