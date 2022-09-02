<template>
  <div class="
      h-10
      md:h-44
      py-4
      px-2
      bg-gray-800
      text-white
      flex
      justify-between
      mt-5
    ">
    <div class="ml-4 px-2 flex flex-col justify-evenly text-md md:text-lg">
      <p class="hover:underline cursor-pointer">Om oss</p>
      <p class="hover:underline cursor-pointer">Kontakta oss</p>
      <p class="hover:underline cursor-pointer">Våran databas</p>
      <p class="hover:underline cursor-pointer">Ännu en länk</p>
    </div>
    <div class="flex flex-col items-center">

      <div>
        <img src="~static/flame icon.png" class="w-20 items-center" />
      </div>
      <div>
        back to top
      </div>
      <div class="h-max flex align-center">
        <img src="~static/flame icon.png" class="w-20 self-center" />

      </div>
      <div class="flex flex-row mx-2 items-center">
        <a href="https://mobile.twitter.com/abbgymnasiet">
          <img src="~static/twitter logo.png" class="
            w-10
            mx-4
            transform
            transition
            duration-200
            ease-in-out
            hover:scale-110
          " />
        </a>
        <a href="https://sv-se.facebook.com/abbgymnasiet">
          <img src="~static/facebook logo.png" alt="" class="
            w-12
            mx-4
            filter
            invert
            transform
            transition
            duration-200
            ease-in-out
            hover:scale-110
          " /></a>
      </div>
    </div>
</template>