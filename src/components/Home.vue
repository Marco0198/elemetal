<template lang="">
  <div>
    <div class="row-hero">
      <video
        class="video"
        poster="../assets/video1.mp4"
        height=""
        autoplay
        playsinline
        muted
        loop
      >
        <source src="../assets/video1.mp4" type="video/webm" />
      </video>
      <div class="video-quote">
        <div class="home cointainer lead">
          <h2>Welcome to Kieltec</h2>
          <p>I'm here to repair</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Source+Code+Pro:wght@300;400;500;600;700&display=swap");
body {
  margin: 0;
  padding: 0;
  font-family: Arial;
  background: white;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, "Noto Sans", "Liberation Sans", sans-serif,
    "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
}

.row-hero {
  height: 50rem;
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
  background-size: cover;
  z-index: -1;
  transform: translateX(-50%) translateY(-80%);
  min-width: 100%;
  min-height: 100%;
}

.video-quote {
  padding-top: 200px;
  width: 100%;
  height: 85%;
  color: white;
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
.home p {
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
