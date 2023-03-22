<template>
  <div class="menu">
    <div class="menu__logo"><img src="@/img/logo.svg"></div>
      <ul class="menu__link">
        <li v-for="link in list" :key="link">
          {{ link }}
        </li>
      </ul>
    <div class="actions">
      <button class="actions__consultation">Get consultation</button>
      <button class="actions__log-in"><img src="@/img/account.svg"></button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheMenu',

  data () {
    return {
      list: ['About Us', 'Courses', 'Events', 'Blog', 'Contacts']
    }
  }
}
</script>

<style scoped lang="scss">
  * {
      font-family: 'Lato';
  }
  .menu {
    position: relative;
    margin: 0 auto;
    max-width: 1320px;
    display: flex;
    justify-content: flex-start;
    padding-top: 20px;

    &__logo {
      padding-top: 20px;
      margin-right: 60px;
      &::after {
        content: '';
        position: absolute;
        top: 133px;
        left: -220px;
        background: url('../img/shapes.svg');
        width: 96px;
        height: 96px;
      }
    }

    &__link {
      display: flex;
      gap: 40px ;
      margin-right: 225px;

      li {
        list-style: none;
        font-weight: 700;
        font-size: 16px;
        line-height: 160%;
        color: #424551;
      }
    }

    .actions {
      display: flex;

      &__consultation {
        padding: 0px 40px;
        background: linear-gradient(55.95deg, #FF3F3A 0%, #F75E05 100%);
        border: none;
        border-radius: 4px;
        font-weight: 700;
        font-size: 16px;
        line-height: 52px;
        letter-spacing: 0.5px;
        color: #FFFFFF;
        margin-right: 36px;
      }
      &__log-in {
        background: inherit;
        border: none;
        &::after {
          content: '';
          position: absolute;
          top: -40px;
          right: -74px;
          background: url('../img/shapes.svg');
          width: 96px;
          height: 96px;
          transform: rotate(134deg);
        }
      }
    }
  }
</style>
