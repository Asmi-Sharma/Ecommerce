<template>
  <div
    class="border border-[#cccccc] shadow-sm rounded-lg pt-4 pr-4 w-[273px] hover:shadow-2xl mt-6"
  >
    <div class="px-6">
      <div class="flex justify-between pb-8">
        <span class="text-2xl font-medium">{{ props.cardTitle }}</span>
        <img :src="props.icon" class="w-8" />
      </div>
      <div class="pr-2 pb-6 text-xl">
        {{ props.description }}
      </div>
    </div>
    <button
      class="border border-buttongrey rounded-se-3xl py-4 px-8 bg-buttongrey flex items-center gap-1 text-base"
      style="border-bottom-left-radius: inherit"
    >
      Discover
      <n-icon :size="15">
        <ArrowDownOutline />
      </n-icon>
    </button>
  </div>
</template>

<script lang="ts" setup>
import { NIcon } from "naive-ui";
import { ArrowDownOutline } from "@vicons/ionicons5";

const props = defineProps({
  cardTitle: String,
  id: Number,
  description: String,
  icon: String,
});
</script>
