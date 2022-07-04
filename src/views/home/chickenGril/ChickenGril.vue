<template lang="">
    <div id="chicken-gril">
        <SectionContent :title="title" :description="description" :callToAction="callToAction" />
        <SectionImage :url="imageUrl" />
    </div>
</template>
<script>
import SectionContent from "../general/SectionContent.vue";
import SectionImage from "../general/SectionImage.vue";
export default {
  name: "ChickenGril",
  data() {
    return {
      title: "Chicken Gril",
      description:
        "Duis culpa dolore eu sint dolore qui aliquip ex eu ullamco in proident aute pariatur. Ad elit aliqua veniam in proident ipsum mollit proident velit reprehenderit tempor minim deserunt ad. Ullamco nisi velit.",
      callToAction: {
        label: "Order now",
        to: "#",
      },
      imageUrl: require("@/assets/images/1.jpg"),
    };
  },
  components: {
    SectionContent,
    SectionImage,
  },
};
</script>
<style scoped>
#chicken-gril {
  width: 100%;
  height: 100vh;
  padding: 50px 5%;
  background: url("@/assets/images/wave-bg-2-reverse.png");
  background-color: var(--white);
  background-size: 100% 100%;
  background-repeat: no-repeat;
  display: flex;
  align-items: center;
}

@media only screen and (max-width: 1500px) {
  #chicken-gril {
    height: fit-content;
    /* padding: 100px 5%; */
  }
}
@media only screen and (max-width: 900px) {
  #chicken-gril {
    /* padding-top: 100px; */
    /* height: fit-content; */
    flex-direction: column;
    background: var(--white);
  }
}
</style>