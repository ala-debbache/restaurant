<template lang="">
    <div class="content">
        <h1 data-aos="fade-down" data-aos-delay="0">{{title}}</h1>
        <p data-aos="fade-right" data-aos-delay="0" contentEditable>
            {{description}}
        </p>
        <v-btn
        data-aos="fade-right" data-aos-delay="0"
        color="#f2b705"
        elevation="2"
        large
        >{{callToAction.label}}</v-btn>
    </div>
</template>
<script>
export default {
  name: "SectionContent",
  props: ["title", "description", "callToAction"],
};
</script>
<style scoped>
.content {
  width: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.content h1 {
  font-size: 84px;
  color: var(--yellow-2);
  transition: 0.5s;
}

.content p {
  color: var(--white);
  max-width: 80%;
  text-align: justify;
  margin-bottom: 20px;
  animation-delay: 0.5s;
  transition: 0.5s;
}

.content button {
  max-width: max-content;
  animation-delay: 1s;
  transition: 0.5s;
}

@media only screen and (max-width: 900px) {
  .content {
    margin-bottom: 50px;
    width: 100%;
    /* text-align: center;
    align-items: center; */
  }
  .content h1 {
    font-size: 58px;
  }
  .content p {
    color: var(--black);
    max-width: 90%;
  }
}

@media only screen and (max-width: 800px) {
}
</style>