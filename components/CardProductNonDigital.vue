<template>
  <div class="relative text-center w-[132px] h-[188px] mb-[10%]">
    <button
      class="absolute bottom-0 w-[132px] h-[32px] border left-0 rounded-xl bg-[#08A081] hover:bg-[#8ADAC9] border-[#08A081] text-white font-medium"
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
        card.name === 'Layanan Belum Terdaftar?' ? '!text-[#08A081] bg-white': ''
      "
    >
      {{ card.button }}
    </button>
    <img
      :src="card.images"
      :alt="card.name"
      class="w-[120px] h-auto mx-auto"
      :class="card.name === 'SeGlowUp' ? 'w-[90px]' : ''"
    />
    <h1 class="text-[#08A081] font-semibold mb-1 mt-2">
      {{ card.name }}
    </h1>
    <p class="text-[#08A081]">{{ card.title }}</p>
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
