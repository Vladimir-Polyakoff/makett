<script>
export default {
  name: 'MainFeatured',

  data () {
    return {
      list: [
        {
          imgSrc: require('@/img/1.png'),
          buttonStyles: 'background: #03CEA4;',
          title: 'Marketing',
          description: 'The Ultimate Google Ads Training Course',
          price: '$100 |',
          name: 'by Jerome Bell'
        },
        {
          imgSrc: require('@/img/2.png'),
          buttonStyles: 'background: #5A87FC;',
          title: 'Management',
          description: 'Prduct Management Fundamentals',
          price: '$480 |',
          name: 'by Marvin McKinney'
        },
        {
          imgSrc: require('@/img/3.png'),
          buttonStyles: 'background: #F89828;',
          title: 'HR & Recruting',
          description: 'HR  Management and Analytics',
          price: '$200 |',
          name: 'by Leslie Alexander Li'
        },
        {
          imgSrc: require('@/img/4.png'),
          buttonStyles: 'background: #03CEA4;',
          title: 'Market',
          description: 'Brand Management & PR Communications',
          price: '$530 |',
          name: 'by Kristin Watson'
        },
        {
          imgSrc: require('@/img/5.png'),
          buttonStyles: 'background: #5A87FC;',
          title: 'Managеment',
          description: 'Business Development Management',
          price: '$400 |',
          name: 'by Dianne Russell'
        },
        {
          imgSrc: require('@/img/6.png'),
          buttonStyles: 'background: #F52F6E;',
          title: 'Design',
          description: 'Graphic Design Basic',
          price: '$500 |',
          name: 'by Guy Hawkins'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="max-width">
    <div class="container">

      <div class="title">
        <img src="@/img/feat.svg">
        <button>View all courses</button>
      </div>

        <div class="card-container">
          <div v-for="card in list" :key="card.title" class="card">
            <img :src="card.imgSrc" class="photo"/>

            <div class="description-box">
              <div
                class="card-title"
                :style="card.buttonStyles"
              >{{ card.title }}</div>
              <div class="description">{{ card.description}}</div>

              <div class="name-box">
                <div class="price">{{ card.price}}</div>
                <div class="name">{{ card.name}}</div>
              </div>
            </div>

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
    padding-bottom: 180px;
  }
  .container {
    position: relative;
    max-width: 1320px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    .title {
      width: 100%;
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      margin-bottom: 60px;
      button {
        width: 202px;
        height: 52px;
        border-radius: 4px;
        font-weight: 700;
        font-size: 16px;
        line-height: 52px;
        letter-spacing: 0.5px;
        background: inherit;
        border-color: #F75E05;
        color:#F75E05;
        margin-right: 90px;
      }
    }
    .card-container {
      display: flex;
      gap: 30px;
      flex-wrap: wrap;
      .card {
        display: flex;
        width: 600px;
        height: 214px;
        left: 345px;
        top: 2152px;
        background: #FFFFFF;
        border: 1px solid #E5E8ED;
        box-shadow: 0px 80px 80px -20px rgba(154, 156, 165, 0.08), 0px 30px 24px -10px rgba(154, 156, 165, 0.05), 0px 12px 10px -6px rgba(154, 156, 165, 0.04), 0px 4px 4px -4px rgba(30, 33, 44, 0.03);
        border-radius: 4px;
        gap: 32px;
        .photo:nth-child(1n) {
          width: 214px;
          height: 214px;
          border-radius: 4px 0px 0px 4px
        }
        .description-box {
          display: flex;
          flex-direction: column;
          align-items: flex-start;
          justify-content: center;
          gap: 20px;
          .card-title {
            width: 112px;
            height: 23px;
            background:  #03CEA4;
            border-radius: 4px;
            font-size: 14px;
            line-height: 150%;
            color: #FFFFFF;
            padding: 2px 8px;
            display: flex;
            align-items: center;
            justify-content: center;
          }
          .description {
            width: 322px;
            font-weight: 700;
            font-size: 20px;
            line-height: 150%;
            color: #1E212C;
            text-align: start;
          }
          .name-box {
            display: flex;
            gap: 4px;
            .price {
              font-weight: 700;
              font-size: 18px;
              line-height: 150%;
              color: #FF4242;
            }
            .name {
              font-size: 18px;
              line-height: 150%;
              color: #787A80;
            }
          }
        }
      }
    }
  }
</style>
