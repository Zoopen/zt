<template>
  <div>
    <Banner />
    <Ourservice />
    <Advantage />
    <Successfulcase />
    <Evaluation />
    <Openclass />
    <News />
  </div>
</template>

<script>
export default {};
</script>
<style lang="scss">
@mixin no-select() {
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
body {
  overflow-x: hidden;
  @include no-select;
}
ul {
  padding: unset;
}

a{
  text-decoration: none!important;
}

ul,
ol,
li {
  list-style: none;
}
section{
  overflow: hidden;
}
@mixin title-component() {
  .title-component {
    overflow: hidden;
    text-align: center;
    justify-content: center;

    h3 {
      margin-top: 60px;
      margin-bottom: 20px;
      font-family: MicrosoftYaHei-Bold;
      font-size: 28px;
      font-weight: normal;
      font-stretch: normal;
      line-height: 36px;
      letter-spacing: 0px;
      color: #333333;
    }

    h4 {
      margin-bottom: 50px;
      font-family: MicrosoftYaHei;
      font-size: 14px;
      font-weight: normal;
      font-stretch: normal;
      letter-spacing: 0px;
      color: #999999;
    }
  }
}

@include title-component;
</style>
