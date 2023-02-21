<template>
  <div
    class="w-full min-h-screen font-sans text-gray-900 bg-gradient-to-br from-transparent to-orange-100"
    :class="sidebarOpen ? 'overflow-hidden h-screen' : ''"
  >
    <nav
      class="flex items-center justify-between px-6 py-8 max-w-screen-xl mx-auto max-w-screen-xl md:px-12 lg:px-16 xl:px-24"
    >
      <a href="#" class="text-3xl md:text-4xl font-bold tracking-wide"
        ><span class="text-orange-600">O</span>zark</a
      >
      <div
        class="inset-0 transition-all bg-white/70 backdrop-blur-xl z-20 md:static md:bg-transparent md:flex items-center justify-center space-y-8 md:space-y-0 md:space-x-8 flex-col md:flex-row lg:space-x-14"
        :class="sidebarOpen ? 'fixed flex' : 'hidden'"
      >
        <ul
          class="flex flex-col md:flex-row items-center space-y-6 md:space-y-0 md:space-x-6 lg:md:-x-8"
        >
          <li
            class="text-lg md:text-base lg:text-lg font-medium group"
            :class="{ 'text-orange-500': activeMenu === menu }"
            v-for="menu in menus"
          >
            <a href="#">{{ menu }}</a>
            <div
              class="h-0.5 bg-orange-500 scale-x-0 group-hover:scale-100 transition-transform origin-left rounded-full duration-300 ease-out"
            ></div>
          </li>
        </ul>
        <button
          class="flex justify-center items-center h-13 px-7 font-medium text-white bg-orange-700 rounded-xl hover:shadow-primary transition-shadow duration-300 whitespace-nowrap"
        >
          Get Started
        </button>
      </div>
    </nav>
    <div
      class="flex gap-y-24 justify-between py-12 px-6 mx-auto max-w-screen-xl sm:px-8 md:px-12 lg:px-16 xl:px-24"
    >
      <div class="relative z-10 md:w-1/2 w-full">
        <img
          class="absolute top-0 right-0 md:-top-4 md:-right-8 w-24 h-auto"
          src="./assets/images/leaf.png"
          alt=""
        />
        <span class="flex items-center px-1 text-xl text-orange-700">
          <span class="font-medium">100% Authentic American food</span>
          <img class="w-auto h-8" src="./assets/images/vegetable.png" alt="" />
        </span>
        <h1 class="pt-4 text-6xl font-bold tracking-tighter leading-tight">
          Experience true flavor and original
          <span class="whitespace-nowrap text-orange-600">American food</span>
        </h1>
        <p class="pt-8 text-lg text-gray-600 leading-relaxed">
          Choose variety of South American food prepared by our expert chefs and
          enjoy the beatuful Baguio atmosphere
        </p>
        <div class="flex pt-8 space-x-6">
          <button
            class="flex justify-center items-center h-13 px-8 font-medium bg-orange-500 text-white rounded-xl hover:shadow-primary transition-shadow duration-300"
          >
            Get Started
          </button>
          <button
            class="flex justify-center items-center h-13 px-8 font-medium text-gray-900 border-gray-900 rounded-xl hover:shadow-xl transition-shadow duration-300"
          >
            Explore menu
          </button>
        </div>
        <div class="flex pt-20">
          <img class="w-24 h-auto" src="./assets/images/chef.png" alt="" />
          <div class="pt-5 pl-3">
            <div class="text-lg font-bold leading-relaxed">
              Chef of the month
            </div>
            <div class="inline-flex text-gray-600 leading-relaxed">
              People loved his cooking
            </div>
            <div class="font-bold text-orange-600 leading-relaxed">
              80+ famous dishes
            </div>
          </div>
        </div>
      </div>
      <div class="flex-1 flex flex-col relative">
        <img
          class="max-w-xl drop-shadow-2xl self-end"
          src="./assets/images/dish.png"
          alt=""
        />
        <div
          class="absolute -right-6 top-32 flex flex-col py-5 px-7 rounded-xl shadow-xl bg-white/80 backdrop-blur-xl hover:-translate-y-2 hover:shadow-2xl transition-all duration-300"
        >
          <div class="flex -space-x-3">
            <div
              v-for="i in 3"
              class="w-13 h-13 rounded-full border-4 border-white object-cover overflow-hidden"
            >
              <img :src="`src/assets/images/avatar-${i}.jpeg`" alt="" />
            </div>
          </div>
          <div class="pt-3 font-bold">Happy customers</div>
          <div class="flex items-center text-gray-600 leading-relaxed">
            <StarIcon class="w-5 h-5" />
            <span class="pl-1">4.9 (+2.5k Ratings)</span>
          </div>
        </div>
        <div
          class="absolute left-0 bottom-16 flex rounded-xl shadow-xl bg-white/80 backdrop-blur-xl hover:-translate-y-2 hover:shadow-2xl transition-all duration-300"
        >
          <img
            class="w-auto h-20 self-end"
            src="./assets/images/driver.png"
            alt=""
          />
          <div class="pr-7 pl-2 py-5">
            <div class="font-bold">Fast Delivery</div>
            <div class="to-gray-600 leading-relaxed">30 mins delivery</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import StarIcon from "./icons/star.vue";
const activeMenu = "Home";
const menus = ["Home", "Bed and Breakfast", "Events", "FAQs", "Contact Us"];
</script>
