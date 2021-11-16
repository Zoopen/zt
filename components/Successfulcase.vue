<template>
  <section class="successful-case">
    <!-- 成功案例 -->
    <div class="container-fluid">
      <div class="row title-component">
        <div class="col-xs-12">
          <h3>成功案例</h3>
          <h4>成为赋能企业变革的管理咨询卓越品牌</h4>
        </div>
      </div>
      <div class="row case-list-box">
        <div class="case-list">
          <div class="case-item" v-for="(item, index) in cases" :key="index">
            <div class="case-img-box">
              <img :src="item.img" alt="" class="case-img" />
              <div class="case-mask">
                <img :src="item.logo" alt="" class="case-logo" />
              </div>
            </div>
            <div class="case-name">{{ item.title }}</div>
          </div>
        </div>
      </div>
      <a class="more-case-btn" href="#"
        >更多成功案例
        <img
          src="~/static/images/right_gray.png"
          alt=""
          class="more-case-btn-icon"
        />
      </a>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      cases: [
        {
          img: require("~/static/images/1.jpg"),
          logo: require("~/static/images/logo.png"),
          title: `李锦记研发管理体系咨询项目`,
        },
        {
          img: require("~/static/images/1.jpg"),
          logo: require("~/static/images/logo.png"),
          title: `李锦记研发管理体系咨询项目`,
        },
        {
          img: require("~/static/images/1.jpg"),
          logo: require("~/static/images/logo.png"),
          title: `李锦记研发管理体系咨询项目`,
        },
        {
          img: require("~/static/images/1.jpg"),
          logo: require("~/static/images/logo.png"),
          title: `李锦记研发管理体系咨询项目`,
        },
        {
          img: require("~/static/images/1.jpg"),
          logo: require("~/static/images/logo.png"),
          title: `李锦记研发管理体系咨询项目`,
        },
        {
          img: require("~/static/images/1.jpg"),
          logo: require("~/static/images/logo.png"),
          title: `李锦记研发管理体系咨询项目`,
        },
        {
          img: require("~/static/images/1.jpg"),
          logo: require("~/static/images/logo.png"),
          title: `李锦记研发管理体系咨询项目`,
        },
        {
          img: require("~/static/images/1.jpg"),
          logo: require("~/static/images/logo.png"),
          title: `李锦记研发管理体系咨询项目`,
        },
        {
          img: require("~/static/images/1.jpg"),
          logo: require("~/static/images/logo.png"),
          title: `李锦记研发管理体系咨询项目`,
        },
        {
          img: require("~/static/images/1.jpg"),
          logo: require("~/static/images/logo.png"),
          title: `李锦记研发管理体系咨询项目`,
        },
      ],
    };
  },
};
</script>
<style lang="scss">
//成功案例
.successful-case {
  background-color: #ffffff;

  .title-component {
    h3 {
      margin-top: 123px;
    }
  }

  .case-list-box {
    margin-bottom: 50px;
  }

  .case-list {
    display: grid;
    grid-template-columns: repeat(5, minmax(0, 1fr));
    row-gap: 30px;

    &:last-child {
      margin-bottom: unset;
    }

    .case-item {
      flex: 1;
      width: 100%;
      height: 100%;
      text-align: center;

      &:hover {
        .case-name {
          color: #881c30;
        }

        .case-img-box {
          .case-mask {
            top: 0;
          }
        }
      }

      .case-img-box {
        margin-bottom: 15px;
        overflow: hidden;
        position: relative;

        img.case-img {
          display: block;
          width: 100%;
          height: 100%;
        }

        .case-mask {
          position: absolute;
          top: -100%;
          left: 0;
          width: 100%;
          height: 100%;
          // background-color: #a51c30;
          background-color: rgba(165, 28, 48, 0.7);
          // opacity: 0.15;
          display: flex;
          justify-content: center;
          align-items: center;
          transition: all 0.3s;

          .case-logo {
            width: 100px;
            object-fit: contain;
          }
        }
      }

      .case-name {
        font-family: MicrosoftYaHei;
        font-size: 14px;
        font-weight: normal;
        font-stretch: normal;
        letter-spacing: 0px;
        color: #333333;
      }
    }
  }

  a.more-case-btn {
    margin: 0 auto;
    margin-bottom: 60px;
    box-sizing: border-box;
    display: flex;
    // justify-content: center;
    align-items: center;
    width: 193px;
    height: 47px;
    padding: 0 26px;
    background-color: #f0f0f0;
    border-radius: 24px;

    font-family: MicrosoftYaHei;
    font-size: 14px;
    font-weight: normal;
    font-stretch: normal;
    letter-spacing: 0px;
    color: #333333;

    .more-case-btn-icon {
      margin-left: 19px;
    }
  }
}
</style>
