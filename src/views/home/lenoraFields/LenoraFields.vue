<template>
  <div id="lenora-fields">
    <div class="overlay"></div>
    <div class="content">
      <p data-aos="fade-down">
        Magna deserunt tempor voluptate reprehenderit veniam anim. Reprehenderit
        magna nostrud excepteur nisi exercitation officia et dolor.
      </p>
      <h3 data-aos="fade-down">Lenora Fields</h3>
    </div>
  </div>
</template>
<script>
export default {
  name: "LenoraFields",
};
</script>
<style scoped>
#lenora-fields {
  width: 100%;
  height: 100vh;
  padding: 0 5%;
  background: url("@/assets/images/1.jpg");
  /* filter: blur(1px); */
  background-size: cover;
  background-position: center;
  position: relative;
}
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(242, 203, 5, 0.5);
  backdrop-filter: blur(15px);
  z-index: 0;
  /* opacity: 0.5; */
}
.content {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  z-index: 1;
}
.content p {
  max-width: 80%;
  font-size: 30px;
}
.content h3 {
  font-size: 54px;
}

@media only screen and (max-width: 1500px) {
  #lenora-fields {
    height: 50vh;
  }
}

@media only screen and (max-width: 900px) {
  .content p {
    font-size: 20px;
  }
  .content h3 {
    font-size: 48px;
  }
}

@media only screen and (max-width: 800px) {
  .content p {
    font-size: 18px;
  }
  .content h3 {
    font-size: 40px;
  }
}
</style>