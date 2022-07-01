<script>
export default {
}
</script>

<template>
  <footer class="container-gravy my-5">
    <div class="footer relative bg-$black rounded-lg px-10 py-7 md:px-20 md:py-14">
      <div class="w-full flex justify-between items-end">
        <img src="@/assets/images/sp.png" alt="footer logo" class="w-20 sm:w-auto">
        <div class="buttons flex flex-col sm:flex-row items-center">
          <p class="footer__subtitle text-white mb-4 sm:mb-0 sm:mr-7 text-xl md:text-3xl">
            Ready for takeoff ?
          </p>
          <a data-type="button" class="btn bg-$primary rounded text-white px-5 text-lg py-4 btn-primary min-w-max" href="#">
            Download The App
          </a>
        </div>
      </div>
      <div class="line w-full h-px bg-$black-2 my-10" />
      <div class="w-full flex justify-between items-center">
        <ul
          class="navbar-links flex flex-col md:flex-row md:text-center text-white"
        >
          <li class="navbar-links__item md:mr-5">
            <NuxtLink to="/#hero">
              Card Reader
            </NuxtLink>
          </li>
          <li class="navbar-links__item md:mx-5 mt-3 md:mt-0">
            <NuxtLink to="/#partners">
              Merchants
            </NuxtLink>
          </li>
          <li class="navbar-links__item md:mx-5 mt-3 md:mt-0">
            <NuxtLink to="/about">
              About
            </NuxtLink>
          </li>
          <li class="navbar-links__item md:mx-5 mt-3 md:mt-0">
            <NuxtLink to="/#cta">
              Contact
            </NuxtLink>
          </li>
        </ul>
        <div class="socials flex flex-col sm:flex-row">
          <a href="https://www.instagram.com/splishpay/" target="_blank" class="item w-10 h-10 rounded-sm bg-white flex items-center justify-center sm:ml-2 mb-3 sm:mb-0">
            <img src="@/assets/icons/Instagram.svg" alt="Instagram Icon" class="">
          </a>
          <a href="https://twitter.com/splishpay/" target="_blank" class="item w-10 h-10 rounded-sm bg-white flex items-center justify-center sm:ml-2 mb-3 sm:mb-0">
            <img src="@/assets/icons/Twitter.svg" alt="Twitter Icon" class="">
          </a>
          <a href="https://www.facebook.com/splishpay/" target="_blank" class="item w-10 h-10 rounded-sm bg-white flex items-center justify-center sm:ml-2 mb-3 sm:mb-0">
            <img src="@/assets/icons/Facebook.svg" alt="Facebook Icon" class="">
          </a>
          <a href="https://www.linkedin.com/company/splishpay/" target="_blank" class="item w-10 h-10 rounded-sm bg-white flex items-center justify-center sm:ml-2">
            <img src="@/assets/icons/LinkedIn.svg" alt="LinkedIn Icon" class="">
          </a>
        </div>
      </div>
      <div class="line w-full h-px bg-$black-2 my-10" />
      <p class="text-xs copy">SplishPay © 2022 All Rights Reserved | Privacy Policy</p>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  margin-left: -10px;
  margin-right: -10px;
  img {
  }
  .copy {
    color: rgba(#FFF, 0.56);
  }
}
</style>
