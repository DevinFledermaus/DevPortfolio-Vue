<template>
  <section id="projects">
      <h2 data-text="Projects">Projects</h2>
      <!-- <div class="filters">
        <ul class="filter-btns">
          <li class="active" techStack="all">all</li>
          <li techStack="frontend">FrontEnd</li>
          <li techStack="backend">BackEnd</li>
        </ul>
      </div> -->
      <div class="container">
        <div class="proj proj1">
          <div class="content">
            <h4>Title 1</h4>
            <p>Description</p>
          </div>
        </div>
        <div class="proj proj2">
          <div class="content">
            <h4>Title 2</h4>
            <p>Description</p>
          </div>
        </div>
        <div class="proj proj3">
          <div class="content">
            <h4>Title 3</h4>
            <p>Description</p>
          </div>
        </div>
        <div class="proj proj4">
          <div class="content">
            <h4>Title 4</h4>
            <p>Description</p>
          </div>
        </div>
        <div class="proj proj5">
          <div class="content">
            <h4>Title 5</h4>
            <p>Description</p>
          </div>
        </div>
        <div class="proj proj6">
          <div class="content">
            <h4>Title 6</h4>
            <p>Description</p>
          </div>
        </div>
      </div>
  </section>
</template>

<script>
export default {

}
</script>

<style scoped>
section {
  background: transparent;
}

.container {
  position: relative;
  width: 800px;
  height: 500px;
  background: #222;
}

.container .proj {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  transition: 0.5s;
}

.container .proj.proj1 {
  background: #00f;
  clip-path: polygon(0 0, 5% 0, 17% 100%, 0% 100%);
}
.container .proj.proj2 {
  background: #0f0;
  clip-path: polygon(5% 0, 33% 0, 21% 100%, 17% 100%);
}
.container .proj.proj3 {
  background: #f00;
  clip-path: polygon(33% 0, 37% 0, 44% 100%, 21% 100%);
}
.container .proj.proj4 {
  background: #ff0;
  clip-path: polygon(37% 0, 77% 0, 52% 100%, 44% 100%);
}
.container .proj.proj5 {
  background: #f0f;
  clip-path: polygon(77% 0, 89% 0, 82% 100%, 52% 100%);
}
.container .proj.proj6 {
  background: url(../assets/sugar-skull.jpg);
  background-size: cover;
  clip-path: polygon(89% 0, 100% 0, 100% 100%, 82% 100%);
}

.container:hover .proj {
  clip-path: polygon(100% 0, 100% 0, 100% 100%, 100% 100%);
}
.container .proj:hover {
    clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
}

.container .proj .content {
  position: absolute;
  bottom: -100%;
  left: 0;
  width: 70%;
  padding: 20px;
  background: #fff;
  opacity: 0;
  transition: 0.5s;
}

.container .proj:hover .content {
  bottom: 0;
  opacity: 1;
}

</style>