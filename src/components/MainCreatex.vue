<script>
export default {
  name: 'MainCreatex',

  data () {
    return {
      creatList: [
        {
          icon: '',
          desription: 'A fermentum in morbi pretium aliquam adipiscing donec tempus.'
        },
        {
          icon: '',
          desription: 'Vulputate placerat amet pulvinar lorem nisl.'
        },
        {
          icon: '',
          desription: 'Consequat feugiat habitant gravida quisque elit bibendum id adipiscing sed.'
        },
        {
          icon: '',
          desription: 'Etiam duis lobortis in fames ultrices commodo nibh.'
        },
        {
          icon: '',
          desription: 'Tincidunt sagittis neque sem ac eget.'
        },
        {
          icon: '',
          desription: 'Ultricies amet justo et eget quisque purus vulputate dapibus tortor.'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="max-width">
    <div class="container">
      <div>
        <img  class="photo" src="@/img/image.png">
      </div>
      <div class="list-container">
        <img src="@/img/heading.svg" class="title">
        <div class="list">
          <div v-for="item in creatList" :key="item.description" class="list__item"><span class="icon">{{ item.icon }}</span> <span>{{ item.desription }}</span></div>
        </div>
        <button>More about us</button>
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
    background: #fff; //!
  }
  .container {
    position: relative;
    max-width: 1320px;
    padding-top: 210px;
    margin: 0 auto;
    display: flex;
    padding-bottom: 180px;
    &::before {
      content: '';
      position: absolute;
      left: -331px;
      background: url('../img/dots1.svg');
      width: 102.18px;
      height: 124.74px;
      opacity: 0.8;
      transform: rotate(-129.46deg);
    }
    &::after {
      content: '';
      background: url('../img/circles.svg');
      position: absolute;
      width: 122px;
      height: 287px;
      right: -302px;
      bottom: 0px;
      mix-blend-mode: multiply;
    }
    .photo {
      margin-right: 135px;
    }
    .list-container {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      text-align: start;
      .title {
        margin-bottom: 40px;
      }
      .list {
        max-width: 358px;
      }
      .list__item {
        font-size: 16px;
        line-height: 160%;
        color: #424551;
        display: flex;
        gap: 12px;
        margin-bottom: 12px;
        margin-left: 28px;
        .icon {
          position: absolute;
          right: 470px;
          background: url('../img/check.svg');
          display:inline-block;
          width: 16px;
          height: 16px;
          margin-top: 4px;
        }
      }
      button {
        width: 161px;
        height: 44px;
        left: 1185px;
        top: 1734px;
        background: linear-gradient(55.95deg, #FF3F3A 0%, #F75E05 100%);
        border-radius: 4px;
        font-weight: 500;
        font-size: 14px;
        line-height: 44px;
        letter-spacing: 0.5px;
        color: #FFFFFF;
        border:none;
      }
    }
  }
</style>
