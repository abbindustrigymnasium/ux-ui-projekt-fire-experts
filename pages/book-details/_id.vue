<template>
  <div class="bg-gray-800 bg-opacity-50 rounded-3xl p-5 md:p-10 h-auto w-full">
    <div class="flex flex-col md:flex-row">
      <img :src="currentBook.img" class="w-full md:w-1/4 h-full rounded-3xl" />
      <div class="flex flex-wrap flex-col md:w-2/3 ml-2 p-4">
        <p class="text-2xl xl:text-4xl font-bold">
          {{ currentBook.title }}
        </p>
        <p class="text-2xl">Av {{ currentBook.author }}</p>
        <p class="text-md italic">Genrer: {{ currentBook.genre.join(", ") }}</p>
        <div class="text-lg mt-2 pr-5">
          <p>
            {{ currentBook.title }} är en bok om just
            {{ currentBook.title }} bla bla bla bla
          </p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris
            maximus felis eget metus volutpat, quis ullamcorper diam commodo.
            Pellentesque id tellus dapibus, laoreet dui ut, bibendum est. Duis
            eget sodales est. Phasellus vestibulum dolor tristique massa
            imperdiet blandit. Morbi sit amet euismod neque, vitae aliquam
            mauris. Sed porta finibus justo sed lobortis. Duis dolor risus,
            rutrum vitae enim quis, bibendum porttitor elit. Etiam congue
            tincidunt elementum. Etiam vestibulum aliquam blandit. Quisque nec
            pellentesque velit. Proin tristique velit vitae metus mollis, quis
            venenatis arcu ultrices.
          </p>
        </div>
      </div>
    </div>
    <div class="w-full flex flex-row flex items-center">
      <p class="mr-5 text-lg">Pris: 150kr</p>
      <div
        class="
          px-5
          py-4
          mr-5
          mt-2
          bg-gray-800
          w-36
          rounded-xl
          flex
          justify-center
          align-center
          cursor-pointer
          transform
          transition
          duration-500
          ease-in-out
          hover:scale-110
        "
      >
        <p>Köp</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted () {
    console.log(this.$route.params.id)
  },
  data () {
    return {
      bookId: this.$route.params.id,
      currentBook: [],
    }
  },
  async fetch () {
    this.currentBook = await fetch(
      'http://localhost:5000/books/' + this.$route.params.id
    ).then(res => res.json())
  }
}
</script>