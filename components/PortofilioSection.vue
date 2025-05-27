<template>
  <div class="flex mt-[10%]">
    <div class="flex gap-2">
      <div class="pr-2 pb-10 w-[185px]" v-for="port in portofolio" :key="port">
        <div
          :class="`${port.bg} px-6 pb-8 rounded-b-2xl rounded-tr-[70px]  rounded-tl-[70px] relative text-white text-center`"
        >
          <img
            class="absolute -top-14 left-1/2 -translate-x-1/2 w-[100px]"
            :src="port.images"
            alt="images"
          />
          <div class="pt-8">
            <h1 class="text-[28px] font-bold">{{ port.rate }}</h1>
            <p class="text-base mt-1">{{ port.title }}</p>
          </div>
        </div>
    </div>
  </div>
  <div class="flex flex-col pl-12 relative ">
    <h1 class="text-[26px] font-bold pr-2 z-10">Jadilah bagian dari Seakun</h1>
    <p class="text-black/30 z-10 text-[15px] pr-[120px]">
      Dapatkan manfaat Patungan Berlangganan. Nikmati layanan premium dengan
      lebih hemat, aman dan legal
    </p>
    <img class="absolute right-1 w-[43%] bottom-0" src="/images/portofolio/green-bg.png" alt="bg">
  </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      portofolio: [
        {
          title: "Pengguna",
          images: "/images/portofolio/pengguna.png",
          rate: "94.500+",
          bg: "bg-[#34BB9E]",
        },
        {
          title: "Transaksi",
          images: "/images/portofolio/Transaksi.png",
          rate: "553.000+",
          bg: "bg-[#FF5968]",
        },
        {
          title: "Layanan",
          images: "/images/portofolio/Layanan.png",
          rate: "45",
          bg: "bg-[#38ADEF]",
        },
        {
          title: "Tingkat Kepuasan",
          images: "/images/portofolio/Tingkat-Kepuasan.png",
          rate: "9/10",
          bg: "bg-[#FABF18]",
        },
      ],
    };
  },
};
</script>

<style></style>
