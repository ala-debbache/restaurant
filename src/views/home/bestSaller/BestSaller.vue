<template lang="">
    <div id="best-saller">
        <SectionDescription :title="title" :text="text" :color="color" />
        <div class="cards">
            <BestSellerCard v-for="(item,i) in bestSellers" :key="i" :title="item.title" :description="item.description" :image="item.image" />
        </div>
    </div>
</template>
<script>
import SectionDescription from "../general/SectionDescription.vue";
import BestSellerCard from "./partials/BestSellerCard.vue";
export default {
  name: "BestSaller",
  data() {
    return {
      title: "Best Saller",
      text: "Non ad eu esse qui mollit et est velit minim. Nostrud nostrud enim laboris sit cillum culpa tempor qui incididunt deserunt.",
      color: "var(--black)",
      bestSellers: [
        {
          title: "Card Title",
          description:
            "Amet ipsum qui dolore velit est occaecat incididunt duis ad deserunt.",
          image: require("@/assets/images/1.jpg"),
        },
        {
          title: "Card Title",
          description:
            "Amet ipsum qui dolore velit est occaecat incididunt duis ad deserunt.",
          image: require("@/assets/images/2.jpg"),
        },
        {
          title: "Card Title",
          description:
            "Amet ipsum qui dolore velit est occaecat incididunt duis ad deserunt.",
          image: require("@/assets/images/3.jpg"),
        },
      ],
    };
  },
  components: {
    SectionDescription,
    BestSellerCard,
  },
};
</script>
<style scoped>
#best-saller {
  width: 100%;
  height: 100vh;
  padding: 100px 5%;
  background-color: var(--white);
  display: flex;
  flex-direction: column;
  align-items: center;
}

.cards {
  width: 100%;
  display: flex;
  justify-content: space-around;
}

@media only screen and (max-width: 1500px) {
  #best-saller {
    height: fit-content;
  }
  .cards {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}

@media only screen and (max-width: 800px) {
  /* #best-saller {
    height: fit-content;
  } */
}
</style>