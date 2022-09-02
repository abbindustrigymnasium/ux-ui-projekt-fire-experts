<template>
  <div
    class="
      h-10
      md:h-28
      py-4
      px-2
      bg-gray-800
      text-white
      flex
      justify-between
      items-center
      mb-5
    "
  >
    <nuxt-link to="/" class="flex flex-row mx-2 items-center">
      <p class="text-lg md:text-2xl flex mr-4">Fire Experts</p>
      <img src="~static/flame icon.png" class="w-6" />
    </nuxt-link>
    <div class="flex flex-row mx-2 items-center">
      <nuxt-link to="/cart" class="w-8 mx-4 filter invert cursor-pointer">
        <img src="~static/shopping-cart-icon-png-transparent-28.jpg" alt="" />
      </nuxt-link>
      <nuxt-link to="/profile">
      <img
        src="~static/profile-png-icon-1.jpg"
        class="w-8 mx-4 filter invert"
      />
    </nuxt-link>
    </div>
  </div>
</template>