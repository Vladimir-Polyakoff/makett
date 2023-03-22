<script>
export default {
  name: 'FooterContact',

  data () {
    return {
      list: [
        {
          logo: require('@/img/footerLogo.svg'),
          description: 'Createx Online School is a leader in online studying. We have lots of courses and programs from the main market experts. We provide relevant approaches to online learning, internships and employment in the largest companies in the country. ',
          icons: require('@/img/socials.svg')
        }
      ],
      columnLIst: [
        [
          'SITE MAP',
          'About Us',
          'Courses',
          'Events',
          'Contacts'
        ],
        [
          'COURSES',
          'Marketing',
          'Management',
          'HR & Recruting',
          'Design',
          'Development'
        ],
        [
          'CONTACT US',
          '(405) 555-0128',
          'hello@createx.com'
        ]
      ]
    }
  }
}
</script>

<template>
  <div class="max-width">
    <div class="container">
      <div class="socials">
        <div v-for="block in list" :key="block.title" class="socials__blocks">

          <div class="site-logo">
            <img :src="block.logo" class="title"/>
            <div class="description">{{ block.description }}</div>
            <img :src="block.icons" class="icon"/>
          </div>
        </div>

        <div v-for="column in columnLIst" :key="column[0]" class="contacts">
          <div
            v-for="(item, index) in column"
            :key="item"
            :class="!index ? 'contacts__title' : 'contacts__item'"
          >{{ item }}</div>
        </div>

      </div>
    </div>
    <div class="copyright">
      <img src="@/img/copyright.svg">
      <button class="arrow-top">GO TO TOP</button>
    </div>
  </div>
</template>

<style scoped lang="scss">
 * {
    font-family: 'Lato';
  }
  .max-width {
    width: 1920px;
    background: #1E212C;
    padding-top: 80px;
  }
  .container {
    max-width: 1320px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-bottom: 60px;

    .socials {
      display: flex;
      text-align: start;
      gap: 80px;
    }

    .site-logo {
      max-width: 280px;
      .title {
        margin-bottom: 24px;
      }
    }
    .description {
      font-size: 12px;
      line-height: 150%;
      color: #FFFFFF;
      margin-bottom: 38px;
      opacity: .3;
    }

    .contacts__title {
      font-weight: 700;
      font-size: 16px;
      line-height: 150%;
      letter-spacing: 1px;
      text-transform: uppercase;
      color: #FFFFFF;
      margin-bottom: 12px;
    }
    .contacts__item {
      font-size: 16px;
      line-height: 160%;
      color: #FFFFFF;
      opacity: .3;
      margin-bottom: 8px;
    }

  }

  .copyright {
    max-width: 1920px;
    margin: 0 auto;
    padding: 20px 300px;
    display: flex;
    justify-content: space-between;
    background: #53535563;
    .arrow-top {
      font-weight: 700;
      font-size: 14px;
      line-height: 150%;
      color: #FFFFFF;
      opacity: 0.6;
      background: #53535503;
      border: none;
    }
  }
</style>
