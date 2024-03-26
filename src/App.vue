<script>
import Header from "./components/header.vue"
import Bodyer from "./components/bodyer.vue"
import Footer from "./components/footer.vue"
import Tees from "./components/test.vue"
import Particles from "@tsparticles/vue3";
//import { loadFull } from "tsparticles"; // if you are going to use `loadFull`, install the "tsparticles" package too.
import { loadSlim } from "@tsparticles/slim"; // if you are going to use `loadSlim`, install the "@tsparticles/slim" package too.

createApp(App).use(Particles, {
  init: async engine => {
    // await loadFull(engine); // you can load the full tsParticles library from "tsparticles" if you need it
    await loadSlim(engine); // or you can load the slim version from "@tsparticles/slim" if don't need Shapes or Animations
  },
});
const particlesLoaded = async container => {
    console.log("Particles container loaded", container);
};
export default{
  data(){
    return{
      root_css:{
        height:"100vh",
        width:"100vw",
        // background:"black",
        display:"flex",
        flexDirection:"column",
        overflow: "hidden",

      },
      head_css:{
        height:"170px",
        // background:"pink",,
        width:"100%"
      },
      body_css:{
        minHeight:"400px",
        width:"100%",
        // background:"green",
        flex:"1",
        display:"flex"
      },
      foot_css:{
        height:"70px",
        width:"100%",
        background:"yellow"
      }
    }
  },
  components:{
    Header,
    Bodyer,
    Footer,
    Tees,
  }
}
</script>
<template>
  <vue-particles
            id="tsparticles"
            @particles-loaded="particlesLoaded"
            :options="{
                    background: {
                        color: {
                            value: '#0d47a1'
                        }
                    },
                    fpsLimit: 120,
                    interactivity: {
                        events: {
                            onClick: {
                                enable: true,
                                mode: 'push'
                            },
                            onHover: {
                                enable: true,
                                mode: 'repulse'
                            },
                        },
                        modes: {
                            bubble: {
                                distance: 400,
                                duration: 2,
                                opacity: 0.8,
                                size: 40
                            },
                            push: {
                                quantity: 4
                            },
                            repulse: {
                                distance: 200,
                                duration: 0.4
                            }
                        }
                    },
                    particles: {
                        color: {
                            value: '#ffffff'
                        },
                        links: {
                            color: '#ffffff',
                            distance: 150,
                            enable: true,
                            opacity: 0.5,
                            width: 1
                        },
                        move: {
                            direction: 'none',
                            enable: true,
                            outModes: 'bounce',
                            random: false,
                            speed: 6,
                            straight: false
                        },
                        number: {
                            density: {
                                enable: true,
                            },
                            value: 80
                        },
                        opacity: {
                            value: 0.5
                        },
                        shape: {
                            type: 'circle'
                        },
                        size: {
                            value: { min: 1, max: 5 }
                        }
                    },
                    detectRetina: true
                }"
        />
  <div :style="root_css">
    <div :style="head_css">
      <Header />
    </div>
    <div :style="body_css">
      <!-- <Bodyer /> -->
      <Tees />
    </div>
    <div :style="foot_css">
      <Footer />
    </div>
  </div>
</template>
<style scoped>
*{
  border:0;
  
}
</style>
