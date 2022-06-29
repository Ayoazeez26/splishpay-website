<script>
export default {
}
</script>

<template>
  <section class="container-gravy mb-5">
    <div id="hero" class="header relative bg-$black rounded-lg pt-12 md:pt-44 pl-2 md:pl-28 pb-12 md:pb-40">
      <h1 class="header__title text-white text-4xl md:text-6xl lg:text-8xl">
        Business like never before
      </h1>
      <p class="header__subtitle text-white text-xl md:text-2xl mt-6">
        The goals for Splish are to design and build easy-to-use and affordable products that help organize all of Africa's business information.
      </p>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.header {
  margin-top: 151px;
  margin-left: -10px;
  margin-right: -10px;
  background-image: url("@/assets/images/about-hero.png");
  background-position: left;
  background-size: cover;
  background-repeat: no-repeat;
  &__title {
    width: 100%;
    max-width: 628px;
  }
  &__subtitle {
    width: 100%;
    max-width: 644px;
  }
  img {
    @media screen and (min-width: 768px) and (max-width: 1280px) {
      display: none;
    }
  }
  @media screen and (max-width: 640px) {
    margin-top: 80px;
  }
}
</style>
