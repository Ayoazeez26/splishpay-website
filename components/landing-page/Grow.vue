<script>
export default {
}
</script>

<template>
  <section class="container-gravy my-5">
    <div class="grow bg-$black rounded-lg py-20 text-center mx-auto w-full">
      <span class="text-$primary uppercase font-medium">grow with splish</span>
      <h1 class="grow__title text-white text-4xl md:text-6xl mx-auto mt-6">
        Do it the easy way
      </h1>
      <p class="grow__subtitle text-white text-xl md:text-2xl mt-6 mx-auto">
        With our complete business toolkit, maximize the efficiency of your business.
      </p>
      <div class="cards flex flex-wrap mx-auto mt-12 px-10 w-full">
        <div class="cards__card flex flex-col justify-between items-start red rounded p-10 my-3">
          <img src="@/assets/icons/Activity.svg" alt="activity icon">
          <div class="text-left">
            <p class="font-medium text-white uppercase">
              record a sale
            </p>
            <p class="text-white mt-6 text-2xl">
              During a sale, you can record a sale by cash, bank transfer, invoice or card. Giving your business detailed information on all your day to day activities.
            </p>
          </div>
        </div>
        <div class="cards__card flex flex-col justify-between items-start yelow rounded p-16 my-3">
          <img src="@/assets/icons/Star.svg" alt="activity icon" class="self-end -mr-14 -mt-14">
          <div class="text-left text-white">
            <p class="font-medium uppercase">
              Start, run and grow
            </p>
            <p class="mt-6 text-4xl">
              Create an account within minutes and enjoy access to future-focused tools for your business from point-of-sale to financial services
            </p>
            <p class="mt-6 text-lg">
              No hidden fees. Only pay when you take a payment
            </p>
          </div>
        </div>
        <img src="@/assets/images/blur.png" alt="blurred image" class="my-3">
        <div class="cards__card flex flex-col items-start rounded p-10 my-3">
          <div class="text-left text-white">
            <p class="font-medium uppercase">
              create items
            </p>
            <p class="mt-8 text-2xl">
              Create and manage items, so you can sell better and faster
            </p>
            <div class="mt-8 w-full">
              <div class="item flex justify-between items-center p-4">
                <div class="flex">
                  <div class="green w-8 h-8 rounded-full mr-2" />
                  <div class="text-xs">
                    <p>NIKE Sneakers</p>
                    <p class="small">
                      16 Items
                    </p>
                  </div>
                </div>
                <img src="@/assets/icons/arrow_right.svg" alt="right arrow">
              </div>
              <div class="item flex justify-between items-center p-4">
                <div class="flex">
                  <div class="blue w-8 h-8 rounded-full mr-2" />
                  <div class="text-xs">
                    <p>ASOS Apparels</p>
                    <p class="small">
                      32 Items
                    </p>
                  </div>
                </div>
                <img src="@/assets/icons/arrow_right.svg" alt="right arrow">
              </div>
              <div class="item flex justify-between items-center p-4">
                <div class="flex">
                  <div class="yellow w-8 h-8 rounded-full mr-2" />
                  <div class="text-xs">
                    <p>Smiley Socks</p>
                    <p class="small">
                      8 Items
                    </p>
                  </div>
                </div>
                <img src="@/assets/icons/arrow_right.svg" alt="right arrow">
              </div>
            </div>
          </div>
        </div>
        <div class="cards__card flex flex-col items-start rounded p-10 my-3">
          <div class="text-left text-white">
            <p class="font-medium uppercase">
              manage staff
            </p>
            <img src="@/assets/images/avatars.png" alt="avatars" class="mt-8">
            <div class="mt-4 flex w-full">
              <img src="@/assets/icons/list-style.svg" alt="list style" class="list ml-3">
              <div class="flex flex-col text-lg ml-3">
                <p class="create">
                  Create and manage people who help you run your business.
                </p>
                <p class="mt-3">
                  Easily customizable access for staff.
                </p>
                <p class="mt-3">
                  Keep track of team performance, Pay team with ease.
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="cards__card flex flex-col items-start rounded pt-12 px-10 my-3">
          <div class="text-left text-white">
            <p class="font-medium uppercase">
              customers
            </p>
            <p class="mt-8 text-2xl">
              Create and manage customers. You can have all your customer details from name to address. We also allow you to Import customers from excel with ease.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.grow {
  margin-left: -10px;
  margin-right: -10px;
  &__title {
    width: 100%;
    max-width: 509px;
  }
  &__subtitle {
    width: 100%;
    max-width: 503px;
  }
  .cards {
    &__card {
      &:nth-child(1) {
        width: 100%;
        max-width: 400px;
        height: 621px;
        background: rgba(227, 19, 82, 0.4);
        border: 1px solid #E31352;
        backdrop-filter: blur(92px);
      }
      &:nth-child(2) {
        margin-left: 24px;
        margin-right: 24px;
        width: 100%;
        max-width: 576px;
        height: 621px;
        background-image: url('@/assets/images/yellow_bg.png');
        background-position: cover;
      }
      &:nth-child(4) {
        width: 400px;
        height: 400px;
        background-color: $black-2;
        background-image: url('@/assets/icons/gem_1.svg');
        background-position: center;
        .item {
          &:nth-child(1) {
            background-color: rgba(0, 0, 0, 0.3);
            border-radius: 6px;
          }
          .small {
            font-size: 10px;
          }
          .green {
            background-color: #17E5A1;
          }
          .blue {
            background-color: #007AFF;
          }
          .yellow {
            background-color: #E0B002;
          }
        }
      }

      &:nth-child(5) {
        width: 448px;
        height: 400px;
        margin-left: 24px;
        margin-right: 24px;
        background-color: $black-2;
        .list {
          height: 180px;
        }
        .create {
          margin-top: 30px;
        }
      }

      &:nth-child(6) {
        width: 400px;
        height: 400px;
        background-color: $black-2;
        // background-image: url('@/assets/icons/gem_1.svg');
        // background-position: center;
        .item {
          &:nth-child(1) {
            background-color: rgba(0, 0, 0, 0.3);
            border-radius: 6px;
          }
          .small {
            font-size: 10px;
          }
          .green {
            background-color: #17E5A1;
          }
          .blue {
            background-color: #007AFF;
          }
          .yellow {
            background-color: #E0B002;
          }
        }
      }

    }
  }
}
</style>
