<template>
  <div class="LayoutDefault">
    <nav >
     <the-nav-bar></the-nav-bar>
    </nav>
    <main class="LayoutDefault__main">
      <slot/>
    </main>
    <footer >
    <the-footer></the-footer>
    </footer>
  </div>
  
</template>

<script>
 import TheNavBar from '@/components/layouts/TheNavBar.vue'
 import TheFooter from '@/components/layouts/TheFooter.vue'
export default {
 components: {TheNavBar,TheFooter},
  name: `LayoutDefault`,
 
};
</script>

<style >
.LayoutDefault__main{
  justify-content :center;
  margin-top: -50px;
  text-align: center;
  min-height:800px;
 background-attachment: fixed;

}
</style>



