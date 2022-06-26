<script>
import HeroSection from '~/components/landing-page/Hero.vue'
import PartnerSection from '~/components/landing-page/Partners.vue'
export default {
  name: 'IndexPage',
  components: {
    HeroSection,
    PartnerSection
  }
}
</script>
<template>
  <div>
    <HeroSection />
    <PartnerSection />
  </div>
</template>
