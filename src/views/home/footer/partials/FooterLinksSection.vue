<template lang="">
    <div class="footer-links-section">
        <h5 class="title">{{title}}</h5>
        <ul class="footer-links-liste">
            <li v-for="(link,i) in links" :key="i" class="footer-link">
                <a :href="link.to">{{link.label}}</a>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
  name: "FooterLinksSection",
  props: ["title", "links"],
};
</script>
<style scoped>
.title {
  font-size: 24px;
  color: var(--white);
  margin-bottom: 20px;
}
.footer-links-liste {
  list-style: none;
  padding: 0;
}

.footer-link a {
  font-size: 18px;
  text-decoration: none;
  color: var(--white);
  transition: 0.3s;
}
.footer-link a:hover {
  color: var(--yellow-2);
}

@media only screen and (max-width: 1000px) {
  .footer-links-section {
    margin: 30px 0;
  }
}
</style>