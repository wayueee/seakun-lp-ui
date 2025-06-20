<template>
  <div class="relative text-center w-[102px] h-[115px] md:w-[132px] md:h-[188px] mb-[10%]">
    <button
      class="absolute bottom-0 ml-2 text-[11px] leading-[18px] w-[86px] h-[18px] md:w-[132px] font-semibold md:h-[36px] border left-0 rounded-[6px] bg-[#08A081] hover:bg-[#8ADAC9] text-white"
      :disabled="
        card.name === 'Sefitnes' ||
        card.name === 'Seatap' ||
        card.name === 'Sekelas' ||
        card.name === 'Sekatering' ||
        card.name === 'Sekantor' ||
        card.name === 'Sejalan'||
        card.name === 'Seumrah'||
        card.name === 'Setrip'
      "
      :class="
        card.name === 'Sefitnes' ? 'bg-[#8ADAC9] !border-white': ''||
        card.name === 'Seatap' ? 'bg-[#8ADAC9] !border-white': ''||
        card.name === 'Sekelas' ? 'bg-[#8ADAC9] !border-white': ''||
        card.name === 'Sekatering' ? 'bg-[#8ADAC9] !border-white': ''||
        card.name === 'Sekantor' ? 'bg-[#8ADAC9] !border-white': ''||
        card.name === 'Sejalan'? 'bg-[#8ADAC9] !border-white': ''||
        card.name === 'Seumrah'? 'bg-[#8ADAC9] !border-white': ''||
        card.name === 'Setrip' ? 'bg-[#8ADAC9] !border-white': '' ||
        card.name === 'Layanan Belum Terdaftar?' ? '!text-[#08A081] bg-white  hover:bg-white': ''
      "
    >
      {{ card.button }}
    </button>
    <img
      :src="card.images"
      :alt="card.name"
      class="w-[60px] md:w-[120px] h-auto mx-auto"
      :class="card.name === 'SeGlowUp' ? 'w-[47px] md:w-[90px]' : ''"
    />
    <h1 class="text-[#08A081] font-semibold text-[13px] md:text-[18px] mb-1 mt-2"
    :class="card.name === 'Layanan Belum Terdaftar?' ? '!text-[12px] md:!text-[17px]': ''">
      {{ card.name }}
    </h1>
    <p class="text-[#08A081] text-[11px] md:text-[14px]">{{ card.title }}</p>
  </div>
</template>

<script>
export default {
  props: {
    card: {
      type: Object,
      default: () => {},
    },
  },
};
</script>

<style></style>
