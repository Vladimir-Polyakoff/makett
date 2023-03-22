<script>
import Menu from '@/components/Menu'
import HeaderContant from '@/components/HeaderContant'
import HeaderFooter from '@/components/HeaderFooter'

export default {
  name: 'TheHeader',

  components: {
    Menu,
    HeaderContant,
    HeaderFooter
  }
}
</script>

<template>
  <div>
    <Menu></Menu>
    <HeaderContant></HeaderContant>
    <HeaderFooter></HeaderFooter>
  </div>
</template>
