<template>
  <div>
    <div
      class="bg-white rounded-2xl flex justify-between items-center px-6 py-4"
      style="box-shadow: 0px 8px 0px #ffd540"
    >
      <img :src="props.product.icon" class="w-6" />
      <h3 class="text-2xl font-medium">{{ props.product.title }}</h3>
      <n-icon :size="18" @click="selectCard(props.product.id)">
        <PlusOutlined class="text-[#3C479D]" />
      </n-icon>
    </div>
    <ReusableProductCard
      v-if="props.product.id == selectedId"
      :selectedCard="props.product"
    />
  </div>
</template>
<script lang="ts" setup>
import { NIcon } from "naive-ui";
import { PlusOutlined } from "@vicons/material";

const props = defineProps({
  product: Object,
  id: Number,
  icon: String,
});

const selectedId: Ref<Number> = ref(0);

const selectCard = (id: Number) => {
  if (selectedId.value != id) {
    selectedId.value = id;
  } else {
    selectedId.value = 0;
  }
};
</script>
