<template>
  <footer>
      <h3>made by devin fledermaus with love</h3>
      <div class="social-icons">
          <a href="https://github.com/Koumori97" target="_blank">Github</a>
          <a href="https://www.linkedin.com/in/devin-fledermaus-23a091221/" target="_blank">Linkedin</a>
      </div>
  </footer>
</template>

<script>
export default {

}
</script>

<style>
footer {
    width: 100%;
    height: 50px;
    background: #000;
    display: flex;
    justify-content: center;
    align-items: center;
    text-transform: capitalize;
}

footer h3 {
    color: #fff;
}

footer .social-icons {
    position: absolute;
    right: 0;
    padding: 0 20px;
}

footer .social-icons a{
    color: #fff;
    display: inline-block;
    padding: 5px 15px;
    font-size: 1em;
    border-radius: 5px;
    margin: 0 1px;;
}
footer .social-icons a:hover {
     background: #ff275f;
}

</style>