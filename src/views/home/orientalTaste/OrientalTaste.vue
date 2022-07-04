<template lang="">
    <div id="oriental-taste">
        <SectionContent :title="title" :description="description" :callToAction="callToAction" />
        <SectionImage :url="imageUrl" />
    </div>
</template>
<script>
import SectionContent from "../general/SectionContent.vue";
import SectionImage from "../general/SectionImage.vue";
export default {
  name: "OrientalTaste",
  data() {
    return {
      title: "Oriental Taste",
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
#oriental-taste {
  width: 100%;
  height: 100vh;
  padding: 100px 5%;
  padding-bottom: 100px;
  background: url("@/assets/images/wave-bg-1-reverse.png");
  background-color: var(--white);
  background-size: 100% 100%;
  background-repeat: no-repeat;
  background-position: bottom;
  display: flex;
  align-items: center;
}
@media only screen and (max-width: 1500px) {
  #oriental-taste {
    height: fit-content;
  }
}
@media only screen and (max-width: 900px) {
  #oriental-taste {
    flex-direction: column;
    background: var(--white);
  }
}
</style>