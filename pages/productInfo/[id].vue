<template>
  <div class="flex flex-col items-center mt-8">
    <p>product id = {{ product[0].id }}</p>
    <p>product title = {{ product[0].product_title }}</p>
    <p>description = {{ product[0].product_description }}</p>
    <p class="text-2xl">
      Since the design of detail page was not provided so I just displayed the
      data.
    </p>
  </div>
</template>
<script setup>
import multiplebox from "@/assets/svg/multiplebox.svg";
import multiplecircle from "@/assets/svg/multiplecircle.svg";
import bar from "@/assets/svg/bar.svg";
import heart from "@/assets/svg/heart.svg";

const router = useRouter();
const id = router.currentRoute.value.params.id;
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

const product = cardData.filter((card) => card.id == id);
</script>
