<script>
export default {
  name: 'MainBenefits'
}
</script>

<template>
  <div class="max-width">
    <div class="container">
      <div>
        <div class="sub-title">Our benefits</div>
        <div class="title">That’s how we do it</div>
      </div>

      <div class="actions">
        <button class="star">Experienced Tutors</button>
        <button class="feed">Feedback & Support</button>
        <button class="library">24/7 Online Library</button>
        <button class="community">Community</button>
      </div>
      <div class="list-container">
        <div class="list-container__title">Only practicing tutors</div>
          <div class="list-container__description">Urna nisi, arcu cras nunc. Aenean quam est lobortis   mi non fames dictum suspendisse. Morbi mauris cras massa ut dolor quis sociis mollis augue. Nunc, sodales tortor sit diam mi amet massa. Fermentum diam diam sociis vestibulum. Nulla nisl accumsan, id dignissim massa ut amet. Amet enim, nisi tempus vehicula.
        </div>
      </div>
      <img src="../img/mack.svg">
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
  }
  .container {
    position: relative;
    max-width: 1320px;
    padding-top: 60px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    padding-bottom: 100px;
    padding-bottom: 240px;
    img {
      width: 600px;
      height: 440px;
      position: absolute;
      right: 100px;
      bottom: 120px;
    }
    .sub-title {
      font-weight: 700;
      font-size: 16px;
      line-height: 150%;
      text-align: center;
      letter-spacing: 1px;
      text-transform: uppercase;
      color: #1E212C;
    }
    .title {
      font-weight: 900;
      font-size: 46px;
      line-height: 130%;
      text-align: center;
      color: #1E212C;
      margin-bottom: 60px;
    }
    .actions {
      position: relative;
      display: flex;
      margin-bottom: 182px;
      button {
        width: 307px;
        height: 46px;
        font-weight: 700;
        font-size: 16px;
        line-height: 160%;
        display: flex;
        justify-content: center;
        align-items: center;
        color: #9A9CA5;
        background: inherit;
        border: none;
        &:hover {
          border: 1px solid #FF3F3A;
          border-radius: 4px;
          color: #FF3F3A;
        }
      }
      .star::before {
        content: '';
          width: 15px;
          height: 14px;
          position: absolute;
          top: 15px;
          left: 61px;
          background: url('../img/star.svg');
      }
      .feed::before {
        content: '';
          width: 15px;
          height: 15px;
          position: absolute;
          top: 15px;
          left: 361px;
          background: url('../img/like.svg');
      }
      .library::before {
        content: '';
          width: 15px;
          height: 15px;
          position: absolute;
          top: 15px;
          left: 671px;
          background: url('../img/layouts.svg');
      }
      .community::before {
        content: '';
          width: 15px;
          height: 15px;
          position: absolute;
          top: 15px;
          left: 1004px;
          background: url('../img/chat.svg');
      }
    }
    .list-container {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      text-align: start;
      max-width: 495px;
      &__title {
        font-weight: 900;
        font-size: 32px;
        line-height: 130%;
        color: #1E212C;
        margin-bottom: 24px;
      }
      &__description {
        font-size: 16px;
        line-height: 160%;
        color: #424551;
      }
    }
  }
</style>
