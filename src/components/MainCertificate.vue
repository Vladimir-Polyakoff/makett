<script>
export default {
  name: 'MainCertificate',

  data () {
    return {
      list: [
        {
          imgSrc: require('@/img/cert1.svg')
        },
        {
          imgSrc: require('@/img/cert2.svg')
        },
        {
          imgSrc: require('@/img/cert3.svg')
        }
      ]
    }
  }
}
</script>

<template>
  <div class="max-width">
    <div class="container">

      <div class="sub-title">Createx Certificate</div>
      <div class="title">Your expertise will be confirmed</div>

      <div class="description">We are accredited by international professional organizations and institutes:</div>

      <div class="img-box">
        <div v-for="logo in list" :key="logo.imgSrc" class="logo">
          <img :src="logo.imgSrc"/>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
 * {
    font-family: 'Lato';
  }
  .max-width {
    width: 1920px;
    background: #fff;
    padding-top: 120px;
  }
  .container {
    position: relative;
    max-width: 1320px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    &::after {
      content: '';
      background: url('../img/certificate.png');
      position: absolute;
      right: 0px;
      top: 0px;
      width: 705px;
      height: 500px;
      border-radius: 4px;
    }
    .sub-title {
      font-weight: 700;
      font-size: 16px;
      line-height: 150%;
      letter-spacing: 1px;
      text-transform: uppercase;
      color: #1E212C;
    }

    .title {
      max-width: 392px;
      text-align: start;
      font-weight: 900;
      font-size: 46px;
      line-height: 130%;
      color: #1E212C;
      margin-bottom: 48px;
    }

    .description {
      max-width: 390px;
      text-align: start;
      font-size: 16px;
      line-height: 160%;
      color: #424551;
      margin-bottom: 32px;
    }
    .img-box {
      display: flex;
      gap: 40px;
      margin-bottom: 111px;
    }
  }
</style>
