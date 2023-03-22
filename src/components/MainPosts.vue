<script>
export default {
  name: 'MainPosts',

  data () {
    return {
      list: [
        {
          imgSrc: require('@/img/post1.svg'),
          badge: require('@/img/podcast.svg'),
          meta: require('@/img/meta1.svg'),
          question: 'What is traffic arbitrage and does it really make money?',
          description: 'Pharetra, ullamcorper iaculis viverra parturient sed id sed. Convallis proin dignissim lacus, purus gravida...',
          next: 'Listen'
        },
        {
          imgSrc: require('@/img/post2.svg'),
          badge: require('@/img/video.svg'),
          meta: require('@/img/meta2.svg'),
          question: 'What to do and who to talk to if you want to get feedback on the product',
          description: 'Neque a, senectus consectetur odio in aliquet nec eu. Ultricies ac nibh urna urna sagittis faucibus...',
          next: 'Watch'
        },
        {
          imgSrc: require('@/img/post3.svg'),
          badge: require('@/img/article.svg'),
          meta: require('@/img/meta3.svg'),
          question: 'Should you choose a creative profession if you are attracted to creativity?',
          description: 'Curabitur nisl tincidunt eros venenatis vestibulum ac placerat. Tortor, viverra sed vulputate ultrices...',
          next: 'Read'
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
        <img src="@/img/posts.svg" class="title"/>
        <button>Go to blog</button>
      </div>

      <div class="card-box">
        <div v-for="card in list" :key="card.meta" class="card">
          <img class="card__badge" :src="card.badge"/>
          <img class="card__img" :src="card.imgSrc"/>
          <img class="card__meta" :src="card.meta"/>
          <div class="card__question">{{ card.question }}</div>
          <div class="card__description">{{ card.description }}</div>
          <div class="next-arr">
            <div class="next-arr__next">{{ card.next }}</div>
            <img class="next-arr__arr" src="@/img/arr-back.svg">
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
    padding-top: 130px;
    padding-bottom: 180px;
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
      align-items: flex-end;
      margin-bottom: 60px;
      button {
        background: linear-gradient(55.95deg, #FF3F3A 0%, #F75E05 100%);
        border-radius: 4px;
        font-weight: 700;
        font-size: 16px;
        line-height: 52px;
        display: flex;
        align-items: center;
        text-align: center;
        letter-spacing: 0.5px;
        color: #FFFFFF;
        padding: 0px 40px;
        border: none;
      }
    }

    .card-box {
      display: flex;
      gap: 30px;
      margin-left: 40px;
      .card {
          position: relative;
          width: 390px;
          text-align: start;
        &__badge {
          position: absolute;
          top: 12px;
          left: 12px;
        }
        &__img {
          margin-bottom: 16px;
        }
        &__meta {
          margin-bottom: 8px;
        }
        &__question {
          font-weight: 700;
          font-size: 20px;
          line-height: 150%;
          margin-bottom: 8px;
          color: #1E212C;
        }
        &__description {
          font-size: 16px;
          line-height: 160%;
          color: #424551;
          margin-bottom: 16px;
        }
        .next-arr {
          display: flex;
          gap: 8px;
          &__next {
            font-weight: 700;
            font-size: 16px;
            line-height: 160%;
            color: #1E212C;
            margin-right: 8px;
          }
          &__arr {
            transform: rotate(180deg);
          }
        }
      }
    }
  }
</style>
