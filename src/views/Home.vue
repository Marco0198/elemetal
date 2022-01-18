<template>
  <div>
    <TheNavBar />
    <Home />
    <About />
    <Service />
    <Contact />
    <TheFooter />
  </div>
</template>
<script>
import TheNavBar from "@/components/layouts/TheNavBar.vue";
import Service from "@/components/Service.vue";
import Home from "@/components/Home.vue";
import Contact from "@/components/Contact.vue";
import About from "@/components/About.vue";
import TheFooter from "@/components/layouts/TheFooter.vue";
export default {
  components: { TheNavBar, Service, Contact, TheFooter, About, Home },
};
</script>


