<template>
  <About />
  <Projects />
  <Testimonials />
  <Contact />
  <Footer />
</template>

<script>
import About from '../components/About.vue'
import Projects from '../components/Projects.vue'
import Testimonials from '../components/Testimonial.vue'
import Contact from '../components/Contact.vue'
import Footer from '../components/Footer.vue'

export default {
  name: 'Home',
  components: { About, Projects, Testimonials, Contact, Footer }
}
</script>

<style>

html {
  height: 100vh;
}

section {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 600px;
    flex-direction: column;
    padding: 30px;
    background: #333;
    margin: 20px 10px;
    border-radius: 10px;
}

section h2 {
  position: relative;
  font-size: 3em;
  color: #252839;
  -webkit-text-stroke: 0.3vw #383d52;
  text-transform: uppercase;
}
section h2::before {
  content: attr(data-text);
  position: absolute;
  top: 0;
  left: 0;
  width: 0;
  height: 100%;
  color: #01fe87;
  -webkit-text-stroke: 0vw #383d52;
  border-right: 2px solid #01fe87;
  overflow: hidden;
  animation: motion 6s linear infinite;
}
@keyframes motion {
  0%,10%,100% {
    width: 0;
  }
  70%,90% {
    width: 100%;
  }
}

section .container {
  background: #fff;
  width: 70vw;
  height: 400px;
}

</style>