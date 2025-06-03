<template>
  <div>
    <div class="">
      <h1 class="mt-[8%] mb-3 text-3xl font-semibold">Layanan Non Digital</h1>
      <p class="mb-10 text-[18px]">
        Beragam layanan non digital untuk pengguna setia Seakun.
      </p>
    </div>
    <div class="grid grid-cols-7 mt-10 mb-7">
      <CardProductNonDigital
        v-for="item in productNonDigital"
        :key="item"
        :card="item"
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      productNonDigital: [
        {
          name: "Semabar",
          title: "(Main Bareng)",
          images: "/images/card-non-digital/semabar.png",
          button: "Pesan",
        },
        {
          name: "SeGlowUp",
          title: "(GlowUp Bareng)",
          images: "/images/card-non-digital/seglowup.png",
          button: "Pesan",
        },
        {
          name: "Sekurban",
          title: "(Kurban Bareng)",
          images: "/images/card-non-digital/sekurban.png",
          button: "Pesan",
        },
        {
          name: "Sekeranjang",
          title: "(Belanja Bareng)",
          images: "/images/card-non-digital/sekeranjang.png",
          button: "Pesan",
        },
        {
          name: "Sefitnes",
          title: "(Fitnes Bareng)",
          images: "/images/card-non-digital/sefitnes.png",
          button: "Segera Hadir",
        },
        {
          name: "Seatap",
          title: "(Tinggal Bareng)",
          images: "/images/card-non-digital/seatap.png",
          button: "Segera Hadir",
        },
        {
          name: "Sekelas",
          title: "(Kelas Bareng)",
          images: "/images/card-non-digital/sekelas.png",
          button: "Segera Hadir",
        },
        {
          name: "Sekatering",
          title: "(katering Bareng)",
          images: "/images/card-non-digital/sekatering.png",
          button: "Segera Hadir",
        },
        {
          name: "Sekantor",
          title: "(kantor Bareng)",
          images: "/images/card-non-digital/sekantor.png",
          button: "Segera Hadir",
        },
        {
          name: "Sejalan",
          title: "(jalan Bareng)",
          images: "/images/card-non-digital/sejalan.png",
          button: "Segera Hadir",
        },
        {
          name: "Seumrah",
          title: "(Umrah Bareng)",
          images: "/images/card-non-digital/seumrah.png",
          button: "Segera Hadir",
        },
        {
          name: "Setrip",
          title: "(Trip Bareng)",
          images: "/images/card-non-digital/setrip.png",
          button: "Segera Hadir",
        },
        {
          name: "Layanan Belum Terdaftar?",
          images: "/images/card-non-digital/layanan.png",
          button: "Ajukan Layanan",
        },
      ],
    };
  },
};
</script>

<style></style>
