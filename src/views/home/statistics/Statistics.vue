<template lang="">
    <div id="statistics">
        <SectionDescription :title="title" :text="text" :color="color" />
        <div class="cards">
          <StatisticsCard v-for="(item,i) in statistics" :key="i" :number="item.number" :label="item.label.toUpperCase()" />
        </div>
    </div>
</template>
<script>
import SectionDescription from "../general/SectionDescription.vue";
import StatisticsCard from "./parials/StatisticsCard.vue";
export default {
  name: "Statistics",
  data() {
    return {
      title: "Statistics",
      text: "Non ad eu esse qui mollit et est velit minim. Nostrud nostrud enim laboris sit cillum culpa tempor qui incididunt deserunt.",
      color: "var(--white)",
      statistics: [
        {
          number: 123,
          label: "outlefts",
        },
        {
          number: 100,
          label: "chef",
        },
        {
          number: 100,
          label: "menu",
        },
        {
          number: 100,
          label: "country",
        },
      ],
    };
  },
  components: {
    SectionDescription,
    StatisticsCard,
  },
};
</script>
<style scoped>
#statistics {
  width: 100%;
  height: 100vh;
  padding: 0 5%;
  background: url("@/assets/images/statistics.png");
  background-size: 100% cover;
  background-position: center;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.cards {
  width: 100%;
  display: flex;
  justify-content: space-around;
}

@media only screen and (max-width: 900px) {
  #statistics {
    height: fit-content;
  }
  .cards {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}
</style>