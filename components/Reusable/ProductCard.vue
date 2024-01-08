<template>
  <div
    class="rounded-lg bg-[#FFE58C] px-16 pt-10 pb-16 flex gap-28 items-center"
  >
    <div class="w-1/2">
      <h1 class="text-5xl">{{ props.selectedCard[0].product_title }}</h1>
      <p class="text-2xl pt-6 pb-8">
        {{ props.selectedCard[0].product_description }}
      </p>
      <button
        class="border-2 border-black text-xl rounded-3xl py-2 px-6 bg-[#F15A29]"
      >
        Discover Product
      </button>
    </div>
    <div class="w-1/2 text-lg font-normal">
      <div
        v-for="(product, i) in props.selectedCard[0].Accordion"
        :key="i"
        class="py-6 border-b border-black"
      >
        <div
          class="flex justify-between items-center hover:cursor-pointer text-lg"
        >
          {{ product.title }}
          <n-icon :size="15">
            <ChevronDown />
          </n-icon>
        </div>
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
import { NIcon, NDropdown } from "naive-ui";
import { ChevronDown } from "@vicons/ionicons5";

const props = defineProps({
  selectedCard: Object,
});
</script>
