<template>
  <div class="intor" id="Introduce">
    <div class="title" id="Introduce1">我们能做什么？</div>
    <div class="container">
      <div class="row content" id="Introduce2">
        <div class="col-4">
          <img src="~@assets/yery.png" alt="" />
        </div>
        <div class="col-4">
          <img src="~@assets/fasf.png" alt="" />
        </div>
        <div class="col-4">
          <img src="~@assets/vzx.png" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    $(document).scroll(() => {
      for (let index = 1; index < 3; index++) {
        Restore(`#Introduce${index}`);
      }
    });
  },
};
</script>

<style lang="less" scoped>
.intor {
  margin: 100px 0;
  .title {
    font-size: 64px;
    font-family: Microsoft YaHei-Bold, Microsoft YaHei;
    font-weight: bold;
    color: #131414;
    line-height: 75px;
    text-align: center;
    margin: 124px 0;
  }
  .content {
  min-width: 1400px;
    img {
      width: 432px;
      height: 566px;
    }
  }
}
</style>
