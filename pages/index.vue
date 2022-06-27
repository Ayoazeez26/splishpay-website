<script>
import HeroSection from '~/components/landing-page/Hero.vue'
import PartnerSection from '~/components/landing-page/Partners.vue'
import GrowthSection from '~/components/landing-page/Grow.vue'
export default {
  name: 'IndexPage',
  components: {
    HeroSection,
    PartnerSection,
    GrowthSection
  }
}
</script>
<template>
  <div>
    <HeroSection />
    <PartnerSection />
    <GrowthSection />
  </div>
</template>
