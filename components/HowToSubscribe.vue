<template>
  <div
    class="w-full h-auto pl-[12%] py-[6%] pr-[12%] text-center bg-[#F6B93B] relative"
  >
    <img
      src="/images/subscribe/right-shape.png"
      alt="right-shape"
      class="absolute w-[270px] h-[576px] left-[1095px] top-0"
    />
    <h1 class="text-[30px] font-semibold text-white">Cara Berlangganan</h1>
    <p class="pt-1 text-[17px] leading-7 font-light text-white">
      Berikut ini cara berlangganan layanan premium di Seakun.id
    </p>
    <img
      src="/images/subscribe/balon.svg"
      alt=""
      class="absolute w-[105px] h-[115px] top-[83px]"
    />
    <div class="grid grid-cols-5 mt-[8%] justify-items-center relative">
      <div
        v-for="item in subscribe"
        :key="item.number"
        class="bg-white rounded-full flex flex-col items-center mb-10 mt-2 shadow-md"
      >
        <img
          src="/images/subscribe/background.png"
          alt="bg"
          class="w-[198px] h-[135px]"
        />
        <img
          :src="item.images"
          :alt="item.name"
          class="w-[120px] h-auto mb-4 absolute bottom-[50%]"
        />
        <p class="text-sm text-[#17A398] font-semibold absolute top-[50%]">
          {{ item.number }} <span class="text-[#17A398]">{{ item.name }}</span>
        </p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      subscribe: [
        {
          number: "1",
          name: "Pesan Layanan",
          images: "/images/subscribe/pesan.png",
        },
        {
          number: "2",
          name: "Pembayaran",
          images: "/images/subscribe/pembayaran.png",
        },
        {
          number: "3",
          name: "Menunggu Pembayaran",
          images: "/images/subscribe/menunggu.png",
        },
        {
          number: "4",
          name: "Pesanan Diterima",
          images: "/images/subscribe/pesanan.png",
        },
        {
          number: "5",
          name: "Selesai",
          images: "/images/subscribe/selesai.png",
        },
      ],
    };
  },
};
</script>

<style></style>
