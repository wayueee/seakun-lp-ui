<template>
  <div class="relative bg-white py-20 px-4 md:px-16">
<div>
    <img
      class="absolute w-[90%] right-[11.2%] top-0 z-0"
      src="/images/benefit/shape.png"
      alt="bg-shape"
    />
</div>
<div class="relative">
    <img
      class="absolute w-[80%] top-28 right-[8%] z-0"
      src="/images/benefit/map.png"
      alt="map"
    />
</div>

    <div class="relative z-10 text-center  ">
      <h1 class="text-xl md:text-[28px] font-bold leading-tight">
        Beragam Manfaat
        <br />
        <span class="block">Yang Bisa Kamu Dapatkan</span>
      </h1>
    </div>

    <div class="relative z-10 flex flex-wrap justify-center mt-14 gap-x-16 gap-y-8 max-w-4xl ml-[22%]">
      <div
        v-for="(item, index) in benefit"
        :key="index"
        class="flex items-center w-[300px] space-x-2"
      >
        <img :src="item.images" alt="icon" class="w-[17%] " />
        <p class="text-[#2D2D2D] text-sm w-36 font-medium">{{ item.title }}</p>
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
