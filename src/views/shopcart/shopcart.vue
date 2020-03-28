<template>
  <div  class="div1">
    <div class="block">
      <el-carousel height="150px" :interval="4000">
        <el-carousel-item
          v-for="item in imagesbox"
          :key="item.id"
          align="center"
        >
          <img :src="item.idview" height="100%" width="100%"/>
        </el-carousel-item>
      </el-carousel>
    </div>

    <el-row :gutter="15" type="flex">
      <el-col>
        <img
          class="img2"
          src="../../assets/img/iconfont/hospitalserver/今日挂号.png"
        />
        <div>今日挂号</div>
      </el-col>
      <el-col>
        <img
          class="img2"
          src="../../assets/img/iconfont/hospitalserver/预约挂号.png"
        />
        <div>预约挂号</div>
      </el-col>
      <el-col>
        <img
          class="img2"
          src="../../assets/img/iconfont/hospitalserver/门诊缴费.png"
        />
        <div>门诊缴费</div>
      </el-col>
    </el-row>
    <el-container>
      <el-card class="box-card">
        <div slot="header" class="clearfix">
          <span class="span1">门诊服务</span>
        </div>
        <el-row :gutter="15" type="flex">
          <el-col>
            <img
              class="img3"
              src="../../assets/img/iconfont/hospitalserver/排队候诊.png"
            />
            <div>排队候诊</div>
          </el-col>
          <el-col>
            <img
              class="img3"
              src="../../assets/img/iconfont/hospitalserver/门诊专家.png"
            />
            <div>门诊专家</div>
          </el-col>
          <el-col>
            <img
              class="img3"
              src="../../assets/img/iconfont/hospitalserver/医生排班.png"
            />
            <div>医生排班</div>
          </el-col>
          <el-col>
            <img
              class="img3"
              src="../../assets/img/iconfont/hospitalserver/查报告单.png"
            />
            <div>查报告单</div>
          </el-col>
        </el-row>
      </el-card>
    </el-container>
    <el-container>
      <el-card class="box-card">
        <div slot="header" class="clearfix">
          <span class="span1">住院服务</span>
        </div>
        <el-row :gutter="15" type="flex" align="middle" justify="center">
          <el-col :span="12">
            <el-card class="box-card" :body-style="{ padding: '10px' }">
              <el-row :gutter="50" type="flex" align="middle" justify="center">
                <el-col :span="6">
                  <img
                    class="img4"
                    src="../../assets/img/iconfont/hospitalserver/充值.png"
                /></el-col>
                <el-col :span="18" pull="3">
                  <el-row align="middle" justify="start">
                    <span style="font-weight:bold font-size:10px"
                      >预交金充值</span
                    >
                  </el-row>
                  <el-row style="font-size:5px " align="middle" justify="start">
                    <span style="color:#C0C0C0">缴纳住院押金</span>
                  </el-row>
                </el-col>
              </el-row>
            </el-card>
          </el-col>
          <el-col :span="12">
            <el-card class="box-card" :body-style="{ padding: '10px' }">
              <el-row :gutter="50" type="flex" align="middle" justify="center">
                <el-col :span="6">
                  <img
                    class="img4"
                    src="../../assets/img/iconfont/hospitalserver/日清单.png"
                /></el-col>
                <el-col :span="18" pull="3">
                  <el-row align="middle" justify="start">
                    <span style="font-weight:bold font-size:10px"
                      >住院日清单</span
                    >
                  </el-row>
                  <el-row style="font-size:5px" align="middle" justify="start">
                    <span style="color:#C0C0C0">查看每日住院</span>
                  </el-row>
                </el-col>
              </el-row>
            </el-card>
          </el-col>
        </el-row>
      </el-card>
    </el-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      imagesbox: [
        { id: 0, idview: require("../../assets/img/Carousel/1.png") },
        { id: 1, idview: require("../../assets/img/Carousel/2.png") },
        { id: 2, idview: require("../../assets/img/Carousel/3.png") }
      ]
    };
  }
};
</script>
<style>
.img4 {
  width: 24px;
  height: 24px;
}
.box-card {
  margin-top: 3%;
  flex: auto;
}
.clearfix {
  font-size: 12px;
  vertical-align: middle;
  display: table-cell;
  font-weight: bold;
  margin-bottom: 2%;
}
.el-card__header {
  height: 3%;
}
.div2 {
  margin-top: 3;
}
.el-carousel {
  margin-top: 3%;
}
.el-carousel-item {
  border-radius: 30px
}
.img2 {
  margin-top: 10%;
  height: 70%;
  width: 80%;
}
.img3 {
  margin-top: 10%;
  height: 60%;
  width: 70%;
}
.el-col {
  text-align: center;
}
</style>
