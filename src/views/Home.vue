<template>
  <Layout name="LayoutDefault">
    <div>
     <app-accordion>

    </app-accordion>
    
    </div>
  </Layout>
</template>
<script>

//import HomePageComponent from "@/components/HomePageComponent.vue";
import Layout from "@/layouts/Layout";
import AppAccordion from "@/components/AppAccordion";

import { required, email, minLength } from "vuelidate/lib/validators";

import axios from "axios";
export default {
  components: {  Layout,AppAccordion },

  

}
</script>


