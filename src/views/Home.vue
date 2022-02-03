<template>
  <Layout name="LayoutDefault">
    <div>
     <Home />
    <About />
    <Service />
    <Contact />
    </div>
  </Layout>
</template>
<script>
import Service from "@/components/Service.vue";
import Home from "@/components/Home.vue";
import Contact from "@/components/Contact.vue";
import About from "@/components/About.vue";
import Layout from "@/layouts/Layout";

export default {
  components: {  Service,Layout, Contact, About, Home },
};
</script>


