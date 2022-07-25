<template>
  <div class="home" id="Banner">
    <div class="head">
      <div class="row">
        <div class="col-12 col-lg-6 left" id="Banner1">
          <div class="title">聚合你的广告资源</div>
          <div class="top_p">赋能出海品牌 助力全球营销</div>
        </div>
        <div class="col-12 col-lg-6">
          <swiper id="home" class="swiper" :options="swiperOption">
            <swiper-slide>
              <img src="~@assets/vzxv.png" alt="" />
            </swiper-slide>
            <swiper-slide>
              <img src="~@assets/erwrfd.png" alt="" />
            </swiper-slide>
            <swiper-slide>
              <img src="~@assets/ewr.png" alt="" />
            </swiper-slide>
          </swiper>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      swiperOption: {
        slidesPerView: 1.6,
        watchSlidesProgress: true,
        centeredSlides: true,
        loop: true,
        speed: 500,
        loopedSlides: 3,
        autoplay: true,
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },
        pagination: {
          el: ".swiper-pagination",
          //clickable :true,
        },
        on: {
          progress: function () {
            for (let i = 0; i < this.slides.length; i++) {
              var slide = this.slides.eq(i);
              var slideProgress = this.slides[i].progress;
              let modify = 1;
              if (Math.abs(slideProgress) > 1) {
                modify = (Math.abs(slideProgress) - 1) * 0.3 + 1;
              }
              let translate = slideProgress * modify * 260 + "px";
              let scale = 1 - Math.abs(slideProgress) / 3;
              let zIndex = 999 - Math.abs(Math.round(10 * slideProgress));
              slide.transform(
                "translateX(" + translate + ") scale(" + scale + ")"
              );
              slide.css("zIndex", zIndex);
              slide.css("opacity", 1);
              if (Math.abs(slideProgress) > 3) {
                slide.css("opacity", 0);
              }
            }
          },
          setTransition: function (transition) {
            for (var i = 0; i < this.slides.length; i++) {
              var slide = this.slides.eq(i);
              slide.transition(transition);
            }
          },
        },
      },
    };
  },
    mounted() {
      for (let index = 1; index < 2; index++) {
        Restore(`#Banner${index}`);
      }
  },
};
</script>

<style lang="less" scoped>
.home {
  display: flex;
  justify-content: center;
}
.head {
  height: 820px;
  max-width: 1600px;
  min-width: 1440px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background: url("~@assets/czxc.png") no-repeat;
  background-position: center;
  background-size: 100% 100%;
  padding: 0 88px 0 64px;
  // .top {
    .left {
      display: flex;
      flex-direction: column;
      justify-content: center;
      .title {
        font-size: 64px;
        font-family: Microsoft YaHei-Bold, Microsoft YaHei;
        font-weight: bold;
        color: #131414;
        transition: all 0.4s;
      }
      .top_p {
        font-size: 40px;
        font-family: Microsoft YaHei-Regular, Microsoft YaHei;
        font-weight: 400;
        color: #131414;
        line-height: 47px;
        letter-spacing: 12px;
        transition: all 0.4s;
      }
    }

    #home {
      img {
        width: 372px;
        height: 510px;
        transition: all 1.8s;
      }
    }
  // }
}
</style>
