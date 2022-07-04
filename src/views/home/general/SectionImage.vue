<template >
  <div class="image">
    <img data-aos="fade-left" src="@/assets/images/2.jpg" />
  </div>
</template>
<script>
export default {
  name: "SectionImage",
  props: ["url"],
};
</script>
<style scoped>
.image {
  width: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.image img {
  width: 80%;
  border-radius: 50%;
}
@media only screen and (max-width: 900px) {
  .image {
    width: 100%;
    margin-bottom: 50px;
  }
  .image img {
    width: 80%;
  }
}
</style>