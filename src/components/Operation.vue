<template>
  <div class="business">
    <div class="container">
      <div class="account">
        <div class="title">账号运营</div>
        <div class="row describe">
          <div class="col-5 left">
            <div class="tit">打造账号</div>
            <div class="tet">建立品牌流量洼地</div>
            <div class="txt">
              <div>品牌账号为基础</div>
              <div>结合达人合作信息流广告、网红带货</div>
            </div>
          </div>
          <div class="col-4 navimg">
            <img src="~@assets/xcvxc.png" alt="" />
          </div>
          <div class="col-3 right">
            <div>高频互动</div>
            <div>时尚展现</div>
            <div>精准触达</div>
            <div>品牌心智</div>
          </div>
        </div>
      </div>
      <div class="streaming">
        <div class="title">跨境直播</div>
        <div class="row describe">
          <div class="col-7 left">
            <div class="tit">娱乐式、交互式</div>
            <div class="tet">一站式的购物体验</div>
            <div class="txt">
              <div>直播可以快速建立信任关系，实时与用户互动</div>
              <div>更好展示商品，从而促进销售</div>
            </div>
          </div>
          <div class="col-5 navimg2">
            <img src="~@assets/xcvxc.png" alt="" />
          </div>
        </div>
      </div>
      <div class="deal">
        <div class="row describe">
          <div class="col-5 navimg2">
            <img src="~@assets/xcvxc.png" alt="" />
          </div>
          <div class="col-7 left">
            <div class="tet">
              2021年印尼、英国相继开通了小黄车购物功能。黑五期间，TikTok
              单场直播间突破<span>＄50万</span> 成交。
            </div>
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
};
</script>
<style lang="less" scoped>
.business {
  padding: 100px 0;
  .title {
    font-size: 64px;
    font-family: Microsoft YaHei-Bold, Microsoft YaHei;
    font-weight: bold;
    color: #30d89d;
    text-align: center;
  }
  .describe {
    margin: 220px 0;

    .left {
      padding: 96px 0 0;
      .tit {
        font-size: 48px;
        font-family: Microsoft YaHei-Bold, Microsoft YaHei;
        font-weight: bold;
        color: #30d89d;
      }
      .tet {
        font-size: 48px;
        font-family: Microsoft YaHei-Bold, Microsoft YaHei;
        font-weight: bold;
        color: #131414;
        margin: 8px 0 24px;
        > span {
          color: #30d89d;
          font-size: 64px;
        }
      }
      .txt {
        font-size: 24px;
        font-family: Microsoft YaHei-Bold, Microsoft YaHei;
        font-weight: bold;
        color: #131414;
      }
    }
    .navimg {
      text-align: center;
      > img {
        width: 304px;
        height: 650px;
      }
    }
    .navimg2{
      text-align: center;
      >img{
        width: 264px;
        height: 564px;
      }
    }
    .right {
      display: flex;
      flex-direction: column;
      justify-content: center;
      > div {
        font-size: 24px;
        font-family: Microsoft YaHei-Bold, Microsoft YaHei;
        font-weight: bold;
        color: #30d89d;
        line-height: 28px;
        margin: 12px 0;
      }
    }
  }
  .streaming {
    .toggle {
      .left1 {
        .txt1 {
        }
      }
      .right2 {
        width: 264px;
        height: 564px;
      }
    }
  }
}
</style>
