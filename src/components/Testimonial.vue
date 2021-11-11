<template>
  <section id="testimonials">
      <h2 data-text="Testimonials">Testimonials</h2>
      <h3>Stories</h3>
      <div class="container">
        <div class="card-container active">
          <div class="card">
            <div class="content">
              <h4>Jason Wandrag</h4>
              <q>Quote</q>
              <p>Lecturer</p>
            </div>
            <img src="../assets/JasonW.png" alt="pic">
          </div>
        </div>
        <div class="card-container">
          <div class="card">
            <div class="content">
              <h4>Thapelo Tsotetsi</h4>
              <q>Quote</q>
              <p>Lecturer</p>
            </div>
            <img src="../assets/Thapelo.png" alt="pic">
          </div>
        </div>
        <div class="card-container">
          <div class="card">
            <div class="content">
              <h4>Naeemah Davis</h4>
              <q>Quote</q>
              <p>Peer</p>
            </div>
            <img src="../assets/Nae.png" alt="pic">
          </div>
        </div>
        <div class="card-container">
          <div class="card">
            <div class="content">
              <h4>Abdur-Razaaq Jardien</h4>
              <q>Quote</q>
              <p>Peer</p>
            </div>
            <img src="../assets/Abdur.png" alt="pic">
          </div>
        </div>
        <div class="card-container">
          <div class="card">
            <div class="content">
              <h4>Nasar Kamish</h4>
              <q>Quote</q>
              <p>Peer</p>
            </div>
            <img src="../assets/Nasar.png" alt="pic">
          </div>
        </div>
        <div class="card-container">
          <div class="card">
            <div class="content">
              <h4>Shuaib Dollie</h4>
              <q>Quote</q>
              <p>Peer</p>
            </div>
            <img src="../assets/Shuaib.png" alt="pic">
          </div>
        </div>
        <div class="card-container">
          <div class="card">
            <div class="content">
              <h4>Yamkela Mathontsi</h4>
              <q>Quote</q>
              <p>Peer</p>
            </div>
            <img src="../assets/Yamkela.png" alt="pic">
          </div>
        </div>

        <div id="next" @click="next()"></div>
        <div id="prev" @click="prev()"></div>

      </div>
  </section>
</template>

<script>

export default {
  setup() {
    const cards = document.querySelectorAll('.card-container');
    const index = 0;

    const next = () => {
      console.log('hi', cards[index]);
      cards[index].classList.remove('active');
      index = (index - 1) % cards.length;
      cards[index].classList.add('active');
    }

    const prev = () => {
      console.log('bye');
      cards[index].classList.remove('active');
      index = (index - 1 + cards.length);
      cards[index].classList.add('active');
    }

    return { next, prev }
  }
}
</script>

<style scoped>
section {
    border-radius: 10px;
    background: #e0e0e0;
    box-shadow: inset 12px 12px 20px #5a5a5a,
                inset -12px -12px 20px #ffffff;
}

.container {
  position: relative;
  perspective: 1000px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  margin: auto 7px;
}

.container .card {
  position: relative;
  width: 600px;
  height: 350px;
  margin: 20px;
  margin-top: 80px;
  display: flex;
  transition: 0.5s;
  justify-content: flex-start;
  align-items: center;
  background: linear-gradient(45deg,#1a2f3f,#7094ce);
}

.container .card img {
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  height: 300px;
  transition: 0.5s;
}

.container .card:hover img {
  left: 80%;
  height: 450px;
}

.container .card .content {
  position: relative;
  width: 50%;
  left: 20%;
  padding: 20px 20px 20px 40px;
  opacity: 0;
  visibility: hidden;
  transition: 0.5s;
}

.container .card:hover .content {
  left: 0;
  opacity: 1;
  visibility: visible;
}

.container .card .content h4 {
  color: #fff;
  text-transform: capitalize;
  font-size: 2.2em;
  line-height: 1em;
}

.container .card .content q {
  color: #fff;
}

.container .card .content p {
  color: #fff;
  font-weight: 700;
  text-transform: uppercase;
}

.container .card-container {
  display: none;
  position: absolute;
  bottom: 0;
}

.container .card-container.active {
  display: flex;
}

.container #next,
.container #prev {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  height: 50px;
  width: 50px;
  line-height: 50px;
  text-align: center;
  font-size: 20px;
  background: #fff;
  color: #333;
  cursor: pointer;
  border-radius: 50%;
  box-shadow: 0 5px 10px #3337;
}

.container #next {
  right: -70px;
}

.container #prev {
  left: -70px;
}



@media (max-width: 991px) { 
    .container .card {
        width: auto;
        max-width: 600px;
        align-items: flex-start;
    }

    .container .card:hover {
        height: 600px;
    }

    .container .card:hover img {
        left: 50%;
        height: 350px;
    }

    .container .card .content {
        width: 100%;
        left: 0;
        padding: 40px;
    }
}

@media (max-width: 767px) {
    .container {
        flex-direction: column;
    }

    .container .card {
        margin: 40px 20px;
    }
}

@media (max-width: 420px) {
    .container .card .content {
        padding: 30px;
    }

    .container .card:hover img {
        height: 300px;
    }
}

</style>