<script>
export default {
  name: 'AppNavbar',
  data: () => ({
    open: false,
    showModal: false,
    scrolled: false
  }),
  created () {
    // eslint-disable-next-line nuxt/no-globals-in-created
    if (typeof window !== 'undefined') {
      // here `window` is available
      // eslint-disable-next-line nuxt/no-globals-in-created
      window.addEventListener('scroll', this.handleScroll)
    }
  },
  destroyed () {
    // eslint-disable-next-line nuxt/no-globals-in-created
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll () {
      this.scrolled = window.scrollY > 0
    },
    goToBook () {
      this.$router.push('http://calendly.com/schooldose')
    }
  }
}
</script>
<template>
  <nav class="app-nav" :class="scrolled ? 'navbar-scroll' : ''">
    <ComingSoon :show-modal="showModal" @hide="showModal = false" />
    <div class="navbar">
      <div class="navbar-left">
        <NuxtLink to="/" class="navbar__logo">
          <img src="@/assets/images/splish.png" alt="Splish logo">
        </NuxtLink>
        <button class="navbar__toggle d-lg-none" @click="open = !open">
          <span class="sr-only">Toggle Navbar</span>
          <div />
          <div />
          <div />
        </button>
        <ul
          class="navbar-links pl-0 pl-sm-5 my-0 nunito"
          :class="{ 'navbar-links--open': open }"
        >
          <button class="navbar-links__toggle d-lg-none" @click="open = !open">
            <span class="sr-only">Toggle Navbar</span>
            <img src="@/assets/icons/close.svg" alt="close icon">
          </button>
          <li class="navbar-links__item">
            <NuxtLink to="/">
              Features
            </NuxtLink>
          </li>
          <li class="navbar-links__item">
            <NuxtLink to="/#valets">
              About
            </NuxtLink>
          </li>
          <li class="navbar-links__item">
            <NuxtLink to="/blog">
              Blog
            </NuxtLink>
          </li>
          <li class="navbar-links__item">
            <NuxtLink to="/#valets">
              FAQ
            </NuxtLink>
          </li>
          <li class="navbar-links__item d-lg-none">
            <a data-type="button" class="btn btn-outline-primary" href="https://calendly.com/schooldose/30min" target="_blank" rel="noreferrer">
              Book Demo
            </a>
          </li>
          <li class="navbar-links__item d-lg-none">
            <a data-type="button" class="btn btn-outline-primary" href="https://skoolapp-demo.netlify.app/auth/login">
              Login
            </a>
          </li>
          <li class="navbar-links__item d-lg-none">
            <a data-type="button" class="btn btn-primary" href="https://skoolapp-demo.netlify.app/auth/signup">
              Create Account
            </a>
          </li>
        </ul>
      </div>
      <ul class="navbar-links d-none d-lg-flex mb-0">
        <li class="navbar-links__item">
          <a data-type="button" class="btn btn-outline-primary" href="https://calendly.com/schooldose/30min" target="_blank" rel="noreferrer">
            Book Demo
          </a>
        </li>
        <li class="navbar-links__item">
          <a data-type="button" class="btn btn-outline-primary" href="https://skoolapp-demo.netlify.app/auth/login">
            Login
          </a>
        </li>
        <li class="navbar-links__item">
          <a data-type="button" class="btn btn-primary" href="https://skoolapp-demo.netlify.app/auth/signup">
            Create Account
          </a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
.app-nav {
  position: fixed;
  top: 0;
  width: 100%;
  border-bottom: 1px solid #E3E8EF;
  z-index: 10;
}
.navbar {
  padding: 30px 10px;
  width: 1400px;
  max-width: 100%;
  margin: 0 auto;

  &__logo {
    img {
      max-width: 200px;
    }
  }

  &-left {
    display: flex;
    @media screen and (max-width: 768px) {
      width: 100%;
      justify-content: space-between;
    }
  }

  &-links {
    display: flex;
    align-items: center;
    list-style-type: none;

    &__item {
      margin: 0 10px;
      a:not([data-type=button]) {
        color: #0B2348;
        text-decoration: none;
        &:hover {
          opacity: 0.9;
          color: #0B2348;
        }
      }

      button:not([data-type=button]) {
        color: $black;
        font-weight: 700;
        border-radius: 8px;
        min-height: 50px;
        min-width: 170px;
      }
    }

    @media screen and (max-width: 991px) {
      transform: translateX(500px);
      pointer-events: none;
      position: fixed;
      transition: transform .2s ease-out;
      display: flex;
      flex-direction: column;
      padding-top: 150px;
      padding-left: 30px !important;
      padding-right: 30px;
      top: 0;
      bottom: 0;
      right: 0;
      width: 500px;
      max-width: 100vw;
      background-color: #FFF;
      z-index: 100;
      &__toggle {
        display: none;
      }
      &--open {
        transform: translateX(0);
        pointer-events: all;

        .navbar-links__toggle {
          display: block;
          position: fixed;
          top: 30px;
          right: 10px;
          background: none;
          border: none;
        }

        .navbar-links__item {
          text-align: left;
          margin: 20px 0;
          width: 100%;

          .btn {
            width: 100%;
          }
        }
      }
    }
  }

  &__toggle {
    background: none;
    border: none;

    div {
      background-color: $primary;
      height: 3px;
      border-radius: 2px;
      margin: 4px;
      &:nth-child(2) {
        width: 20px;
      }

      &:nth-child(3) {
        width: 15px;
      }

      &:last-child {
        width: 9px;
      }
    }
  }
  &-scroll {
    box-shadow: 1px 2px 18px rgba(0, 0, 0, 0.1);
    background-color: white !important;
  }
}
</style>
