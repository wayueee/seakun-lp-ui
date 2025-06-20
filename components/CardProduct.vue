<template>
  <div>
    <div>
      <div
        class="bg-white relative shadow-md rounded-2xl flex flex-col px-2  md:px-3 w-[178px] h-[338px] md:w-[268px] md:h-[434.5px]"
      >
        <button
          class="absolute bottom-0 md:mt-4  max-md:text-xs bg-[#08A081] hover:bg-[#8ADAC9] text-white md:w-[240px] w-[142px] h-[34px] md:h-[48px] mb-3 max-md:ml-3 md:py-4  rounded-lg text-sm"
        >
          Pesan
        </button>
        <div
          class="mx-auto my-3"
          :class="
            card.name === 'Youtube' || card.name === 'Apple Music' ? 'mt-5' : ''
          "
        >
          <img :src="card.images" alt="icon" class="w-[40px] md:w-[76px] h-[21px] md:h-[35px] md:mb-3" />
        </div>
        <div class="flex">
          <img
            :src="card.imagesCard"
            alt="icon"
            :class="card.name === 'Youtube' ? 'md:w-[44.60px] md:h-[31px]' : ''"
            class="ml-2 mr-5 w-7 md:w-12 h-auto mb-3"
          />
          <h2
            :class="card.name === 'Youtube' ? 'md:py-2' : 'pt-2 md:pt-4'"
            class="text-[14px] md:text-sm font-semibold mb-1"
          >
            {{ card.name }}
          </h2>
        </div>
        <hr :class="card.name === 'Youtube' ? 'mb-3 mt-2' : 'md:mb-1 mb-4'" />

        <div class="relative">
          <div v-for="user in card.type" :key="user" class="mb-2 relative">
            <p class="md:text-[13px] text-[10px] text-gray-500">{{ user.user }}</p>
            <p class="md:text-[14px] text-[11px] font-semibold mb-1">
              {{ user.price
              }}<span class="text-[11px] md:text-sm font-normal"> /{{ user.duration }}</span>
            </p>
            <p
              class="absolute md:px-2 right-0 top-2 md:text-[10px] text-[9px] md:pt-2 rounded-xl bg-[#E9FAF5] text-[#00BA88] w-[70px] md:w-[120px] md:h-[31px]"
            >
              {{ user.choiceDuration }}
            </p>
          </div>
        </div>
        <div class="absolute bottom-[18%] flex">
          <img
            src="/images/card/vector.png"
            alt="eyes"
            class="w-[15] h-[10px] md:mt-1 mx-2"
          />
          <button
            class="text-[#08A081] hover:text-green-700 md:text-[13px] text-[10px] font-thin"
          >
            Lihat Skema harga
          </button>
        </div>
      </div>
    </div>
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
