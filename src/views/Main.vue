<script>
import MainCreatex from '@/components/MainCreatex'
import MainFeatured from '@/components/MainFeatured'
import MainBenefits from '@/components/MainBenefits'
import MainWorkshop from '@/components/MainWorkshop'
import MainCertificate from '@/components/MainCertificate'
import MainTeam from '@/components/MainTeam'
import MainPosts from '@/components/MainPosts'

export default {
  name: 'TheMain',

  components: {
    MainCreatex,
    MainFeatured,
    MainBenefits,
    MainWorkshop,
    MainCertificate,
    MainTeam,
    MainPosts
  }
}
</script>

<template>
  <div>
    <MainCreatex></MainCreatex>
    <MainFeatured></MainFeatured>
    <MainBenefits></MainBenefits>
    <MainWorkshop></MainWorkshop>
    <MainCertificate></MainCertificate>
    <MainTeam></MainTeam>
    <MainPosts></MainPosts>
  </div>
</template>
