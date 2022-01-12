<template lang="">

  <div>
   <nav
     class="navbar navbar-expand-lg  bg-dark  shadow-sm bg-light fixed-top"
    >
      <b-navbar-toggle style="color:white;" target="nav-collapse"></b-navbar-toggle>

      <b-collapse   id="nav-collapse" is-nav>
        <a class="navbar-brand d-flex align-items-center" href="#">
          <svg
            width="40px"
            version="1.1"
            id="Layer_1"
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            x="0px"
            y="0px"
            viewBox="0 0 512 512"
            style="enable-background: new 0 0 512 512"
            xml:space="preserve"
          >
            <g>
              <g>
                <path
                  d="M511.981,118.509c-0.135-2.956-1.892-5.726-4.565-7.04l-159.24-79.62c-3.776-1.887-8.363-0.64-10.664,2.898 L229.916,200.282l-55.413-85.891c-0.796-1.235-1.945-2.264-3.259-2.922l-159.24-79.62C6.582,29.138,0,33.218,0,39.268v79.621 c0,4.581,3.712,8.294,8.294,8.294c4.581,0,8.294-3.712,8.294-.294V52.687l142.652,71.326v335.32L16.587,388.008V154.277	c0-4.581-3.712-8.294-8.294-8.294c-4.581,0-8.294,3.712-8.294,8.294v238.857c0,3.142,1.775,6.013,4.585,7.418l159.24,79.62	c5.427,2.714,12.003-1.375,12.003-7.418V318.087l324.17,162.085c5.427,2.714,12.003-1.375,12.003-7.418V118.888	C512,118.76,511.987,118.636,511.981,118.509z M175.827,299.541v-152.5l145.239,225.12L175.827,299.541z M495.413,459.335
l-139.34-69.671l108.576-186.993c2.299-3.961,0.952-9.037-3.009-11.337c-3.96-2.298-9.036-0.953-11.337,3.009L344.094,377.258
L239.77,215.555L347.383,49.998l144.717,72.359l-26.387,45.446c-2.299,3.961-0.952,9.037,3.009,11.337	c3.958,2.297,9.035,0.953,11.337-3.009l15.354-26.443V459.335z"
                  fill="#000"
                />
              </g>
            </g>
          </svg>
          <span class="mt-3 font-weight-bold text-light">Kieltec</span>
        </a>

        <ul class="navbar-nav ml-auto pl-lg-4">
          <li class="nav-item px-lg-2 active">
            <a style="color:white;" class="nav-link" href="#">
              <span  class="d-inline-block d-lg-none icon-width"
                ><i  class="fas fa-home bg-light"></i></span
              ><span class="ml-3 text-light">Home</span></a
            >
          </li>
          <li class="nav-item px-lg-2">
            <a style="color:white;"  class="nav-link" href="#"
              ><span class="d-inline-block d-lg-none icon-width"
                ><i class="fas fa-spa"></i></span
              ><span class="ml-3 text-light">Services</span></a
            >
          </li>
          <li class="nav-item px-lg-2">
            <a style="color:white;" class="nav-link" href="#"
              ><span class="d-inline-block d-lg-none icon-width"
                ><i class="far fa-user"></i></span
              ><span class="ml-3 ">About</span></a
            >
          </li>

          <li class="nav-item px-lg-2">
            <a style="color:white;" class="nav-link" href="#"
              ><span class="d-inline-block d-lg-none icon-width"
                ><i  class="far fa-envelope"></i
              ></span>
              <span class="ml-3 ">Contact</span></a
            >
          </li>
        </ul>
        <ul class="navbar-nav ml-auto mt-3 mt-lg-0">
          <li class="nav-item">
            <a style="color:white;" class="nav-link" href="#">
              <i class="fab fa-twitter"></i
              ><span class="d-lg-none ml-3 ">Twitter</span>
            </a>
          </li>
          <li class="nav-item">
            <a style="color:white;" class="nav-link" href="#">
              <i class="fab fa-facebook"></i
              ><span class="d-lg-none ml-3 ">Facebook</span>
            </a>
          </li>
          <li>
            <a style="color:white;" class="nav-link" href="#">
              <i class="fab fa-instagram"></i
              ><span class="d-lg-none ml-3 ">Instagram</span>
            </a>
          </li>
          <li>
            <a style="color:white;"  class="nav-link" href="#">
              <i class="fab fa-linkedin"></i
              ><span class="d-lg-none ml-3 ">Linkedin</span>
            </a>
          </li>
        </ul>
      </b-collapse>
    </nav>
  </div>
</template>
<script>
export default {
  computed: {
    isLogin() {
      return this.$store.getters["login/isLogin"];
    },

    users() {
      return JSON.parse(localStorage.getItem("user"));
    },
  },
  methods: {
    logout() {
      this.$store.dispatch("login/logout");

      return (
        this.$store.getters["login/isLogin"],
        this.$router.push({ path: "/login" })
      );
    },
    created() {
      this.$store.dispatch("getCurrentUser");
    },
  },
};
</script>
<style >
nav {
  
  color:white;
}
</style>