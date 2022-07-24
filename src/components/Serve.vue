<template>
  <div class="body" id="serve">
    <div class="container">
      <div class="top_title" id="serve1">服务流程</div>
      <div class="row">
        <div class="business">
          <div class="item" id="serve2">
            <img src="~@assets/bty.png" alt="" />
            <div class="title">项目调研</div>
            <div class="txt">
              我们同品牌主一起深入沟通，从而了解客户需求，明确项目目标和标准已确保推进一个顺畅的项目进程，输出项目需求调研表。
            </div>
          </div>
          <div class="item" id="serve3">
            <img src="~@assets/cwr.png" alt="" />
            <div class="title">策划方案</div>
            <div class="txt">
              将对调研信息进行梳理，结合整体营销定位和规划分析品牌特点和红人类型，策划爆点创意和提炼，输出红人定位方案和创意策划方案。
            </div>
          </div>
          <div class="item" id="serve4">
            <img src="~@assets/rgew.png" alt="" />
            <div class="title">匹配红人</div>
            <div class="txt">
              根据红人定位方案开始四配红人，并初步沟通创意方案和档期安排，输出红人列表以及确认最终合作红人及活动内容方案。
            </div>
          </div>
          <div class="item" id="serve5">
            <img src="~@assets/vwr.png" alt="" />
            <div class="title">执行投放</div>
            <div class="txt">
              根据确认的红人和方案我们会统筹管理创作进度和审核节点，确保推广内容无误后按时按量投放。
            </div>
          </div>
          <div class="item" id="serve6">
            <img src="~@assets/zrwq.png" alt="" />
            <div class="title">效果分析</div>
            <div class="txt">
              投放过程中实时监控项目核心指标和多维度分析，最终形成一份全面详细的效果评估报告。
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    $(document).scroll(() => {
      for (let index = 1; index < 7; index++) {
        Restore(`#serve${index}`);
      }
    });
  },
};
</script>

<style lang="less" scoped>
.body {
  padding: 0 0 100px 0;
  .top_title {
    font-size: 64px;
    font-family: Microsoft YaHei-Bold, Microsoft YaHei;
    font-weight: bold;
    color: #131414;
    text-align: center;
    margin: 124px 0;
  }
  .business {
    display: flex;
    > div {
      flex: 1;
    }
    > div:nth-child(2n + 1) {
      margin: 0 24px;
    }
    .item {
      background: linear-gradient(90deg, #f3e7e9 0%, #e3eeff 99%, #e3eeff 100%);
      box-shadow: 2px 6px 19px 1px rgba(3, 1, 18, 0.1);
      border-radius: 16px;
      padding: 64px 24px;
      text-align: center;
      > img {
        width: 64px;
        height: 64px;
      }
      .title {
        font-size: 24px;
        font-family: Microsoft YaHei-Regular, Microsoft YaHei;
        font-weight: 400;
        color: #131414;
        margin: 24px 0 8px;
      }
      .txt {
        font-size: 16px;
        font-family: Microsoft YaHei-Regular, Microsoft YaHei;
        font-weight: 400;
        color: #606266;
        text-align: left;
      }
    }
  }
}
</style>
