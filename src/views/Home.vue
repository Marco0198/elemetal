<template>
  <div>
 
    <nav
      class="navbar navbar-expand-lg navbar-light shadow-sm bg-light fixed-top"
    >
      <b-navbar-toggle
        class="float-right"
        target="nav-collapse"
      ></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
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
          <span class="mt-3 font-weight-bold">Kieltec</span>
        </a>

        <ul class="navbar-nav ml-auto pl-lg-4">
          <li class="nav-item px-lg-2 active">
            <a class="nav-link" href="#">
              <span class="d-inline-block d-lg-none icon-width"
                ><i class="fas fa-home"></i></span
              ><span class="ml-3">Home</span></a
            >
          </li>
          <li class="nav-item px-lg-2">
            <a class="nav-link" href="#"
              ><span class="d-inline-block d-lg-none icon-width"
                ><i class="fas fa-spa"></i></span
              ><span class="ml-3">Services</span></a
            >
          </li>
          <li class="nav-item px-lg-2">
            <a class="nav-link" href="#"
              ><span class="d-inline-block d-lg-none icon-width"
                ><i class="far fa-user"></i></span
              ><span class="ml-3">About</span></a
            >
          </li>

          <li class="nav-item px-lg-2">
            <a class="nav-link" href="#"
              ><span class="d-inline-block d-lg-none icon-width"
                ><i class="far fa-envelope"></i
              ></span>
              <span class="ml-3">Contact</span></a
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

 
<div class="row-hero">
    <video class="video" poster="../assets/video1.mp4" height="" autoplay playsinline muted loop>
      <source src="../assets/video1.mp4" type="video/webm">
    </video>
	<div class="video-quote">
    
    <div class="cointainer">
  <h2>Welcome to Kieltec Repairs</h2>
  <p>I'm here to repair</p>
</div>
  </div>
</div>
    
  </div>
  
</template>
<script>
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Source+Code+Pro:wght@300;400;500;600;700&display=swap");
html, body {
	margin: 0;
	padding: 0;
	font-family: Arial;

 
  color: #fff;
  font-family: "Poppins", sans-serif;
}

.row-hero {
  border:1px solid black;
	height: 70rem;
	width: 100%;
	position: relative;
	overflow: hidden;
	display: flex;
	justify-content: center;

}
	

.video {
	position: absolute;
	top: 50%;
	left: 50%;
	height: 1400px;
	width: auto;
  background-size:cover ;
	z-index: -1;
	transform: translateX(-50%) translateY(-80%);
	min-width: 100%;
	min-height: 100%;
}

.video-quote {

  padding-top:200px ;
  width:100%;
  height:75%;;
	color:white;
  justify-content: center;
  text-align: center;
	background-color: rgba(0, 0, 0, 0.6);
  background-size: cover;

}


.cointainer {
  padding-inline: 2em;
}
h2 {
  font-family: "Source Code Pro", monospace;
  white-space: nowrap;
  font-size: min(3rem, 7vw);
  margin-bottom: 1em;
  font-weight: 600;
  position: relative;
}
h2::before,
h2::after {
  content: "";
  position: absolute;
  inset: 0;
}
h2::before {
  background-color: whitesmoke;
  animation: typewriter 4s 1s steps(25) forwards;
  animation: name duration timing-function delay iteration-count direction
    fill-mode;
}
h2::after {
  width: 0.1em;
  background-color: #333;
  opacity: 0;
  animation: typewriter 4s 1s steps(25) forwards, blinker 500ms ease infinite;
}
p {
  font-size: 1.5rem;
  font-weight: 400;
  opacity: 0;
  transform: translateY(3em);
  animation: fader 1s ease-in 5s forwards;
}

@keyframes typewriter {
  to {
    left: 100%;
  }
}

@keyframes blinker {
  to {
    opacity: 100%;
  }
}

@keyframes fader {
  to {
    opacity: 100;
    transform: translateY(0);
  }
}
</style>
