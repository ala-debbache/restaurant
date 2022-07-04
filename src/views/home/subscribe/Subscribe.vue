<template lang="">
    <div id="subscribe">
        <SectionDescription :title="title" :text="text" :color="color" />
        <div data-aos="fade-up" class="form">
          <input type="text" placeholder="Your email" />
          <button>Subscribe</button>
        </div>
    </div>
</template>
<script>
import SectionDescription from "../general/SectionDescription.vue";
export default {
  name: "Subscribe",
  data() {
    return {
      title: "Subscribe",
      text: "Non ad eu esse qui mollit et est velit minim. Nostrud nostrud enim laboris sit cillum culpa tempor qui incididunt deserunt.",
      color: "var(--black)",
    };
  },
  components: {
    SectionDescription,
  },
};
</script>
<style scoped>
#subscribe {
  width: 100%;
  height: 100vh;
  padding: 0 5%;
  background: url("@/assets/images/subscribe.png");
  /* background-color: var(--white); */
  background-size: cover;
  background-position: center;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.form {
  width: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  box-shadow: 0px 0px 41px 14px rgba(38, 38, 38, 0.15);
  border-radius: 5px 0 0 5px;
}

.form input {
  width: 70%;
  height: 50px;
  padding: 0 10px;
  border: none;
  outline: none;
  background-color: var(--white);
  border-radius: 5px 0 0 5px;
}
.form button {
  width: 30%;
  padding: 0 10px;
  height: 50px;
  background-color: var(--yellow-2);
  border-radius: 0 5px 5px 0;
}

@media only screen and (max-width: 900px) {
  #subscribe {
    background: var(--white);
  }
  .form {
    width: 90%;
  }
}
@media only screen and (max-width: 500px) {
  .form input {
    width: 60%;
  }
  .form button {
    width: 40%;
  }
}
</style>