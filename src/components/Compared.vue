<template>
  <div class="body" id="Compared">
    <swiper class="swiper" :options="swiperOption" id="Compared1">
      <div class="swiper-slide">
        <div class="content">
          <div class="left">
            <div class="desc sdk1">
              <div class="title">自己找网红</div>
              <div class="ness">
                <div>存在问题</div>
                <div>
                  <div>① 高昂时间成本与团队人员成本</div>
                  <div>② 海外红人进度不可控，无约束</div>
                  <div>③ 海外红人资源缺失，找不到</div>
                  <div>④ 没有经验，没有案例，无从下手</div>
                  <div>⑤ 海外红人拿钱跑路，毫无办法</div>
                </div>
              </div>
              <div class="ness">
                <div>优点</div>
                <div>
                  <div>可与红人直接沟通，输出产品特点积累一定海外红人资源</div>
                </div>
              </div>
            </div>
            <div class="desc sdk2">
              <div class="title">找海外MCN</div>
              <div class="ness">
                <div>存在问题</div>
                <div>
                  <div>① 海外溢价空间大，博主价格翻倍</div>
                  <div>② 海外文化差异大，沟通困难</div>
                  <div>③ 海外红人资源缺失，找不到</div>
                  <div>④ 具有一定风险，无法确保合作安排</div>
                </div>
              </div>
              <div class="ness">
                <div>优点</div>
                <div>
                  <div>降低企业时间成本，直接对接红人具有一定海外红人资源</div>
                </div>
              </div>
            </div>
            <div class="desc sdk3">
              <div class="title">聚合出海</div>
              <div class="ness">
                <div>合作优势</div>
                <div>
                  <div>① 自主研发数据平台，海外红人标签化</div>
                  <div>② 103个国家，25个语种，150万+红人资源</div>
                  <div>③ 2000+成功案例沉淀，助推品牌出海</div>
                  <div>④ 专业服务团队，分国家，分语种精细化服务</div>
                  <div>⑤ 建立海外红人黑名单，规避不必要风险</div>
                  <div>⑥ 国内公司，效率高，易沟通</div>
                  <div>⑦ 全包托管式服务，大大降低企业成本</div>
                  <div>⑧ 提供最终结案报告，分析品牌出海走向</div>
                </div>
              </div>
            </div>
          </div>
          <div class="rigth">
            <div>海外网红</div>
            <div>营销服务对比</div>
          </div>
        </div>
      </div>
      <div class="swiper-slide">
        <div class="content">
          <div class="left1">
            <div class="disc item1">
              <div><img src="~@assets/zxc.png" alt="" /></div>
              <div>
                <div class="title">特推</div>
                <div class="tit">爆发力强，影响力大</div>
                <div class="txt">覆盖大众打造热度</div>
                <div class="txt">
                  <span>集中曝光</span><span>品牌调性</span>
                </div>
              </div>
            </div>
            <div class="disc item2">
              <div><img src="~@assets/fwe.png" alt="" /></div>
              <div>
                <div class="title">精准</div>
                <div class="tit">种草能力强，专业性高</div>
                <div class="txt">垂直领域深度影响</div>
                <div class="txt">
                  <span>专业讲解</span><span>信誉背书</span>
                </div>
              </div>
            </div>
            <div class="disc item3">
              <div><img src="~@assets/nfgnf.png" alt="" /></div>
              <div>
                <div class="title">泛推</div>
                <div class="tit">营造真实，扩大口碑</div>
                <div class="txt">关键字SEO优化覆盖</div>
                <div class="txt">
                  <span>真实晒单</span><span>购买互动</span>
                </div>
              </div>
            </div>
          </div>
          <div class="rigth">
            <div>专业输出投放策略</div>
            <div>高效、灵活、省心</div>
          </div>
        </div>
      </div>
    </swiper>
  </div>
</template>

<script>
export default {
  data() {
    return {
      swiperOption: {
        direction: "vertical",
        followFinger: false,
        speed: 800,
        mousewheel: true,
        loop: true,
        pagination: {
          el: ".swiper-pagination",
        },
        on: {
          init: function () {
            let slide = this.slides.eq(0);
            slide.addClass("ani-slide");
          },
          transitionStart: function () {
            for (let i = 0; i < this.slides.length; i++) {
              let slide = this.slides.eq(i);
              slide.removeClass("ani-slide");
            }
          },
          transitionEnd: function () {
            let slide = this.slides.eq(this.activeIndex);
            slide.addClass("ani-slide");
          },
        },
      },
    };
  },
    mounted() {
    $(document).scroll(() => {
      for (let index = 1; index < 2; index++) {
        Restore(`#Compared${index}`);
      }
    });
  },
};
</script>

