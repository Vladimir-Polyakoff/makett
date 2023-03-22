<script>
export default {
  name: 'MainWorkshop',

  data () {
    return {
      list: [
        {
          day: '05',
          month: 'August',
          time: '11:00-14:00',
          description: 'Formation of the organizational structure of the company in the face of uncertainty.',
          format: 'Onine master-class',
          button: 'View more'
        },
        {
          day: '24',
          month: 'July',
          time: '11:00-12:30',
          description: 'Building a customer service department. Best Practices.',
          format: 'Onine lecture',
          button: 'View more'
        },
        {
          day: '05',
          month: 'July',
          time: '11:00-13:00',
          description: 'How to apply methods of speculative design in practice. Worldbuilding prototyping.',
          format: 'Onine workshop',
          button: 'View more'
        }
      ]
    }
  }
}
</script>
<template>
  <div class="max-width">
    <div class="container">

        <img  class="title" src="@/img/work.svg">

        <div class="card-container">
          <div v-for="card in list" :key="card.day" class="card">

            <div class="day">{{ card.day }}</div>

            <div class="month-box">
              <div class="month">{{ card.month }}</div>
              <div class="time">{{ card.time }}</div>
            </div>

            <div class="desc-space">
              <div class="description-box">
                <div class="description">{{ card.description }}</div>
                <div class="format">{{ card.format }}</div>
              </div>

              <button>{{ card.button }}</button>
            </div>
          </div>
        </div>

        <div class="footer">
          <div class="footer__question">Do you want more?</div>
          <button class="footer__button">Explore all events</button>
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
    background: rgba(250, 188, 180, 0.7333333333);
    padding-bottom: 80px;
  }
  .container {
    position: relative;
    max-width: 1320px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    &::before {
      content: '';
      background: url('../img/dots.svg');
      position: absolute;
      left: -320px;
      bottom: 0px;
      width: 171px;
      height: 132px;
      transform: rotate(90deg);
      opacity: .6;
    }
    &::after {
      content: '';
      background: url('../img/Group.svg');
      position: absolute;
      right:-300px;
      top: -2px;
      width: 168px;
      height: 130px;
      opacity: .2;
      transform: rotate(181deg);
    }
    .title {
      width: 461px;
      height: 92px;
      margin: 80px auto 60px;
    }
    .card-container {
      margin-bottom: 65px;
    }
    .card {
      max-width: 1230px;
      height: 126px;
      background: #FFFFFF;
      border-radius: 4px;
      margin-bottom: 24px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      text-align: start;
      padding-inline: 40px;
      &:hover {
        box-shadow: 0px 80px 80px -20px rgba(255, 63, 58, 0.16), 0px 30px 24px -10px rgba(255, 63, 58, 0.1), 0px 12px 10px -6px rgba(255, 63, 58, 0.08), 0px 4px 4px -4px rgba(30, 33, 44, 0.05);
      }
      .day {
        font-weight: 900;
        font-size: 48px;
        line-height: 130%;
        letter-spacing: 1px;
        color: #FF3F3A;
      }
      .month-box {
        margin-right: 40px;
        .month {
          font-weight: 700;
          font-size: 20px;
          line-height: 150%;
          color: #1E212C;
        }
        .time {
          font-size: 16px;
          line-height: 160%;
          color: #787A80;
        }
      }
      .description-box {
        width: 757px;
        margin-right: 40px;
        flex-direction: column;
        display: flex;
        flex:0 1 auto ;
        .description {
          font-weight: 700;
          font-size: 20px;
          line-height: 150%;
          color: #1E212C;
        }
        .format {
          font-size: 16px;
          line-height: 160%;
          display: flex;
          align-items: center;
          color: #787A80;
        }
      }
      button {
        display: flex;
        justify-content:center;
        align-items: center;
        width: 136px;
        height: 44px;
        border-radius: 4px;
        font-size: 14px;
        line-height: 44px;
        letter-spacing: 0.5px;
        background: linear-gradient(55.95deg, #FF3F3A 0%, #F75E05 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
        text-fill-color: transparent;
        &:hover {
          background: linear-gradient(55.95deg, #FF3F3A 0%, #F75E05 100%);
          color: #fff;
          text-fill-color: #fff;
          -webkit-text-fill-color: #fff;
          border: none;
        }
      }
      .desc-space {
        display: flex;
        justify-content: space-evenly;
        flex: 0 1 auto;
      }
    }
    .footer {
      display: flex;
      justify-content: center;
      gap: 40px;
      &__question {
        font-weight: 700;
        font-size: 28px;
        line-height: 150%;
        color: #1E212C;
      }
      &__button {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 214px;
        height: 52px;
        background: linear-gradient(55.95deg, #FF3F3A 0%, #F75E05 100%);
        border-radius: 4px;
        font-weight: 700;
        font-size: 16px;
        line-height: 52px;
        display: flex;
        letter-spacing: 0.5px;
        color: #FFFFFF;
        border: none;
      }
    }
  }
</style>
