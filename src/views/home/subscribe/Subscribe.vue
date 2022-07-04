<template lang="">
    <div id="subscribe">
      <img src="@/assets/images/onion.png" class="icon" id="onion" />
      <img src="@/assets/images/pepper.png" class="icon" id="pepper" />
      <img src="@/assets/images/pepper.png" class="icon" id="pepper2" />
      <img src="@/assets/images/avocado.png" class="icon" id="avocado" />
      <img src="@/assets/images/avocado.png" class="icon" id="avocado2" />
      <img src="@/assets/images/tomato.png" class="icon" id="tomato" />
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
  position: relative;
  width: 100%;
  height: 100vh;
  padding: 50px 5%;
  background-color: var(--white);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.icon {
  position: absolute;
}

#onion {
  width: 150px;
  bottom: 30%;
  left: 10%;
  transform: rotate(60deg);
}

#pepper {
  width: 100px;
  top: 25%;
  right: 7%;
  transform: rotate(-120deg);
}

#pepper2 {
  width: 100px;
  bottom: 10%;
  right: 20%;
  transform: rotate(30deg);
}

#avocado {
  width: 100px;
  top: 10%;
  right: 30%;
  transform: rotate(3deg);
}

#avocado2 {
  width: 100px;
  bottom: 10%;
  left: 20%;
  transform: rotate(-90deg);
}

#tomato {
  width: 100px;
  top: 10%;
  right: 65%;
  transform: rotate(-20deg);
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

@media only screen and (max-width: 1500px) {
  #subscribe {
    height: fit-content;
  }
  #pepper2 {
    display: none;
  }
  #avocado2 {
    display: none;
  }
  #onion {
    bottom: 20%;
    left: 7%;
  }
  #avocado {
    top: 10%;
    right: 20%;
  }
  #tomato {
    top: 10%;
    left: 20%;
  }
  #pepper {
    top: 55%;
    right: 10%;
  }
}

@media only screen and (max-width: 1200px) {
  .icon {
    display: none;
  }
}

@media only screen and (max-width: 900px) {
  .form {
    width: 90%;
    margin-bottom: 100px;
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