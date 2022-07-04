<template lang="">
    <div id="home">
        <HeroSection />
        <BestSaller />
        <OrientalTaste />
        <Statistics />
        <ChickenGril />
        <LenoraFields />
        <Subscribe />
        <Footer />
    </div>
</template>
<script>
import HeroSection from "./heroSection/HeroSection";
import BestSaller from "./bestSaller/BestSaller";
import OrientalTaste from "./orientalTaste/OrientalTaste";
import Statistics from "./statistics/Statistics";
import ChickenGril from "./chickenGril/ChickenGril";
import LenoraFields from "./lenoraFields/LenoraFields";
import Subscribe from "./subscribe/Subscribe";
import Footer from "./footer/Footer";

export default {
  name: "Home",
  components: {
    HeroSection,
    BestSaller,
    OrientalTaste,
    Statistics,
    ChickenGril,
    LenoraFields,
    Subscribe,
    Footer,
  },
};
</script>
<style lang="">
</style>