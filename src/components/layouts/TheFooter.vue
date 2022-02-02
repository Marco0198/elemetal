<template >
  <footer class="footer px-4" style="height: 150px; background: #071c34">
    <div class="copyright text-center">© {{ year }}</div>
  </footer>
</template>
<script>
export default {
  data() {
    return {
      year: new Date().getFullYear(),
    };
  },
};
</script>
