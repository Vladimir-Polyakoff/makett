<script>
export default {
  name: 'MainTeam',

  data () {
    return {
      list: [
        {
          imgSrc: require('@/img/5.png'),
          name: 'Dianne Russell',
          speciality: 'Founder and CEO'
        },
        {
          imgSrc: require('@/img/1.png'),
          name: 'Jerome Bell',
          speciality: 'Founder and Program Director'
        },
        {
          imgSrc: require('@/img/4.png'),
          name: 'Kristin Watson',
          speciality: 'Marketer, Curator of Marketing Course'
        },
        {
          imgSrc: require('@/img/2.png'),
          name: 'Marvin McKinney',
          speciality: 'PM, Curator of Management Course'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="max-width">
    <div class="container">

      <div class="title-box">
        <img src="@/img/team.svg" class="title"/>
        <img src="@/img/arrow.svg" class="arrow"/>
      </div>

      <div class="card-box">
        <div v-for="card in list" :key="card.name" class="card">
          <img :src="card.imgSrc"/>
          <div class="name">{{ card.name}}</div>
          <div class="speciality">{{ card.speciality}}</div>
        </div>
      </div>

      <div class="testomonials-box">
        <img src="@/img/testi.svg" class="title">
        <div class="testomonials">
          <div class="description">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Justo, amet lectus quam viverra mus lobortis fermentum amet, eu. Pulvinar eu sed purus facilisi. Vitae id turpis tempus ornare turpis quis non. Congue tortor in euismod vulputate etiam eros. Pulvinar neque pharetra arcu diam maecenas diam integer in.</div>
            <img src="@/img/user-profile.svg" class="user">
        </div>
      </div>

      <div class="progress">
        <span></span><span></span><span></span><span></span><span></span>
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
    background: #F4F5F7;
    padding-top: 175px;
    &::before {
      content: '';
      display: inline-block;
      position: relative;
      left: 453px;
      top: -108px;
      width: 143px;
      height: 105px;
      background: url('../img/dots.svg');
    }
    &::after {
      content: '';
      display: inline-block;
      position: relative;
      left: -824px;
      top: -662px;
      width: 143px;
      height: 145px;
      background: url('../img/circlesTeam.svg');
    }
  }
  .container {
    position: relative;
    max-width: 1320px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    .title-box {
      width: 100%;
      display: flex;
      justify-content: space-between;
      margin-bottom: 60px;
    }
    .card-box {
      display: flex;
      margin-bottom: 180px;
      gap: 30px;
      .card {
        img {
          width: 285px;
        }
      }
      .name {
        font-weight: 700;
        font-size: 20px;
        line-height: 150%;
        text-align: center;
        color: #424551;
        margin: 16px 0px 4px 0;
      }
    }

    .testomonials-box {
      margin: 0 auto 60px;
      .title {
        margin-bottom: 60px;
      }
      .testomonials {
        max-width: 1020px;
        background: #FFFFFF;
        box-shadow: 0px 80px 80px -20px rgba(154, 156, 165, 0.08), 0px 30px 24px -10px rgba(154, 156, 165, 0.05), 0px 12px 10px -6px rgba(154, 156, 165, 0.04), 0px 4px 4px -4px rgba(30, 33, 44, 0.03);
        border-radius: 4px;
        padding: 54px 106px 54px 164px;
        text-align: start;
        &::before {
          content: '';
          position: absolute;
          left: 0px;
          top: 1000px;
          width: 24px;
          height: 24px;
          background: url('../img/arr-back.svg');
        }
        &::after {
          content: '';
          position: absolute;
          right: 0px;
          top: 1000px;
          width: 48px;
          height: 48px;
          background: url('../img/arr-next.svg');
        }
        .description {
          font-size: 20px;
          line-height: 150%;
          color: #424551;
          max-width: 752px;
          margin-bottom: 24px;
          &::before {
            content: '';
            position: absolute;
            left: 260px;
            width: 28px;
            height: 20px;
            background: url('../img/braces.svg');
          }
        }
      }
    }

    .progress {
      width: 100%;
      display: flex;
      justify-content: center;
      margin-bottom: 90px;
      &::after {
        content: '';
        display: inline-block;
        position: absolute;
        right: -314px;
        bottom: -136px;
        width: 171px;
        height: 144px;
        transform: rotate(270deg);
        background: url('../img/Group.svg');
      }
      span {
        display: inline-block;
        width: 30px;
        height: 3px;
        margin-right: 12px;
        background: #B3B7BC;
      }
    }
  }
</style>
