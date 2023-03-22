<template>
  <div class="container">
    <div class="play">Play showreel</div>
    <div class="description">Enjoy studying
      with Createx Online Courses
    </div>
    <div class="actions">
      <button class="about">About us</button>
      <button class="coursess">Explore courses</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderContant'
}
</script>

<style scoped lang="scss">
  * {
      font-family: 'Lato';
  }
  .container {
    position: relative;
    margin: 0 auto;
    max-width: 1320px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-top: 150px;
    .play {
      font-weight: 700;
      font-size: 14px;
      line-height: 150%;
      color: #1E212C;
      margin:0px 0px 56px 84px;
      &::before {
        content: '';
        position: absolute;
        top: -32px;
        left: 0;
        background: url('../img/hover.svg');
        width: 84px;
        height: 84px;
      }
    }
      .description {
      font-weight: 900;
      font-size: 64px;
      line-height: 130%;
      display: flex;
      align-items: center;
      letter-spacing: 1px;
      color: #1E212C;
      max-width: 496px;
      text-align: start;
      margin-bottom:60px;
      &::before {
        content: '';
        position: absolute;
        background: url('../img/illustration.svg');
        width: 602px;
        height: 551px;
        top: -20px;
        right: 0px;
      }
    }
    .actions {
      display: flex;
      gap: 24px;
      margin-bottom: 259px;
      .about {
        padding: 0px 40px;
        gap: 10px;
        height: 52px;
        border-radius: 4px;
        background: inherit;
        font-weight: 700;
        font-size: 16px;
        line-height: 52px;
        letter-spacing: 0.5px;
        border: 1px solid #F75E05;
        background: linear-gradient(55.95deg, #FF3F3A 0%, #F75E05 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
        text-fill-color: transparent;
      }
      .coursess {
        padding: 0px 40px;
        gap: 10px;
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
  }
</style>
