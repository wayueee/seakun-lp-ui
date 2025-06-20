<template>
  <div class="relative bg-white md:py-20  md:px-16">
    <div class="">
      <img
      class="absolute hidden md:block w-[90%] right-[11.2%] top-0 z-0"
      src="/images/benefit/shape.png"
      alt="bg-shape"
      />
    </div>
    <div class="relative">
  <img class="md:hidden absolute left-0 top-[-24px] " src="/images/benefit/background-mobile.png" alt="bg">
    <img
      class="hidden md:block absolute w-[80%] top-28 right-[8%] z-0"
      src="/images/benefit/map.png"
      alt="map"
    />
</div>

    <div class="relative z-10 text-center">
      <h1 class="text-xl md:text-[28px] text-[22px] font-bold leading-tight">
        Beragam Manfaat
        <br />
        <span class="block">Yang Bisa Kamu Dapatkan</span>
      </h1>
    </div>

    <div class="relative z-10 max-md:grid max-md:grid-cols-2 max-md:pl-6 pr-4 md:flex md:flex-wrap md:justify-center mt-8 md:mt-14 gap-x-16 gap-y-8 md:max-w-4xl md:ml-[22%]">
      <div
        v-for="(item, index) in benefit"
        :key="index"
        class="flex items-center lg:w-[300px] space-x-2"
      >
        <img :src="item.images" alt="icon" class="md:w-[17%] w-[22%]" />
        <p class="text-[#2D2D2D] text-xs md:text-sm md:w-36 font-semibold">{{ item.title }}</p>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      benefit: [
        {
          title: "Hemat Hingga 70%",
          images: "/images/benefit/hemat.png",
        },
        {
          title: "Privasi Terjamin",
          images: "/images/benefit/privasi.png",
        },
        {
          title: "Customer Service Responsif",
          images: "/images/benefit/customer.png",
        },
        {
            title: "Beragam Metode Pembayaran",
            images: "/images/benefit/pembayaran.png",
        },
        {
          title: "Layanan Legal dan Resmi",
          images: "/images/benefit/layanan.png",
        },
        {
          title: "Pengingat Pembayaran",
          images: "/images/benefit/pengingat.png",
        },
      ],
    };
  },
};
</script>

<style></style>
