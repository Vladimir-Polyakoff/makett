<script>
import FooterSubscribe from '@/components/FooterSubscribe'
import FooterContact from '@/components/FooterContact'

export default {
  name: 'TheFooter',

  components: {
    FooterSubscribe,
    FooterContact
  }
}
</script>

<template>
  <div>
    <FooterSubscribe></FooterSubscribe>
    <FooterContact></FooterContact>
  </div>
</template>
