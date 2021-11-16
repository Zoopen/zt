<template>
  <section class="public-class">
    <!-- 近期公开课 -->
    <div class="container">
      <div class="row title-component">
        <div class="col-xs-12">
          <h3>近期公开课</h3>
          <h4>让每一个业务单元都成为有效增长的发动机</h4>
        </div>
      </div>
      <div class="row class-info">
        <swiper
          ref="mySwiper"
          :options="swiperOptions"
          class="index-class-swiper"
        >
          <swiper-slide v-for="(slide, i) in formatData" :key="i">
            <ul class="class-list">
              <li v-for="(course, index) in slide" :key="index">
                <img :src="course.cover" alt="" class="class-cover" />
                <div class="info-box">
                  <div class="class-name">
                    {{ course.name }}
                  </div>
                  <div class="other-info">
                    <div class="start-time">
                      <img :src="aclock" alt="" class="icon" />
                      开课时间：<span>{{ course.start_time }}</span>
                    </div>
                    <div class="address">
                      <img :src="pos" alt="" class="icon" />
                      地点：{{ course.pos }}
                    </div>
                  </div>
                </div>
                <div class="time-tag">
                  <div class="month">
                    <span>{{ course.month }}</span> 月
                  </div>
                </div>
              </li>
            </ul>
          </swiper-slide>
        </swiper>
        <!-- 如果需要导航按钮 -->
        <div class="class-info-switch-btn">
          <div class="index-class-prev" slot="button-prev" @click="prev">
            <img
              src="~/static/images/left_gray.png"
              alt=""
              class="normal-btn"
            />
            <img
              src="~/static/images/left_white.png"
              alt=""
              class="active-btn"
            />
          </div>
          <div class="index-class-next" slot="button-next" @click="next">
            <img
              src="~/static/images/right_gray.png"
              alt=""
              class="normal-btn"
            />
            <img
              src="~/static/images/right_white.png"
              alt=""
              class="active-btn"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      aclock: require("~/static/images/aclock.png"),
      pos: require("~/static/images/pos_dark.png"),
      classes: [
        {
          name: "技术创新管理（平台、技术与重用）", //线下公开课名称
          cover: require("~/static/images/1.jpg"), //线下公开课封面
          start_time: "2021年3月26日-27日", //线下公开课时间
          pos: "深圳", //线下公开课地点
          month: 3, //线下公开课月份
        },
        {
          name: "技术创新管理（平台、技术与重用）", //线下公开课名称
          cover: require("~/static/images/1.jpg"), //线下公开课封面
          start_time: "2021年3月26日-27日", //线下公开课时间
          pos: "深圳", //线下公开课地点
          month: 3, //线下公开课月份
        },
        {
          name: "技术创新管理（平台、技术与重用）", //线下公开课名称
          cover: require("~/static/images/1.jpg"), //线下公开课封面
          start_time: "2021年3月26日-27日", //线下公开课时间
          pos: "深圳", //线下公开课地点
          month: 3, //线下公开课月份
        },
        {
          name: "自行车自行车自行车自行车自行车", //线下公开课名称
          cover: require("~/static/images/1.jpg"), //线下公开课封面
          start_time: "2021年3月26日-27日", //线下公开课时间
          pos: "深圳", //线下公开课地点
          month: 3, //线下公开课月份
        },
        {
          name: "自行车自行车自行车自行车自行车", //线下公开课名称
          cover: require("~/static/images/1.jpg"), //线下公开课封面
          start_time: "2021年3月26日-27日", //线下公开课时间
          pos: "深圳", //线下公开课地点
          month: 3, //线下公开课月份
        },
        {
          name: "自行车自行车自行车自行车自行车", //线下公开课名称
          cover: require("~/static/images/1.jpg"), //线下公开课封面
          start_time: "2021年3月26日-27日", //线下公开课时间
          pos: "深圳", //线下公开课地点
          month: 3, //线下公开课月份
        },
      ],
      swiperOptions: {
        loop: false, // 循环模式选项
        observer: true, //修改swiper自己或子元素时，自动初始化swiper
        observeParents: true, //修改swiper的父元素时，自动初始化swiper
        navigation: {
          nextEl: ".index-class-next",
          prevEl: ".index-class-prev",
        },
      },
    };
  },
  computed: {
    formatData() {
      var a = this.classes;
      var b = [];
      var result = [];
      var k = 0;

      for (var i = 0; i < a.length; ++i) {
        if (i % 3 == 0) {
          b = [];
          for (var j = 0; j < 3; ++j) {
            if (a[i + j] == undefined) {
              continue;
            } else {
              b[j] = a[i + j];
            }
          }
          result[k] = b;
          k++;
        }
      }
      console.log(result);
      return result;
    },
  },
  methods: {
    prev() {
      this.$refs.mySwiper.swiper.slidePrev();
    },
    next() {
      this.$refs.mySwiper.swiper.slideNext();
    },
  },
};
</script>
<style lang="scss">
//近期公开课
.public-class {
  .index-class-swiper {
    overflow: hidden;
    margin-bottom: 50px;
  }

  .class-list {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    column-gap: 30px;
    margin: unset;

    li {
      position: relative;

      &:last-child {
        margin-right: unset;
      }
    }

    .time-tag {
      position: absolute;
      top: 0;
      left: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      width: 50px;
      height: 50px;
      background-color: #9a1e23;
      color: #fff;
      font-family: MicrosoftYaHei;
      font-size: 12px;
      font-weight: normal;
      letter-spacing: 0px;

      .month {
        vertical-align: baseline;
      }

      span {
        font-size: 28px;
      }
    }

    .class-cover {
      width: 100%;
      // object-fit: contain;
    }

    .info-box {
      background-color: #f2f2f2;
      box-sizing: border-box;
      padding: 17px 12px;
    }

    .class-name {
      padding-bottom: 14px;
      font-family: MicrosoftYaHei-Bold;
      font-size: 14px;
      font-weight: bold;
      font-stretch: normal;
      letter-spacing: 0px;
      color: #333333;
    }

    .other-info {
      display: flex;
      justify-content: space-between;
      padding-top: 18px;
      font-family: MicrosoftYaHei;
      font-size: 13px;
      font-weight: normal;
      font-stretch: normal;
      letter-spacing: 0px;
      color: #333333;
      border-top: 1px solid #e5e5e5;

      .icon {
        width: 14px;
        object-fit: contain;
        margin-right: 6px;
      }

      .start-time {
        display: flex;
        align-items: center;

        span {
          font-family: MicrosoftYaHei-Bold;
          font-size: 13px;
          font-weight: normal;
          letter-spacing: 0px;
          color: #9a1e23;
        }
      }

      .address {
        display: flex;
        align-items: center;
      }
    }
  }

  .class-info-switch-btn {
    display: flex;
    width: 160px;
    height: 47px;
    margin: 0 auto;
    margin-bottom: 60px;
    border-radius: 10px;
    overflow: hidden;

    .index-class-prev,
    .index-class-next {
      flex: 1;
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: #f0f0f0;
      transition: all 0.3s;

      .active-btn {
        display: none;
      }

      &:hover {
        background-color: #9a1e23;

        .normal-btn {
          display: none;
        }

        .active-btn {
          display: block;
        }
      }
    }

    .index-class-prev {
      img {
        transform: translateY(50%);
      }
    }

    .index-class-next {
      img {
        transform: translateY(-50%);
      }
    }
  }
}
</style>
