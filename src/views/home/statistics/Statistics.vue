<template lang="">
    <div id="statistics">
      <img src="@/assets/images/onion.png" class="icon" id="onion" />
      <img src="@/assets/images/pepper.png" class="icon" id="pepper" />
      <img src="@/assets/images/pepper.png" class="icon" id="pepper2" />
      <img src="@/assets/images/avocado.png" class="icon" id="avocado" />
      <img src="@/assets/images/avocado.png" class="icon" id="avocado2" />
      <img src="@/assets/images/tomato.png" class="icon" id="tomato" />
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
  position: relative;
  width: 100%;
  height: 100vh;
  padding: 50px 5%;
  background-color: var(--black);
  display: flex;
  flex-direction: column;
  align-items: center;
}

.icon {
  position: absolute;
}

#onion {
  width: 150px;
  bottom: 50%;
  left: 10%;
  transform: rotate(60deg);
}

#pepper {
  width: 100px;
  top: 25%;
  right: 7%;
  transform: rotate(-120deg);
}

#pepper2 {
  width: 100px;
  bottom: 10%;
  right: 20%;
  transform: rotate(30deg);
}

#avocado {
  width: 100px;
  top: 10%;
  right: 30%;
  transform: rotate(3deg);
}

#avocado2 {
  width: 100px;
  bottom: 10%;
  left: 20%;
  transform: rotate(-90deg);
}

#tomato {
  width: 100px;
  top: 10%;
  right: 65%;
  transform: rotate(-20deg);
}

.cards {
  width: 100%;
  display: flex;
  justify-content: space-around;
}

@media only screen and (max-width: 1500px) {
  #statistics {
    height: fit-content;
  }
  #pepper2 {
    display: none;
  }
  #avocado2 {
    display: none;
  }
  #onion {
    bottom: 40%;
    left: 7%;
  }
  #avocado {
    top: 10%;
    right: 20%;
  }
  #tomato {
    top: 10%;
    left: 20%;
  }
  #pepper {
    top: 40%;
    right: 10%;
  }
}

@media only screen and (max-width: 1200px) {
  .icon {
    display: none;
  }
}

@media only screen and (max-width: 1000px) {
  .cards {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    /* flex-direction: column; */
    align-items: center;
  }
  .cards > * {
    margin: 10px;
  }
}

@media only screen and (max-width: 900px) {
  #statistics {
    height: fit-content;
  }
}
</style>