<template lang="">
    <nav>
        <a href="#" class="logo">
            <img src="@/assets/images/logo.png" />
            <h3>Restaurant</h3>
        </a>
        <ul class="nav-links">
            <li class="nav-link" v-for="link in links" :key="link.label"><a :href="link.to">{{link.label}}</a></li>
            <li class="nav-link" id="close">
              <v-btn
                icon
                color="#f2f2f2"
                large
                @click="close"
              >
                <v-icon>mdi-close</v-icon>
              </v-btn>
            </li>
        </ul>
        <v-btn
          icon
          color="#f2f2f2"
          id="open"
          large
          @click="open"
        >
          <v-icon>mdi-menu</v-icon>
        </v-btn>
    </nav>
</template>
<script>
export default {
  name: "NavBar",
  data() {
    return {
      links: [
        {
          label: "Home",
          to: "#",
        },
        {
          label: "Products",
          to: "#",
        },
        {
          label: "Promo",
          to: "#",
        },
        {
          label: "About",
          to: "#",
        },
        {
          label: "Contact",
          to: "#",
        },
      ],
    };
  },
  methods: {
    open() {
      document.querySelector(".nav-links").style.top = 0;
    },
    close() {
      document.querySelector(".nav-links").style.top = "-1000px";
    },
  },
};
</script>
<style scoped>
nav {
  width: 100%;
  padding: 40px 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  text-decoration: none;
  display: flex;
  align-items: center;
}

.logo img {
  width: 100px;
  margin-right: 20px;
}

.logo h3 {
  color: var(--white);
  font-size: 28px;
}

.nav-links {
  width: 60%;
  justify-content: space-around;
  list-style: none;
  display: flex;
  align-items: center;
  transition: 0.3s;
}

.nav-link a {
  text-decoration: none;
  font-size: 20px;
  color: var(--white);
  transition: 0.3s;
}

.nav-link a:hover {
  color: var(--yellow-1);
  cursor: pointer;
}

#close {
  display: none;
}

#open {
  display: none;
}

@media only screen and (max-width: 800px) {
  nav {
    width: 100%;
    padding: 20px 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .logo img {
    width: 75px;
  }
  .logo h3 {
    font-size: 24px;
  }
  .nav-links {
    padding: 20px 0;
    flex-direction: column;
    align-items: center;
    position: absolute;
    top: -1000px;
    left: 0;
    width: 100%;
    background: var(--black);
    z-index: 1;
  }
  .nav-link {
    margin: 20px 0;
  }
  #close {
    display: flex;
  }
  #open {
    display: flex;
  }
}
</style>