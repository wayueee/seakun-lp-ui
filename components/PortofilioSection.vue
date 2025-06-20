1<template>
  <div class="md:flex mt-[10%] flex-col md:flex-row relative">
    <div class=" flex flex-col md:pl-12 relative order-1 md:order-2 ">
      <h1 class=" text-[23px] md:text-[26px] max-md:text-center font-bold pr-2 mt-8 z-10">Jadilah bagian dari Seakun</h1>
      <h1 class="text-black/30 z-10 mb-20 text-[14px] max-md:text-center md:text-[15px] max-md:w-[300px] max-md:ml-14 mt-1 lg:w-[389px] ">
        Dapatkan manfaat Patungan Berlangganan. Nikmati layanan premium dengan
        lebih hemat, aman dan legal
      </h1>
      <img
        class="hidden md:block absolute left-[314px] w-[56%] bottom-0"
        src="/images/portofolio/green-bg.png"
        alt="bg"
      />
    </div>
    <img class="md:hidden w-[106px] sm:w-[126px] h-[510px] absolute top-[52px] left-[267px]" src="/images/portofolio/shape-mobile.png" alt="bg">
    <div class="max-md:grid max-md:grid-cols-2 ml-2 md:flex gap-2 order-2 md:order-1">
      <div
        class="pr-2 pb-12 w-[185px]"
        v-for="port in portofolio"
        :key="port"
      >
        <div
          :class="`${port.bg} px-6 pb-8 rounded-b-2xl rounded-tr-[70px] rounded-tl-[70px] relative text-white text-center`"
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
