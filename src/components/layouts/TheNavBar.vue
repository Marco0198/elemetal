<template lang="">
  <div>
    <nav
      class="navbar navbar-expand-lg navbar-light shadow-sm bg-light fixed-top"
    >
      <b-navbar-toggle
        class="float-right"
        target="nav-collapse"
      ></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <a class="navbar-brand d-flex" href="#">
          <img src="@/assets/logo.jpeg" style="width: 50px" />
          <span class="mt-3 font-weight-bold">Kieltec</span>
        </a>

        <ul class="navbar-nav ml-auto pl-lg-4">
          <li class="nav-item px-lg-2 active">
            <b-nav-item class="nav-link" to="/">
              <span class="d-inline-block d-lg-none icon-width"
                ><i class="fas fa-home"></i></span
              ><span class="ml-3">Home</span>
            </b-nav-item>
          </li>
          <li class="nav-item px-lg-2">
            <b-nav-item class="nav-link scroll" to="/service"
              ><span class="d-inline-block d-lg-none icon-width"
                ><i class="fas fa-spa"></i></span
              ><span class="ml-3">Services</span></b-nav-item
            >
          </li>
          <li class="nav-item px-lg-2">
            <b-nav-item class="nav-link" to="/about"
              ><span class="d-inline-block d-lg-none icon-width"
                ><i class="far fa-user"></i></span
              ><span class="ml-3">About</span></b-nav-item
            >
          </li>

          <li class="nav-item px-lg-2">
            <b-nav-item class="nav-link" to="/contact"
              ><span class="d-inline-block d-lg-none icon-width"
                ><i class="far fa-envelope"></i
              ></span>
              <span class="ml-3">Contact</span></b-nav-item
            >
          </li>
        </ul>
        <ul class="navbar-nav ml-auto mt-3 mt-lg-0">
          <li class="nav-item">
            <a class="nav-link" href="#">
              <i class="fab fa-twitter"></i
              ><span class="d-lg-none ml-3">Twitter</span>
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">
              <i class="fab fa-facebook"></i
              ><span class="d-lg-none ml-3">Facebook</span>
            </a>
          </li>
          <li>
            <a class="nav-link" href="#">
              <i class="fab fa-instagram"></i
              ><span class="d-lg-none ml-3">Instagram</span>
            </a>
          </li>
          <li>
            <a class="nav-link" href="#">
              <i class="fab fa-linkedin"></i
              ><span class="d-lg-none ml-3">Linkedin</span>
            </a>
          </li>
        </ul>
      </b-collapse>
    </nav>
  </div>
</template>
<script>
export default {};
</script>
<style>
nav {
  color: white;
}
</style>
