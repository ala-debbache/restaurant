<template lang="">
    <div data-aos="fade-up" class="card">
        <h5>{{number}}</h5>
        <p>{{label}}</p>
    </div>
</template>
<script>
export default {
  name: "StatisticsCard",
  props: ["number", "label"],
};
</script>
<style scoped>
.card {
  width: 200px;
  height: 200px;
  border: 5px solid var(--white);
  border-radius: 50%;
  display: flex;
  flex-direction: column;
  text-align: center;
  justify-content: center;
  background-color: var(--black);
}

.card h5 {
  font-size: 42px;
  font-weight: 600;
  color: var(--yellow-1);
}

.card p {
  font-size: 30px;
  line-height: 0;
  font-weight: 600;
  color: var(--white);
}

@media only screen and (max-width: 1000px) {
  .card {
    margin-bottom: 20px;
  }
}
</style>