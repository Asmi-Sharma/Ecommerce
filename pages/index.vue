<template>
  <div class="container mt-20">
    <div class="flex flex-col items-center">
      <h1 class="text-[48px] font-bold">Section title</h1>
      <h2 class="text-xl">Section subtitle</h2>
    </div>
    <div class="flex gap-2">
      <div v-for="(product, i) in cardData" :key="i">
        <ReusableCard
          :cardTitle="product.title"
          :id="product.id"
          :description="product.description"
          :icon="product.icon"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
import multiplebox from "@/assets/svg/multiplebox.svg";
import multiplecircle from "@/assets/svg/multiplecircle.svg";
import bar from "@/assets/svg/bar.svg";
import heart from "@/assets/svg/heart.svg";

const cardData = [
  {
    id: 1,
    title: "Card Title 1",
    product_title: "Product title 1",
    icon: multiplebox,
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    Accordion: [
      {
        title: "Accordion title 1",
        Options: ["abc", "xyz", "lmn"],
      },
      {
        title: "Accordion title 2",
        Options: ["asd", "fgh", "jkl"],
      },
      {
        title: "Accordion title 3",
        Options: ["sun", "moon", "earth"],
      },
      {
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
    Accordion: [
      {
        title: "Accordion title 1",
        Options: ["abc", "xyz", "lmn"],
      },
      {
        title: "Accordion title 2",
        Options: ["asd", "fgh", "jkl"],
      },
      {
        title: "Accordion title 3",
        Options: ["sun", "moon", "earth"],
      },
      {
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
    Accordion: [
      {
        title: "Accordion title 1",
        Options: ["abc", "xyz", "lmn"],
      },
      {
        title: "Accordion title 2",
        Options: ["asd", "fgh", "jkl"],
      },
      {
        title: "Accordion title 3",
        Options: ["sun", "moon", "earth"],
      },
      {
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
    Accordion: [
      {
        title: "Accordion title 1",
        Options: ["abc", "xyz", "lmn"],
      },
      {
        title: "Accordion title 2",
        Options: ["asd", "fgh", "jkl"],
      },
      {
        title: "Accordion title 3",
        Options: ["sun", "moon", "earth"],
      },
      {
        title: "Accordion title 4",
        Options: ["orange", "apple", "mango"],
      },
    ],
  },
];
</script>
