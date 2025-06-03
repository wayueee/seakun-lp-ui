<template>
  <div>
    <div>
      <div
        class="bg-white relative shadow-md rounded-2xl flex flex-col px-3 w-[268px] h-[434.5px]"
      >
        <button
          class="absolute bottom-0 mt-4 bg-[#08A081] hover:bg-[#8ADAC9] text-white w-[240px] h-[48px] mb-3 ml-1 py-4 rounded-lg text-sm"
        >
          Pesan
        </button>
        <div
          class="mx-auto my-3"
          :class="
            card.name === 'Youtube' || card.name === 'Apple Music' ? 'mt-5' : ''
          "
        >
          <img :src="card.images" alt="icon" class="w-[76px] h-[28px] mb-3" />
        </div>
        <div class="flex">
          <img
            :src="card.imagesCard"
            alt="icon"
            :class="card.name === 'Youtube' ? 'w-[44.60px] h-[31px]' : ''"
            class="ml-2 mr-5 w-12 h-auto mb-3"
          />
          <h2
            :class="card.name === 'Youtube' ? 'py-2' : 'pt-4'"
            class="text-sm font-semibold mb-1"
          >
            {{ card.name }}
          </h2>
        </div>
        <hr :class="card.name === 'Youtube' ? 'mb-3 mt-2' : 'mb-1'" />

        <div class="relative">
          <div v-for="user in card.type" :key="user" class="mb-2 relative">
            <p class="text-[13px] text-gray-500">{{ user.user }}</p>
            <p class="text-[14px] font-semibold mb-1">
              {{ user.price
              }}<span class="text-sm font-normal"> /{{ user.duration }}</span>
            </p>
            <p
              class="absolute px-2 right-0 top-2 text-[10px] pt-2 rounded-xl bg-[#E9FAF5] text-[#00BA88] w-[120x] h-[31px]"
            >
              {{ user.choiceDuration }}
            </p>
          </div>
        </div>
        <div class="absolute bottom-[18%] flex">
          <img
            src="/images/card/vector.png"
            alt="eyes"
            class="w-[15] h-[10px] mt-1 mx-2"
          />
          <button
            class="text-[#08A081] hover:text-green-700 text-[13px] font-thin"
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
