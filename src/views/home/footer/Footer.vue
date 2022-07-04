<template lang="">
    <div id="footer">
        <div class="description">
            <h5 class="title">Title Here</h5>
            <p>Ea pariatur officia pariatur est minim. Laboris amet Lorem culpa dolor irure sit cupidatat veniam duis exercitation fugiat.</p>
            <ul class="social-links">
                <li v-for="(link,i) in social" :key="i" class="social-link">
                    <a :href="link.to">
                        <v-icon
                        large
                        color="#f2f2f2"
                        >
                        {{link.icon}}
                        </v-icon>
                    </a>
                </li>
            </ul>
        </div>
        <div class="footer-links">
            <FooterLinksSection v-for="(section,i) in footerLinks" :key="i" :title="section.title" :links="section.links" />
        </div>
    </div>
</template>
<script>
import FooterLinksSection from "./partials/FooterLinksSection.vue";
export default {
  name: "Footer",
  components: {
    FooterLinksSection,
  },
  data() {
    return {
      social: [
        {
          icon: "mdi-instagram",
          to: "#",
        },
        {
          icon: "mdi-facebook",
          to: "#",
        },
        {
          icon: "mdi-twitter",
          to: "#",
        },
        {
          icon: "mdi-whatsapp",
          to: "#",
        },
      ],
      footerLinks: [
        {
          title: "About",
          links: [
            {
              label: "link number 1",
              to: "#",
            },
            {
              label: "link number 2",
              to: "#",
            },
            {
              label: "link number 3",
              to: "#",
            },
            {
              label: "link number 4",
              to: "#",
            },
            {
              label: "link number 5",
              to: "#",
            },
          ],
        },
        {
          title: "Services",
          links: [
            {
              label: "link number 1",
              to: "#",
            },
            {
              label: "link number 2",
              to: "#",
            },
            {
              label: "link number 3",
              to: "#",
            },
            {
              label: "link number 4",
              to: "#",
            },
            {
              label: "link number 5",
              to: "#",
            },
          ],
        },
        {
          title: "Others",
          links: [
            {
              label: "link number 1",
              to: "#",
            },
            {
              label: "link number 2",
              to: "#",
            },
            {
              label: "link number 3",
              to: "#",
            },
          ],
        },
      ],
    };
  },
};
</script>
<style scoped>
#footer {
  width: 100%;
  /* height: 100vh; */
  padding: 100px 5%;
  background-color: var(--black);
  display: flex;
  align-items: center;
}

.description {
  width: 50%;
}

.title {
  font-size: 24px;
  color: var(--white);
  margin-bottom: 20px;
}

.description p {
  max-width: 80%;
  font-size: 18px;
  text-align: justify;
  color: var(--white);
  margin-bottom: 30px;
}

.social-links {
  display: flex;
  list-style: none;
  text-align: start;
  padding: 0;
}

.social-link a {
  text-decoration: none;
  margin-right: 10px;
}

.footer-links {
  width: 50%;
  display: flex;
  justify-content: space-around;
}

@media only screen and (max-width: 1000px) {
  #footer {
    height: fit-content;
    padding: 100px 5%;
    flex-direction: column;
    background: var(--black);
  }
  .description {
    width: 100%;
    margin-top: 100px;
  }
  .footer-links {
    width: 100%;
    justify-content: space-between;
  }
}
@media only screen and (max-width: 600px) {
  #footer {
    height: fit-content;
    padding: 50px 5%;
  }
  .footer-links {
    flex-direction: column;
    justify-content: flex-start;
  }
}
</style>