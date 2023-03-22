<script>
export default {
  name: 'FooterSubscribe'
}
</script>

<template>
  <div class="max-width">
    <div class="container">

        <div class="sub-title">Don’t miss anything</div>
        <div class="title">Subscribe to the Createx School announcements</div>

      <div class="input-box">
        <input type="text" placeholder="Your working email">
        <button class="">Subscribe</button>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
 * {
    font-family: 'Lato';
  }
  .max-width {
    position: relative;
    width: 1920px;
    background: rgba(250, 188, 180, 0.7333333333);
    padding-top: 120px;
    &::before {
      content: '';
      display: inline-block;
      position: absolute;
      left: 0;
      bottom: 0;
      width: 354px;
      height: 246px;
      background: url('../img/footerImg.svg');
    }
    &::after {
      content: '';
      display: inline-block;
      position: absolute;
      right: 0px;
      bottom: 0px;
      width: 354px;
      height: 246px;
      background: url('../img/footerImg.svg');
    }
  }
  .container {
    max-width: 1320px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-bottom: 180px;
    .sub-title {
      font-size: 16px;
      font-weight: 700;
      line-height: 150%;
      text-align: center;
      letter-spacing: 1px;
      text-transform: uppercase;
      color: #1E212C;
      margin-bottom: 8px;
    }
    .title {
      max-width: 800px;
      font-style: normal;
      font-weight: 700;
      font-size: 46px;
      line-height: 130%;
      text-align: center;
      color: #1E212C;
      margin-bottom: 50px;
    }
    input {
      width: 422px;
      height: 52px;
      padding-left:16px ;
      border: none;
      margin-right: 24px;
    }
    button {
      width: 154px;
      height: 52px;
      background: linear-gradient(55.95deg, #FF3F3A 0%, #F75E05 100%);
      border-radius: 4px;
      border: none;
      font-weight: 700;
      font-size: 16px;
      line-height: 52px;
      letter-spacing: 0.5px;
      color: #FFFFFF;
    }
  }
</style>
