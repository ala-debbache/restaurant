<template lang="">
    <div data-aos="fade-down" class="description">
        <h3>{{title}}</h3>
        <p :style="'color:'+color">{{text}}</p>
    </div>
</template>
<script>
export default {
  name: "SectionDescription",
  props: ["title", "text", "color"],
};
</script>
<style scoped>
.description {
  width: 50%;
  margin-bottom: 50px;
  text-align: center;
}

.description h3 {
  font-size: 64px;
  color: var(--yellow-2);
  margin-bottom: 20px;
}

.description p {
  color: var(--white);
}

@media only screen and (max-width: 900px) {
  .description h3 {
    font-size: 54px;
  }
}

@media only screen and (max-width: 800px) {
  .description {
    width: 100%;
  }
  .description h3 {
    font-size: 48px;
  }
}
</style>