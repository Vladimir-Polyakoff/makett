<script>
export default {
  name: 'HeaderFooter',

  data () {
    return {
      list: [
        {
          num: '1200',
          title: 'Students graduated'
        },
        {
          num: '84',
          title: 'Completed courses'
        },
        {
          num: '16',
          title: 'Qualified tutors'
        },
        {
          num: '5',
          title: 'Years of experience'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="container">

    <div class="footer">
      <div v-for="item in list" :key="item.title" class="footer__item">
          <span class="num">{{ item.num }}</span><span class="title">{{ item.title }}</span>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
  * {
    font-family: 'Lato';
  }
  .footer {
    position: relative;
    margin: 0 auto;
    max-width: 1320px;
    display: flex;
    margin-bottom: 50px;
    &::before {
        content: '';
        left: -300px;
        top: -34px;
        position: absolute;
        background: url('../img/Group.svg');
        width: 171px;
        height: 143px;
        opacity: .2;
    }
    &::after {
        content: '';
        right:-310px;
        top: -157px;
        position: absolute;
        background: url('../img/dots.svg');
        width: 136px;
        height: 130px;
    }
    &__item {
      display: flex;
    }
    .num {
      font-weight: 900;
      font-size: 46px;
      line-height: 130%;
      color: #1E212C;
      margin-right: 12px;
    }
    .title {
      font-size: 16px;
      line-height: 160%;
      min-width: 137px;
      display: flex;
      align-items: center;
      color: #1E212C;
      margin-right: 140px;
      &::before {
        content: '';
        left:200px;
        position: relative;
        background: url('../img/ellipse.svg');
        width: 8px;
        height: 8px;
      }
    }
  }
</style>
