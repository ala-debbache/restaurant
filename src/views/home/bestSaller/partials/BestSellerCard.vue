<template>
  <div data-aos="fade-up" class="card">
    <img :src="image" :alt="title" />
    <h5>{{ title }}</h5>
    <p>{{ description }}</p>
  </div>
</template>
<script>
export default {
  name: "BestSellerCard",
  props: ["title", "description", "image"],
};
</script>
<style scoped>
.card {
  max-width: 250px;
  text-align: center;
}

.card h5 {
  font-size: 30px;
  color: var(--yellow-1);
}

.card p {
  font-size: 18px;
}

.card img {
  max-width: 250px;
  border-radius: 50%;
}

@media only screen and (max-width: 800px) {
  .card {
    margin-bottom: 20px;
  }
  .card img {
    max-width: 200px;
    border-radius: 50%;
  }
}
</style>