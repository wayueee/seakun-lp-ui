<template>
    <div>
    <h1 class="text-3xl font-medium mb-8">Berlangganan Produk Digital</h1>
    <div class="mb-[2%] flex relative">
      <div
        class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none"
      >
        <!-- Ikon Search (pakai Heroicons, Lucide, atau SVG langsung) -->
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
        class="pr-[10%] mr-[29%] pl-10 py-4 border rounded-lg"
        placeholder="Cari Product"
      />
      <select class="pl-[1%] pr-[5%] mr-[1%] justify-between border rounded-lg py-4">
        <option value="" hidden>Tipe product</option>
        <option value="">All</option>
        <option value="">Ready</option>
        <option value="">Pre-order</option>
      </select>
      <select class="pl-[1%] pr-[4%] border rounded-lg py-4">
        <option value="" hidden>Kategori product</option>
        <option value="">All</option>
        <option value="">Ready</option>
        <option value="">Pre-order</option>
      </select>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 mb-10 pr-[9%] relative">
      <div
        v-for="(item, index) in products"
        :key="index"
        class="bg-white shadow-md rounded-2xl flex flex-col px-5"
      >
         <div class="mx-auto my-3">
             <img :src="item.images" alt="icon" class="w-14 h-10 mb-3 " />
         </div>
        <div class="flex">
            <img :src="item.imagesCard" alt="icon" class="mr-5 w-12 h-auto mb-3" />    
            <h2 class="py-3 text-sm font-semibold mb-1">{{ item.name }}</h2>
        </div>
        <hr :class="item.name === 'Youtube' ? 'my-5' : 'my-2'">

        <div class="mb-[60%]">
            <div v-for="user in item.type" :key="user" class="mb-2">
                <p class="text-[13px] text-gray-500 ">{{ user.user }}</p>
                <p class="text-[14px] font-semibold mb-1">{{ user.price }}<span class="text-sm font-normal"> /{{ user.duration }}</span></p>
            </div>
        </div>
        <div class="absolute bottom-[18%]">
            <button class="text-[#08A081] hover:text-green-700 text-sm font-thin">Lihat Skema harga</button>
        </div>
        <div class="absolute bottom-0">
            <button class="mt-4 bg-[#08A081] hover:bg-green-700 text-white pl-[240%] pr-[220%] mb-3 py-4 rounded-lg text-sm">Pesan</button>
        </div>
      </div>
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
          type: [{
            user : "User Reguler",
            price: "Rp 36.900",
            duration: "bulan",
          }],
          images : "/images/card/Background.png",
          imagesCard : "/images/card/youtube.png",
        },
        {
          name: "Spotify",
          type: [
            {
            user : "User Reguler",
            price: "Rp 36.900",
            duration: "2 bulan",
          },
            {
            user : "User Host ",
            price: "Rp 28.967",
            duration: "bulan",
          },
        ],
          images : "/images/card/Background.png",
          imagesCard : "/images/card/spotify.png",
        },
        {
          name: "Gramedia Digital",
          type: [
            {
            user : "Non Fiksi",
            price: "Rp 29.500",
            duration: "bulan",
          },
            {
            user : "Fiksi",
            price: "Rp 29.500",
            duration: "bulan",
          },
            {
            user : "Full Premium",
            price: "Rp 54.500",
            duration: "bulan",
          },
        ],
          images : "/images/card/Background.png",
          imagesCard : "/images/card/spotify.png",
        },
        {
          name: "Netflix",
          type: [
            {
            user : "User Reguler Tv",
            price: "Rp 61.000",
            duration: "bulan",
          },
            {
            user : "User Host Tv",
            price: "Rp 57.500",
            duration: "bulan",
          },
            {
            user : "User Reguler Non Tv",
            price: "Rp 54.000",
            duration: "bulan",
          },
            {
            user : "User Host Non Tv",
            price: "Rp 47.500",
            duration: "bulan",
          },
            
        ],
          images : "/images/card/Background.png",
          imagesCard : "/images/card/spotify.png",
        },
      ],
    };
  },
};
</script>

<style></style>
