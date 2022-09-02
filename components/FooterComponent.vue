<template>
  <div
    class="
      h-10
      md:h-44
      py-4
      px-2
      bg-gray-800
      text-white
      flex
      justify-between
      mt-5
    "
  >
    <div class="ml-4 px-2 flex flex-col justify-evenly text-md md:text-lg">
      <p>Om oss</p>
      <p>Kontakta oss</p>
      <p>Våran databas</p>
      <p>Ännu en länk</p>
    </div>
    <div class="flex flex-row mx-2 items-center">
      <nuxt-link to="/cart" class="w-8 mx-4 filter invert cursor-pointer">
        <img src="~static/shopping-cart-icon-png-transparent-28.jpg" alt="" />
      </nuxt-link>
      <img
        src="~static/profile-png-icon-1.jpg"
        class="w-8 mx-4 filter invert"
      />
    </div>
  </div>
</template>