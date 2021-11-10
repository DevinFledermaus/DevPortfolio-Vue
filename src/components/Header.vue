<template>
  <header>
      <img src="../assets/sugar-skull.jpg" alt="banner" class="banner">
      <a href="#" class="logo">
          <h2>DF.</h2>
      </a>
      <div class="toggle"></div>
      <nav>
          <div class="nav">
              <a href="#"><h3>Home</h3></a>
              <a href="#"><h3>About</h3></a>
              <a href="#"><h3>Projects</h3></a>
              <a href="#"><h3>Testimonials</h3></a>
          </div>
      </nav>
  </header>
</template>

<script>
export default {

}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    padding: 0 100px;
    background: #000;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    transition: 1s;
    z-index: 100;
}
header.sticky {
    height: 80px;
}

header .banner {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: 1s;
}
header.sticky .banner {
    opacity: 0.5s;
}

header .logo {
    position: absolute;
    top: 50%;
    left: -10%;
    height: 130px;
    width: 200px;
    padding: 2px;
    display: flex;
    justify-content: center;
    align-items: center;
    transform: translate(0,-50%);
    font-size: 1.1em;
    color: #fff;
    font-weight: 700;
    transition: 0.25s;
    text-decoration: none;
    z-index: 1;
    opacity: 0;
    background: transparent;
    overflow: hidden;
    border-radius: 4px;
}
.logo::before {
    content: '';
    position: absolute;
    width: 15px;
    height: 200%;
    background: linear-gradient(#0575E6, #ec4f24);
    animation: animate 4s linear infinite;
}
.logo::after {
    content: '';
    position: absolute;
    inset: 3px;
    background: rgb(22, 22, 22);
    border-radius: 10px;
}
@keyframes animate {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
    }
}

.logo h2 {
    position: relative;
    padding: 5px;
    z-index: 10;
}
header.sticky .logo {
    position: absolute;
    font-size: 1.1em;
    left: 50px;
    width: 70px;
    height: 60px;
    transform: translate(0, -50%);
    opacity: 1;
    transition-delay: 0.75s;
}

nav {
    position: relative;
    display: flex;
    z-index: 1;
}

nav .nav {
    position: relative;
    display: flex;
    transition: 0.25s;
    transform: translateX(100px);
    opacity: 0;
}
header.sticky nav .nav {
    transform: translateX(0);
    opacity: 1;
    transition: 0.75s;
}

nav .nav h3 {
    color: #fff;
    display: inline-block;
    padding: 10px 15px;
    font-size: 1.2em;
    border-radius: 5px;
    margin: 0 1px;
}

nav .nav h3:hover {
    background: #ff275f;
}

@media (max-width: 991px) {
    header {
        padding: 40px;
    }

    header.sticky .logo {
        left: 40px;
    }

    header.sticky .banner {
        opacity: 0;
    }

    nav .nav {
        display: none;
        opacity: 0;
        visibility: hidden;
    }
    nav.active .nav {
        position: fixed;
        top: 80px;
        left: 0;
        width: 100%;
        height: calc(100% - 80px);
        background: #000;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }

    header.sticky nav .nav {
        opacity: 1;
        visibility: visible;
    }

    nav .nav a {
        font-size: 1.5em;
        padding: 5px 15px;
    }
}

</style>