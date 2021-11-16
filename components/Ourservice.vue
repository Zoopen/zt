<template>
  <section class="services">
    <!-- 我们的服务 -->
    <div class="container">
      <div class="row title-component">
        <div class="col-xs-12">
          <h3>我们的服务</h3>
          <h4>
            始终专注于产品创新与研发管理咨询领域，专业是我们的关键核心竞争力
          </h4>
        </div>
      </div>
      <div class="row services-grid">
        <div
          :class="'grid grid-' + (index + 1)"
          v-for="(service, index) in services"
          :key="index"
        >
          <img :src="service.icon" alt="" class="icon" />
          <h5>{{ service.title }}</h5>
          <p>{{ service.content }}</p>
          <img :src="service.img" alt="" class="main-img" />
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      services: [
        {
          icon: require("~/static/images/service01.png"),
          title: `产品战略规划咨询`,
          content: `中天华夏咨询基于著名的业务领先模型(BLM)(华为、IBM等世界500强企业广泛采用并获得成功），借助世界500强背景的资深顾问团队，深入指导产品战略制定的全过程，提升产品的市场竞争力，输出完善而富有竞争力的产品战略规划方案。`,
          img: require("~/static/images/service_01.jpg"),
        },
        {
          icon: require("~/static/images/service02.png"),
          title: `产品研发管理体系建设（IPD）`,
          content: `通过IPD体系构建，建立从市场机会到商业成功的系统管理能力。借助以投资为导向的决策机制、跨部门团队运作、产品与技术开发相分离的异步开发模式，以及面向市场的结构化开发流程等要素，提升产品创新效率，实现市场成功`,
          img: require("~/static/images/service_02.jpg"),
        },
        {
          icon: require("~/static/images/service03.png"),
          title: `产品研发关键人才培养`,
          content: `中天华夏咨询基于著名的业务领先模型(BLM)(华为、IBM等世界500强企业广泛采用并获得成功），借助世界500强背景的资深顾问团队，深入指导产品战略制定的全过程，提升产品的市场竞争力，输出完善而富有竞争力的产品战略规划方案。`,
          img: require("~/static/images/service_03.jpg"),
        },
      ],
    };
  },
};
</script>
<style lang="scss">
// 服务
.services {
  background-color: #f8f8f8;

  .container {
    .services-grid {
      // display: flex;
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      column-gap: 40px;
      align-items: flex-end;
      .grid {
        box-sizing: border-box;
        padding: 10px 20px 20px;
        // margin-right: 40px;
        background-color: #ffffff;
        box-shadow: 0px 10px 18px 0px rgba(0, 0, 0, 0.08);
        border-radius: 10px 10px 0px 0px;

        // &:last-child {
        //   margin-right: unset;
        // }

        &.grid-1 {
          min-height: 456px;
          border-top: 10px solid #d3a857;
        }

        &.grid-3 {
          min-height: 456px;
          border-top: 10px solid #373737;

          h5 {
            color: #373737;
          }
        }

        &.grid-2 {
          min-height: 523px;
          border-top: 10px solid #881c30;

          h5 {
            color: #881c30;
          }
        }
      }

      span {
        display: block;
        margin: 0 auto;
        margin-top: 40px;
        width: 60px;
        height: 60px;
        border: 1px solid red;
      }

      h5 {
        margin: 30px 0;
        text-align: center;
        font-family: MicrosoftYaHei-Bold;
        font-size: 20px;
        font-weight: normal;
        font-stretch: normal;
        line-height: 36px;
        letter-spacing: 0px;
        color: #d3a857;
      }

      p {
        font-family: MicrosoftYaHei;
        font-size: 13px;
        font-weight: normal;
        font-stretch: normal;
        line-height: 22px;
        letter-spacing: 0px;
        color: #666666;
      }

      img.icon {
        display: block;
        width: 65px;
        object-fit: contain;
        margin: 0 auto;
        margin-top: 40px;
      }

      img.main-img {
        width: 100%;
        object-fit: contain;
        margin-top: 30px;
        background-color: #f5daa7;
      }
    }
  }
}
</style>
