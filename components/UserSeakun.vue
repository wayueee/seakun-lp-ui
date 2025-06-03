<template>
  <div class="py-[6%] relative">
    <h1 class="text-[30px] font-semibold pb-2">Pengguna Seakun</h1>
    <p class="text-[18px] leading-7 text-black/50">
      Psst! Sudah ada puluhan ribu pengguna dan ribuan grup yang bergabung
      bersama kami!
    </p>
    <div class="flex gap-4 mt-10 relative">
      <img
        class="w-[50px] h-auto absolute mt-2 right-0"
        src="/images/user/next.png"
        alt="bg"
      />
      <div
      class="flex shadow-lg rounded-lg items-center py-3"
      :class="
          item.name == 'Youtube' ? 'gap-3 px-4 border border-[#08A081]' : 'px-4'
        "
        v-for="item in grups"
        :key="item"
      >
        <img class="w-[35px] h-[30px]" :src="item.images" alt="bg" />
        <h1 class="font-semibold">{{ item.name }}</h1>
        <p class="text-black/60">{{ item.group }}</p>
      </div>
    </div>
    <div class="flex gap-5 mt-6">
      <div
        v-for="group in itemsGroup"
        :key="group"
        class="shadow-lg rounded-lg w-[266px] h-[272px]"
      >
        <div class="flex relative items-center m-3">
          <img class="w-[138px] h-auto" :src="group.images" alt="bg" />
          <h1
            class="absolute right-0 text-white px-2 rounded-full"
            :class="
              group.available == 'available' ? 'bg-[#08A045]' : 'bg-[#FB2525]'
            "
          >
            {{ group.available }}
          </h1>
        </div>
        <div class="flex relative">
          <p class="mx-3 text-[16px] font-semibold mb-2">{{ group.group }}</p>
          <button class="absolute right-3">
            <img
            class="w-[22px] h-auto"
            :class="group.available == 'full' ? 'hidden' : ''"
            :src="group.atomImages"
            alt=""
            />
          </button>
        </div>
        <img
          class="w-[50px] h-auto absolute mt-2 right-0"
          src="/images/user/next.png"
          alt="bg"
        />
          <hr/>
          <div v-for="item,index in group.name" :key="index">
            <h3 :class="item == 'Slot tersedia' ? '!text-[#417465]' : ''" class="ml-3 mt-1">{{ index+1 }}<span class=" ml-2"
              >{{ item }}</span></h3>
            </div>
          </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      grups: [
        {
          images: "/images/user/youtube.png",
          name: "Youtube",
          group: "(200 grup)",
        },
        {
          images: "/images/user/spotify.png",
          name: "",
          group: "",
        },
        {
          images: "/images/user/google-one.png",
          name: "",
          group: "",
        },
        {
          images: "/images/user/netflix.png",
          name: "",
          group: "",
        },
        {
          images: "/images/user/music-one.png",
          name: "",
          group: "",
        },
        {
          images: "/images/user/apple.png",
          name: "",
          group: "",
        },
        {
          images: "/images/user/apple-one.png",
          name: "",
          group: "",
        },
        {
          images: "/images/user/apple-tv.png",
          name: "",
          group: "",
        },
        {
          images: "/images/user/microsoft.png",
          name: "",
          group: "",
        },
        {
          images: "/images/user/watpat.png",
          name: "",
          group: "",
        },
        {
          images: "/images/user/disney.png",
          name: "",
          group: "",
        },
        {
          images: "/images/user/canva.png",
          name: "",
          group: "",
        },
      ],
      itemsGroup: [
        {
          images: "images/user/item-youtube.png",
          atomImages: "/images/user/vector.png",
          group: "Group 1836",
          available: "available",
          name: ["A********************a", "n*****************a", " h*********a", " s*****a", "Slot tersedia"],
        },
        {
          images: "images/user/item-youtube.png",
          atomImages: "/images/user/vector.png",
          group: "Group 1837",
          available: "available",
          name: ["A********************a", "n*****************a", " h*********a", " s*****a", "Slot tersedia"],
        },
        {
          images: "images/user/item-youtube.png",
          atomImages: "/images/user/vector.png",
          group: "Group 1838",
          available: "available",
          name: ["A********************a", "n*****************a", " h*********a", " s*****a", "Slot tersedia",],
        },
        {
          images: "images/user/item-youtube.png",
          atomImages: "/images/user/vector.png",
          group: "Group 1839",
          available: "full",
          name: ["A********************a", "n*****************a", " h*********a", " s*****a", " h*********a",],
        },
      ],
    };
  },
};
</script>

<style></style>
