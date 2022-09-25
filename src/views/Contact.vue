<template>
  <Layout name="LayoutDefault">

    <contact-page-component />

  </Layout>
</template>
<script>
import Layout from "@/layouts/Layout";
import ContactPageComponent from '../components/ContactPageComponent.vue';
export default {
  components: { Layout,ContactPageComponent },
};
</script>
