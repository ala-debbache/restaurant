<template lang="">
    <div id="hero-section">
        <nav-bar></nav-bar>
        <main class="main">
            <div class="content">
                <h1 data-aos="fade-down" data-aos-delay="500">Title Here</h1>
                <p data-aos="fade-right" data-aos-delay="500">
                    Duis culpa dolore eu sint dolore qui aliquip ex eu ullamco in proident aute pariatur. Ad elit aliqua veniam in proident ipsum mollit proident velit reprehenderit tempor minim deserunt ad. Ullamco nisi velit.
                </p>
                <v-btn
                data-aos="fade-right" data-aos-delay="500"
                color="#f2b705"
                elevation="2"
                large
                >Order Now</v-btn>
            </div>
        </main>
    </div>
</template>
<script>
import NavBar from "./partials/NavBar.vue";
export default {
  name: "HeroSection",
  components: {
    NavBar,
  },
};
</script>
<style scoped>
#hero-section {
  width: 100%;
  height: 100vh;
  padding: 0 5%;
  background: url("@/assets/images/hero.png"),
    url("@/assets/images/hero-section-backround.jpg");
  background-size: 65% 100%, cover;
  background-repeat: no-repeat;
  background-position: right, center;
  display: flex;
  flex-direction: column;
}

.overlay {
  display: none;
}

.main {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: row-reverse;
}

.content {
  width: 50%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.content h1 {
  font-size: 84px;
  color: var(--yellow-2);
}

.content p {
  color: var(--white);
  max-width: 80%;
  text-align: justify;
  margin-bottom: 20px;
}

.content button {
  max-width: max-content;
}

@media only screen and (max-width: 1400px) {
  #hero-section {
    height: fit-content;
    background: linear-gradient(
        0deg,
        rgba(38, 38, 38, 0.75) 100%,
        rgba(38, 38, 38, 0.75) 100%
      ),
      url("@/assets/images/hero-section-backround-reverse.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
  }
  .main {
    height: fit-content;
    padding: 100px 0;
    flex-direction: row;
    align-items: center;
  }
}

@media only screen and (max-width: 1000px) {
  .content {
    width: 80%;
  }
  .content h1 {
    font-size: 68px;
  }
  .content p {
    font-size: 20px;
  }
}

@media only screen and (max-width: 900px) {
}

@media only screen and (max-width: 700px) {
  .content {
    width: 100%;
  }
  .content h1 {
    font-size: 54px;
  }
  .content p {
    max-width: 100%;
  }
}
</style>