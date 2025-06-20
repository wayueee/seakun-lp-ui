<template>
  <div
    class="w-full h-auto px-[6%] lg:pl-[12%] py-[6%] lg:pr-[12%] text-center bg-[#F6B93B] relative"
  >
    <img
      src="/images/subscribe/right-shape.png"
      alt="right-shape"
      class="absolute hidden md:block md:w-[270px] md:h-[576px] left-[1095px] top-0"
    />
    <h1 class="text-[20px] md:text-[30px] font-semibold text-white">
      Cara Berlangganan
    </h1>
    <p
      class="pt-1 text-[14px] md:text-[17px] leading-7 font-light max-md:mb-20 text-white"
    >
      Berikut ini cara berlangganan layanan premium di Seakun.id
    </p>
    <img
      src="/images/subscribe/balon.svg"
      alt=""
      class="absolute hidden md:block w-[105px] h-[115px] top-[83px]"
    />
    <div
      class="grid grid-cols-2 md:grid-cols-5 md:mt-[8%] justify-center justify-items-center relative"
    >
      <div
        v-for="item in subscribe"
        :key="item.number"
        :class="[
          ' md:rounded-full md:flex md:flex-col md:items-center max-md:mb-20 mt-2 relative',
          item.number === '5'
            ? 'max-md:col-span-full max-md:justify-self-center '
            : '',
        ]"
      >
        <img
          src="/images/subscribe/background.png"
          alt="bg"
          class="w-[158px] h-[105px] md:w-[198px] md:h-[135px]"
        />
        <img
          :src="item.images"
          :alt="item.name"
          class="w-[80px] md:w-[120px] h-auto mb-4 left-10 absolute bottom-[50%]"
        />
        <p
          class="text-[14px] top-[60%] md:absolute md:left-auto max-md:text-center md:text-sm text-[#17A398] font-semibold"
          :class="[
            item.name === 'Pembayaran'
              ? 'absolute max-md:left-8'
              : '' || item.name === 'Selesai'
              ? 'absolute max-md:left-12'
              : 'absolute max-md:ml-4',
          ]"
        >
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
          name: "Menunggu Proses",
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
