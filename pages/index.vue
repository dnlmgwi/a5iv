<template>
  <div>
    <Navbar ref="navbar" theme="light" />
    <Home3-Header />
    <Home2LightServices />
    <Home3-Works />
    <!-- <Home3-About /> -->
    <!-- <Home3-Video /> -->
    <!-- <Home3-Team /> -->
    <!-- <Home3-Testimonials /> -->
    <!-- <Home3-News /> -->
    <Footer />
  </div>
</template>

<script>
import Home3LightServices from "../components/Home3-Light-Services/index.vue";
import Home2LightServices from "../components/Home2-Light-Services/index.vue";
export default {
  name: "Home3",
  layout: "light",
  head() {
    return {
      titleTemplate: "%s - Home",
    };
  },
  mounted() {
    document.body.classList.add("index3");
    document.body.classList.remove("index2");
    document.body.classList.remove("index4");
    var navbar = this.$refs.navbar.$el;
    if (window.pageYOffset > 300) navbar.classList.add("nav-scroll");
    else navbar.classList.remove("nav-scroll");
    window.addEventListener("scroll", () => {
      if (window.pageYOffset > 300) navbar.classList.add("nav-scroll");
      else navbar.classList.remove("nav-scroll");
    });
  },
  components: { Home3LightServices, Home2LightServices },
};
</script>
