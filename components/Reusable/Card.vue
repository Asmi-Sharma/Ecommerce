<template>
  <div
    class="border border-[#cccccc] shadow-sm rounded-lg pt-4 pr-4 w-[266px] hover:shadow-2xl mt-6"
  >
    <div class="px-4">
      <div class="flex justify-between pb-2">
        <span class="font-medium">Card Title</span>
        <img :src="multiplebox" class="w-6" />
      </div>
      <div class="pr-2 pb-3">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
      </div>
    </div>
    <button
      class="border border-buttongrey rounded-se-3xl p-2 bg-buttongrey flex items-center gap-1"
      style="border-bottom-left-radius: inherit"
    >
      Discover
      <n-icon :size="12">
        <ArrowDownOutline />
      </n-icon>
    </button>
  </div>
</template>

<script setup>
import { NIcon } from "naive-ui";
import { ArrowDownOutline } from "@vicons/ionicons5";
import multiplebox from "@/assets/svg/multiplebox.svg";
</script>
