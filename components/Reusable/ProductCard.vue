<template>
  <div
    class="rounded-lg bg-[#FFE58C] px-8 min-[428px]:px-16 pt-10 pb-16 flex flex-col min-[428px]:flex-row gap-8 min-[428px]:gap-28 items-center"
  >
    <div class="min-[428px]:w-1/2">
      <h1 class="text-[32px] min-[428px]:text-5xl">
        {{ props.selectedCard.product_title }}
      </h1>
      <p class="text-xl min-[428px]:text-2xl pt-6 min-[428px]:pb-8">
        {{ props.selectedCard.product_description }}
      </p>
      <button
        class="border-2 border-black text-xl w-fit rounded-3xl py-2 px-6 bg-[#F15A29] hidden min-[428px]:block"
        @click="productClicked()"
      >
        Discover Product
      </button>
    </div>
    <div class="w-full min-[428px]:w-1/2 text-lg font-normal">
      <div
        v-for="(product, i) in props.selectedCard.Accordion"
        :key="i"
        class="py-6 border-b border-black"
      >
        <div
          class="flex justify-between items-center hover:cursor-pointer text-lg"
        >
          {{ product.title }}
          <n-icon :size="15" @click="handleAccordionClick(product.id)">
            <ChevronDown />
          </n-icon>
        </div>
        <div
          v-if="product.id == selectedId"
          class="border-t-2 border-[#ffa500] bg-[#ffdb9a]"
        >
          <ul v-for="(acc, i) in product.Options">
            <li>{{ acc }}</li>
          </ul>
        </div>
      </div>
    </div>
    <a
      href="https://tailwindcss.com/"
      target="_blank"
      class="border-2 border-black text-xl rounded-3xl py-2 px-6 bg-[#F15A29] min-[428px]:hidden"
    >
      Discover Product
    </a>
  </div>
</template>
<script lang="ts" setup>
import { NIcon, NDropdown } from "naive-ui";
import { ChevronDown } from "@vicons/ionicons5";

const props = defineProps({
  selectedCard: Object,
});

const router = useRouter();

const selectedId: Ref<Number> = ref(0);
const handleAccordionClick = (id: Number) => {
  if (selectedId.value != id) {
    selectedId.value = id;
  } else {
    selectedId.value = 0;
  }
};

const productClicked = () => {
  router.push({
    path: `/productInfo/${props.selectedCard.id}`,
  });
};
</script>
