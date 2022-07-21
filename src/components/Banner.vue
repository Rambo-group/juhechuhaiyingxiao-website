<template>
  <div>
    <div class="container head">
      <div class="row top">
        <div class="col-12 col-lg-6">
          <div class="title">聚合你的广告资源</div>
          <div class="top_p">赋能出海品牌 助力全球营销</div>
        </div>
        <div class="col-12 col-lg-6">
          <swiper id="home" class="swiper" :options="swiperOption">
            <swiper-slide>
              <img src="~@assets/vzxv.png" alt="" />
            </swiper-slide>
            <swiper-slide>
              <img src="~@assets/vzxv.png" alt="" />
            </swiper-slide>
            <swiper-slide>
              <img src="~@assets/vzxv.png" alt="" />
            </swiper-slide>
            <swiper-slide>
              <img src="~@assets/vzxv.png" alt="" />
            </swiper-slide>
            <swiper-slide>
              <img src="~@assets/vzxv.png" alt="" />
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
        mousewheel:true,
        slidesPerView: 1.5,
        watchSlidesProgress: true,

        centeredSlides: true,
        loop: true,
        loopedSlides: 5,
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
              let scale = 1 - Math.abs(slideProgress) / 5;
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
};
</script>

<style lang="less" scoped>
.head {
  height: 820px;
  // display: flex;
  // align-items: center;
  background: url("~@assets/czxc.png") no-repeat;
  background-position: center;
  background-size: 100% 100%;
  .top {
    // line-height: 820px;
    .title {
      font-size: 64px;
      font-family: Microsoft YaHei-Bold, Microsoft YaHei;
      font-weight: bold;
      color: #131414;
    }
    .top_p {
      font-size: 40px;
      font-family: Microsoft YaHei-Regular, Microsoft YaHei;
      font-weight: 400;
      color: #131414;
      line-height: 47px;
      letter-spacing: 12px;
    }

  #home {
    img {
      width: 372px;
      height: 510px;
    }
  }
  }
}
#certify {
	position: relative;
	width: 1200px;
	margin: 0 auto
}

#certify .swiper-container {
	padding-bottom: 60px;
}

#certify  .swiper-slide {
	width: 520px;
	height: 408px;
	background: #fff;
	box-shadow: 0 8px 30px #ddd;
}
#certify  .swiper-slide img{
	display:block;
}
#certify  .swiper-slide p {
	line-height: 98px;
	padding-top: 0;
	text-align: center;
	color: #636363;
	font-size: 1.1em;
	margin: 0;
}

#certify .swiper-pagination {
	width: 100%;
	bottom: 20px;
}

#certify .swiper-pagination-bullets .swiper-pagination-bullet {
	margin: 0 5px;
	border: 3px solid #fff;
	background-color: #d5d5d5;
	width: 10px;
	height: 10px;
	opacity: 1;
}

#certify .swiper-pagination-bullets .swiper-pagination-bullet-active {
	border: 3px solid #00aadc;
	background-color: #fff;
}
</style>
