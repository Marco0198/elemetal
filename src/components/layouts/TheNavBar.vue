<template lang="">
  <div>
    <nav class="navbar navbar-expand-lg navbar-light bg-light shadow-lg p-3 mb-5 bg-white rounded" >
  <div class="container-fluid">
</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav ml-auto pl-lg-4">
          <li class="nav-item px-lg-2 active">
            <b-nav-item class="nav-link" to="/">
              <span class="d-inline-block d-lg-none icon-width"
                ><i class="fas fa-home"></i></span
              ><span class="ml-3">Home</span>
            </b-nav-item>
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
    
    </div>
  </div>
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
.navbar{
  margin-bottom: 150px;

}
</style>
