<template>
  <div>
    <h1 class="text-xl md:text-3xl font-semibold mb-8">Berlangganan Produk Digital</h1>
    <div class="mb-[2%] flex max-md:flex-col relative">
      <div
        class="absolute md:inset-y-0 max-md:top-5 left-0 pl-3 flex items-center pointer-events-none"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-4 w-4 text-gray-400"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M21 21l-4.35-4.35m0 0A7.5 7.5 0 1110.5 3a7.5 7.5 0 016.15 13.65z"
          />
        </svg>
      </div>
        <input
          type="text"
          class="md:pr-[14%] text-sm md:mr-[24%] pl-10 py-4 border border-black rounded-lg"
          placeholder="Cari Product"
        />
        <div class=" max-md:mt-3 flex max-md:justify-between gap-2">
          <select
            class="pl-[1%] max-md:text-sm max-md:pr-[20%] text-black/40 pr-[40%] mr-[1%] border-black justify-between border rounded-lg py-4"
          >
            <option value="" hidden>Tipe product</option>
            <option value="">All</option>
            <option value="">Ready</option>
            <option value="">Pre-order</option>
          </select>
          <select class="pl-[1%] max-md:text-sm pr-[32%] text-black/40 max-md:pr-[12%] border rounded-lg border-black py-4">
            <option value="" hidden>Kategori product</option>
            <option value="">All</option>
            <option value="">Ready</option>
            <option value="">Pre-order</option>
          </select>
        </div>
    </div>
    <div class="grid grid-cols-2 xs:grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 md:gap-4 gap-3 mb-10 lg:pr-[7%] relative">
        <CardProduct v-for="item in products" :key="item"
        :card="item" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        {
          name: "Youtube",
          type: [
            {
              user: "User Reguler",
              price: "Rp 36.900",
              duration: "bulan",
              choiceDuration: "1, 3, 6, 12 Bulan",
            },
          ],
          images: "/images/card/Background.png",
          imagesCard: "/images/card/youtube.png",
        },
        {
          name: "Spotify",
          type: [
            {
              user: "User Reguler",
              price: "Rp 36.900",
              duration: "2 bulan",
              choiceDuration: "2, 3, 6, 12 Bulan",
            },
            {
              user: "User Host ",
              price: "Rp 28.967",
              duration: "bulan",
              choiceDuration: "1 Bulan",
            },
          ],
          images: "/images/card/Background.png",
          imagesCard: "/images/card/spotify.png",
        },
        {
          name: "Gramedia Digital",
          type: [
            {
              user: "Non Fiksi",
              price: "Rp 29.500",
              duration: "bulan",
              choiceDuration: "1, 3 Bulan",
            },
            {
              user: "Fiksi",
              price: "Rp 29.500",
              duration: "bulan",
              choiceDuration: "1, 3 Bulan",
            },
            {
              user: "Full Premium",
              price: "Rp 54.500",
              duration: "bulan",
              choiceDuration: "1, 3 Bulan",
            },
          ],
          images: "/images/card/Background.png",
          imagesCard: "/images/card/gramedia-digital.png",
        },
        {
          name: "Netflix",
          type: [
            {
              user: "User Reguler Tv",
              price: "Rp 61.000",
              duration: "bulan",
              choiceDuration: "2, 3 Bulan",
            },
            {
              user: "User Host Tv",
              price: "Rp 57.500",
              duration: "bulan",
              choiceDuration: "1 Bulan",
            },
            {
              user: "User Reguler Non Tv",
              price: "Rp 54.000",
              duration: "bulan",
              choiceDuration: "2, 3, 6 Bulan",
            },
            {
              user: "User Host Non Tv",
              price: "Rp 47.500",
              duration: "bulan",
              choiceDuration: "1 Bulan",
            },
          ],
          images: "/images/card/Background.png",
          imagesCard: "/images/card/netflix.png",
        },
        {
          name: "Apple Music",
          type: [
            {
              user: "User Host",
              price: "Rp 17.000",
              duration: "bulan",
              choiceDuration: "1, 3, 6 Bulan",
            },
            {
              user: "User Reguler",
              price: "Rp 22.000",
              duration: "bulan",
              choiceDuration: "1, 3, 6 Bulan",
            },
          ],
          images: "/images/card/Background.png",
          imagesCard: "/images/card/apple-music.png",
        },
        {
          name: "Apple One",
          type: [
            {
              user: "User Reguler",
              price: "Rp 36.900",
              duration: "bulan",
              choiceDuration: "1, 3, 6, 12 Bulan",
            },
          ],
          images: "/images/card/Background.png",
          imagesCard: "/images/card/apple-one.png",
        },
        {
          name: "Apple One Premier",
          type: [
            {
              user: "User Reguler",
              price: "Rp 36.900",
              duration: "bulan",
              choiceDuration: "1, 3, 6, 12 Bulan",
            },
          ],
          images: "/images/card/Background.png",
          imagesCard: "/images/card/apple-premier.png",
        },
        {
          name: "Apple TV+",
          type: [
            {
              user: "User Reguler",
              price: "Rp 36.900",
              duration: "bulan",
              choiceDuration: "1, 3, 6, 12 Bulan",
            },
          ],
          images: "/images/card/Background.png",
          imagesCard: "/images/card/apple-tv.png",
        },
      ],
    };
  },
};
</script>

<style></style>
