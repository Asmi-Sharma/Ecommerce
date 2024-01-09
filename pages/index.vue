<template>
  <div class="container my-20">
    <div class="flex flex-col items-center">
      <h1 class="text-[28px] min-[428px]:text-[40px] font-bold">
        Section title
      </h1>
      <h2 class="text-lg min-[428px]:text-2xl">Section subtitle</h2>
    </div>
    <div
      class="flex flex-col min-[428px]:flex-row gap-8 min-[428px]:gap-4 justify-center mt-6"
    >
      <div v-for="(product, i) in cardData" :key="i">
        <ReusableCard
          :cardTitle="product.title"
          :id="product.id"
          :description="product.description"
          :icon="product.icon"
          :selectedCardId="selectedCardId"
          @selected="handleSelect"
          :class="'hidden min-[428px]:block'"
        />
        <ReusableCardSmall
          :product="product"
          :class="'min-[428px]:hidden mx-10'"
        />
      </div>
    </div>
    <ReusableProductCard
      class="mt-8 hidden min-[428px]:flex"
      :selectedCard="selectedCard[0]"
    />
  </div>
</template>

<script lang="ts" setup>
import multiplebox from "@/assets/svg/multiplebox.svg";
import multiplecircle from "@/assets/svg/multiplecircle.svg";
import bar from "@/assets/svg/bar.svg";
import heart from "@/assets/svg/heart.svg";

const selectedCardId: Ref<Number> = ref(1);

const cardData = [
  {
    id: 1,
    title: "Card Title 1",
    product_title: "Product title 1",
    icon: multiplebox,
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    product_description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent scelerisque risus id ante maximus blandit.",
    Accordion: [
      {
        id: 1,
        title: "Accordion title 1",
        Options: ["abc", "xyz", "lmn"],
      },
      {
        id: 2,
        title: "Accordion title 2",
        Options: ["asd", "fgh", "jkl"],
      },
      {
        id: 3,
        title: "Accordion title 3",
        Options: ["sun", "moon", "earth"],
      },
      {
        id: 4,
        title: "Accordion title 4",
        Options: ["orange", "apple", "mango"],
      },
    ],
  },
  {
    id: 2,
    title: "Card Title 2",
    product_title: "Product title 2",
    icon: multiplecircle,
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    product_description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent scelerisque risus id ante maximus blandit.",
    Accordion: [
      {
        id: 1,
        title: "Accordion title 1",
        Options: ["abc", "xyz", "lmn"],
      },
      {
        id: 2,
        title: "Accordion title 2",
        Options: ["asd", "fgh", "jkl"],
      },
      {
        id: 3,
        title: "Accordion title 3",
        Options: ["sun", "moon", "earth"],
      },
      {
        id: 4,
        title: "Accordion title 4",
        Options: ["orange", "apple", "mango"],
      },
    ],
  },
  {
    id: 3,
    title: "Card Title 3",
    product_title: "Product title 3",
    icon: bar,
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    product_description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent scelerisque risus id ante maximus blandit.",
    Accordion: [
      {
        id: 1,
        title: "Accordion title 1",
        Options: ["abc", "xyz", "lmn"],
      },
      {
        id: 2,
        title: "Accordion title 2",
        Options: ["asd", "fgh", "jkl"],
      },
      {
        id: 3,
        title: "Accordion title 3",
        Options: ["sun", "moon", "earth"],
      },
      {
        id: 4,
        title: "Accordion title 4",
        Options: ["orange", "apple", "mango"],
      },
    ],
  },
  {
    id: 4,
    title: "Card Title 4",
    product_title: "Product title 4",
    icon: heart,
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    product_description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent scelerisque risus id ante maximus blandit.",
    Accordion: [
      {
        id: 1,
        title: "Accordion title 1",
        Options: ["abc", "xyz", "lmn"],
      },
      {
        id: 2,
        title: "Accordion title 2",
        Options: ["asd", "fgh", "jkl"],
      },
      {
        id: 3,
        title: "Accordion title 3",
        Options: ["sun", "moon", "earth"],
      },
      {
        id: 4,
        title: "Accordion title 4",
        Options: ["orange", "apple", "mango"],
      },
    ],
  },
];

const selectedCard: Ref<Array<Object>> = ref(
  cardData.filter((card: any) => card.id == selectedCardId.value)
);

const handleSelect = (value: Number) => {
  selectedCardId.value = value;
  selectedCard.value = cardData.filter(
    (card: any) => card.id == selectedCardId.value
  );
};
</script>
