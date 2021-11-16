<template>
  <section class="services-advantage">
    <!-- 服务优势 -->
    <div class="container">
      <div class="row title-component">
        <div class="col-xs-12">
          <h3>中天华夏服务优势</h3>
          <h4>目前已成为众多世界500强企业的合作伙伴</h4>
        </div>
      </div>
      <ul class="row advantage-list">
        <li v-for="(advantage, index) in advantages" :key="index">
          <div class="icon-box">
            <img :src="advantage.icon" alt="" class="icon" />
          </div>
          <h4>{{ advantage.title }}</h4>
          <p>{{ advantage.content }}</p>
        </li>
      </ul>

      <ul class="row additional-box">
        <li>
          <p>20+</p>
          <div>涵盖行业</div>
        </li>
        <li>
          <p>30+</p>
          <div>世界500强合作伙伴</div>
        </li>
        <li>
          <p>500+</p>
          <div>咨询与培训项目成功案例</div>
        </li>
        <li>
          <p>500+</p>
          <div>服务企业</div>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      advantages: [
        {
          icon: require("~/static/images/advantage01.png"),
          title: `资质与方法`,
          content: `严谨、系统的咨询管理体系。国际注册管理咨询CMC。`,
        },
        {
          icon: require("~/static/images/advantage02.png"),
          title: `变革管理`,
          content: `充分调研及“松土”，系统的变革管理最大限度调动积极性，保障变革成功变革管理工具，辅助提升咨询效率。`,
        },
        {
          icon: require("~/static/images/advantage03.png"),
          title: `节奏把握`,
          content: `整体规划、分步实施。量体裁衣、步步为营、稳步推进。切实可行的计划、定期报告。`,
        },
        {
          icon: require("~/static/images/advantage04.png"),
          title: `质量保证`,
          content: `业界首创，为咨询项目设置独立质量保证（QA）管理角色保障项目规范、高质量推进。`,
        },
        {
          icon: require("~/static/images/advantage05.png"),
          title: `量化可视`,
          content: `业界领先的体系成熟度量化评估模型分摸块评审与阶段验收。审慎的试运行、推广与长期辅导。`,
        },
      ],
    };
  },
};
</script>
<style lang="scss">
//服务优势
.services-advantage {
  overflow: unset;
  height: 545px;
  background-color: #373737;
  background: url(~/static/images/advantage_bg.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  position: relative;

  .container {
    .title-component {
      h3 {
        color: #fff;
      }
    }

    .advantage-list {
      display: flex;
      list-style: none;

      li {
        flex: 1;
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        margin-right: 30px;

        &:last-child {
          margin-right: unset;
        }

        .icon-box {
          display: flex;
          justify-content: center;
          align-items: center;
          width: 72px;
          height: 72px;
          background-color: #595959;
          border-radius: 50%;
          margin-bottom: 45px;
        }

        h4 {
          margin: unset;
          margin-bottom: 25px;
          font-family: MicrosoftYaHei-Bold;
          font-size: 18px;
          font-weight: normal;
          font-stretch: normal;
          letter-spacing: 0px;
          color: #ffffff;
        }

        p {
          font-family: MicrosoftYaHei;
          font-size: 14px;
          font-weight: normal;
          font-stretch: normal;
          line-height: 24px;
          letter-spacing: 0px;
          color: #cccccc;
        }
      }
    }

    .additional-box {
      box-sizing: border-box;
      position: absolute;
      bottom: -63px;
      left: 50%;
      margin: unset;
      transform: translateX(-50%);
      display: flex;
      justify-content: center;
      align-items: center;
      width: 964px;
      height: 126px;
      padding: 32px 0;
      background-color: #a51c30;
      border-radius: 10px;
      list-style: none;

      li {
        flex: 1;
        text-align: center;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        p {
          margin-bottom: unset;
          font-family: MicrosoftYaHei-Bold;
          font-size: 40px;
          font-weight: normal;
          font-stretch: normal;
          line-height: 1;
          letter-spacing: 0px;
          color: #ffffff;
        }

        div {
          font-family: MicrosoftYaHei;
          font-size: 18px;
          font-weight: normal;
          letter-spacing: 0px;
          color: #ffffff;
        }
      }
    }
  }
}
</style>