<style lang="less" scoped>
.body {
  margin: 124px 0 224px;
  float: left;
  .content {
    height: 580px;
    width: 1632px;
    display: flex;
    .left {
      position: relative;
      height: 100%;
      width: 72%;
      background: linear-gradient(90deg, #ffffff 0%, #d9ffe7 100%);
      border-radius: 0px 48px 48px 0px;
      padding: 45px 0 0 132px;
      text-align: left;
      .desc {
        box-shadow: 2px 6px 19px 1px rgba(3, 1, 18, 0.1);
        border-radius: 16px;
        .title {
          font-size: 16px;
          font-family: Microsoft YaHei-Bold, Microsoft YaHei;
          font-weight: bold;
          color: #131414;
          margin-bottom: 8px;
        }
        .ness {
          > div {
            margin-top: 4px;
          }
          > div:nth-child(1) {
            font-size: 12px;
            font-family: Microsoft YaHei-Bold, Microsoft YaHei;
            font-weight: bold;
            color: #131414;
          }
          > div:nth-child(2) div {
            font-size: 12px;
            font-family: Microsoft YaHei-Regular, Microsoft YaHei;
            font-weight: 400;
            color: #131414;
            margin: 4px 0;
          }
        }
      }
      .sdk1 {
        position: absolute;
        top: 56px;
        right: 456px;
        padding: 32px 24px;
        width: 240px;
        z-index: 999;
        background: linear-gradient(90deg, #ffffff 0%, #e9f4ff 100%);
      }
      .sdk2 {
        position: absolute;
        top: 288px;
        right: 419px;
        margin-top: 27px;
        padding: 24px 24px;
        width: 540px;
        background: linear-gradient(90deg, #fffeff 0%, #d7fffe 100%);
      }
      .sdk3 {
        position: absolute;
        top: 48px;
        right: 136px;
        width: 296px;
        padding: 40px 32px;
        background: linear-gradient(90deg, #a1c4fd 0%, #c2e9fb 100%);
      }
    }
    .left1 {
      position: relative;
      height: 100%;
      width: 72%;
      background: linear-gradient(90deg, #ffffff 0%, #d9ffe7 100%);
      border-radius: 0px 48px 48px 0px;
      text-align: left;
      .disc {
        display: flex;
        box-shadow: 2px 6px 19px 1px rgba(3, 1, 18, 0.1);
        border-radius: 12px;
        padding: 16px;
        img {
          width: 114px;
          height: 114px;
        }
        .title {
          font-size: 20px;
          font-family: Microsoft YaHei-Bold, Microsoft YaHei;
          font-weight: bold;
          color: #131414;
        }
        .tit {
          font-size: 16px;
          font-family: Microsoft YaHei-Bold, Microsoft YaHei;
          font-weight: bold;
          color: #131414;
          margin: 4px 0 8px;
        }
        .txt {
          font-size: 14px;
          font-family: Microsoft YaHei-Regular, Microsoft YaHei;
          font-weight: 400;
          color: #606266;
        }
      }
      .item1 {
        position: absolute;
        top: 52px;
        right: 476px;
        width: 340px;
        background: linear-gradient(90deg, #fddb92 0%, #d1fdff 100%);
      }
      .item2 {
        position: absolute;
        top: 216px;
        right: 228px;
        width: 356px;
        background: linear-gradient(90deg, #96fbc4 0%, #f9f586 100%);
      }
      .item3 {
        position: absolute;
        top: 380px;
        left: 378px;
        width: 340px;
        background: linear-gradient(90deg, #accbee 0%, #e7f0fd 100%);
      }
    }
    .rigth {
      width: 432px;
      margin-left: 24px;
      padding-top: 88px;
      text-align: left;
      > div {
        font-size: 32px;
        font-family: Microsoft YaHei-Bold, Microsoft YaHei;
        font-weight: bold;
        color: #131414;
      }
    }
  }
}
.swiper-wrapper {
  transition-delay: 0.3s;
}
.swiper-container {
  height: 580px;
  margin: 20px auto;
}
.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}

.swiper-slide {
  .left {
    transform: translateX(-200px);
    opacity: 0;
    transition: all 0.6s;
    .sdk1 {
      transform: translateX(-200px);
      opacity: 0;
      transition: all 1s;
    }
    .sdk2 {
      transform: translateX(-200px);
      opacity: 0;
      transition: all 1s;
    }
    .sdk3 {
      transform: translateX(-200px);
      opacity: 0;
      transition: all 0.8s;
    }
  }
  .left1 {
    transform: translateX(-200px);
    opacity: 0;
    transition: all 0.6s;
    .item1 {
      transform: translateX(-200px);
      opacity: 0;
      transition: all 0.8s;
    }
    .item2 {
      transform: translateX(-200px);
      opacity: 0;
      transition: all 1s;
    }
    .item3 {
      transform: translateX(-200px);
      opacity: 0;
      transition: all 1.1s;
    }
  }
  .rigth {
    transform: translateX(200px);
    opacity: 0;
    transition: all 0.6s;
  }
}
.ani-slide {
  .left,
  .rigth {
    transform: translateX(0);
    opacity: 1;
    .sdk1,
    .sdk2,
    .sdk3 {
      transform: translateX(0);
      opacity: 1;
    }
  }
  .left1 {
    transform: translateX(0);
    opacity: 1;
    .item1,
    .item2,
    .item3 {
      transform: translateX(0);
      opacity: 1;
    }
  }
}
</style>
