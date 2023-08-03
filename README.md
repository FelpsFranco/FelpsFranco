<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width,initial-scale=1.0" />
    <link rel="icon" href="<%= BASE_URL %>favicon.ico" />
    <title>codesandbox</title>
  </head>
  <body style="background: black;">
    <noscript>
      <strong
        >We're sorry but codesandbox doesn't work properly without JavaScript
        enabled. Please enable it to continue.</strong
      >
    </noscript>
    <div id="app">
      <template>
          <div class="hello">
            <div id="demo">
              <div id="inner-demo">
                <h1 id="inner-demo-2">
                  <br />
                </h1>
              </div>
            </div>
            <VueParticle domId="demo" :config="particleConfig" />
          </div>
      </template>
    </div>
  </body>
              <script>
import VueParticle from "vue-particlejs";
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  components: {
    VueParticle,
  },
  data() {
    return {
      particleConfig: {
        particles: {
          number: { value: 150, density: { enable: true, value_area: 500 } },
          color: { value: "#ffffff" },
          shape: {
            type: "triangle",
            stroke: { width: 0, color: "#ffffff" },
            // polygon: { nb_sides: 20 },
            image: { src: "img/github.svg", width: 100, height: 100 },
          },
          opacity: {
            value: 5,
            random: false,
            anim: { enable: false, speed: 1, opacity_min: 0.1, sync: false },
          },
          size: {
            value: 5,
            random: true,
            anim: { enable: false, speed: 150, size_min: 0.1, sync: false },
          },
          line_linked: {
            enable: true,
            distance: 100,
            color: "#ffffff",
            opacity: 0.4,
            width: 1.5,
          },
          move: {
            enable: true,
            speed: 4,
            direction: "none",
            random: false,
            straight: false,
            out_mode: "out",
            bounce: false,
            attract: { enable: false, rotateX: 600, rotateY: 1200 },
          },
        },
        interactivity: {
          detect_on: "canvas",
          events: {
            onhover: { enable: true, mode: "grab, bubble" },
            onclick: { enable: true, mode: "repulse" },
            resize: true,
          },
          modes: {
            grab: { distance: 200, line_linked: { opacity: 0.5 } },
            bubble: {
              distance: 100,
              size: 5,
              duration: 1,
              opacity: 8,
              speed: 5,
            },
            repulse: { distance: 200, duration: 0.4 },
            push: { particles_nb: 4 },
            remove: { particles_nb: 2 },
          },
        },
        retina_detect: true,
      },
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#demo {
  width: 100%;
  height: 30vh;
  background: url("") black;
}

#inner-demo {
  width: 100%;
  height: 0%;
  display: flex;
  align-items: left;
  justify-content: left;
  color: black;
  font-size: 1em;
}
#inner-demo h1 {
  position: relative;
  left: 1em;
  color: white;
  top: 0.5em;
}
</style>
</html>
