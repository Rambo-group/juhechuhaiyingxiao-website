<template>
  <div class="business" id="Advertising">
    <div class="container">
      <div class="title" id="Advertising1">广告投放</div>
      <div class="row item" id="Advertising2">
        <div class="col-5"><img src="~@assets/xcvxc.png" alt="" /></div>
        <div class="col-7">
          <div class="tit">Facebook</div>
          <div class="txt">
            全球庞大的社交媒体平台，月活跃用户达20亿人，为广告投放提供海量的目标受众及较精确的人群触达。
          </div>
        </div>
      </div>
      <div class="row item" id="Advertising3">
        <div class="col-7">
          <div class="tit" style="text-align: right;">lnstagram</div>
          <div class="txt" style="text-align: right;">
            全球日活跃账户数量超过5亿+
          </div>
          <div class="txt" style="text-align: right;">
           90%+的lnstagram账户关注了商家
          </div>
          <div class="txt" style="text-align: right;">
            每天有超过5亿用户使用Instagram快拍
          </div>
        </div>
        <div class="col-5"><img src="~@assets/kuk.png" alt="" /></div>
      </div>
      <div class="row item" id="Advertising4">
        <div class="col-5"><img src="~@assets/vxc.png" alt="" /></div>
        <div class="col-7">
          <div class="tit">TikTok</div>
          <div class="txt">
            TikTok是字节跳动旗下面向全球广告主的营销服务品牌，汇聚海量流量、数据、优质内容，为全球广告合作伙伴提供综合数字营销解决方案，帮助品牌实现和用户的高效沟通。
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script >
export default {
  data() {
    return {};
  },
   mounted() {
    $(document).scroll(() => {
      for (let index = 1; index < 5; index++) {
        Restore(`#Advertising${index}`);
      }
    });
  },
};
</script>
<style lang="less" scoped>
.business {
  margin: 124px 0;
  padding: 124px 0 124px;
  background-color: #2e2e3a;
  .title {
    font-size: 64px;
    margin-top: 100px;
    font-family: Microsoft YaHei-Bold, Microsoft YaHei;
    font-weight: bold;
    color: #72e5ce;
    text-align: center;
  }
  .item {
    text-align: center;
    margin-top: 124px;
    img {
      width: 276px;
      height: 590px;
    }
    .tit {
      font-size: 48px;
      font-family: Microsoft YaHei-Bold, Microsoft YaHei;
      font-weight: bold;
      color: #72e5ce;
      line-height: 56px;
      text-align: left;
      margin: 40px 0 32px;
    }
    .txt {
      font-size: 24px;
      font-family: Microsoft YaHei-Bold, Microsoft YaHei;
      font-weight: bold;
      color: #ffffff;
      line-height: 28px;
      text-align: left;
    }
  }
}
</style>
