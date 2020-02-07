<template>
  <div>
    <Navbar/>
    <div class="container">
      <nuxt />
    </div>
  </div>
</template>
<script>
import Navbar from '~/components/Navbar.vue'
export default {
  name: "default",
  components: {
    Navbar
  }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css?family=Roboto+Slab:400,600,800&display=swap');
body{
  font-family: 'Roboto Slab', serif;
  font-size: 20px;
  margin: 0;
  padding: 0;
}
.container{
  width: 70%;
  margin: auto;
}


/* media quireies */
@media (max-width: 320px) {
  .container{
    width: 95%;
    margin: auto
  }
}

@media (min-width: 321px ) and (max-width: 375px) {
  .container {
    width: 95%;
    margin: auto
  }
}

@media (min-width: 376px ) and (max-width: 425px) {
  .container{
    width: 95%;
    margin: auto
  }
}

@media (min-width: 426px ) and (max-width: 768px) {
  .container{
    width: 95%;
    margin: auto
  }
}

@media (min-width: 769px ) and (max-width: 1024px) {
  .container{
    width: 70%;
    margin: auto;
  }
}

@media (min-width: 1025px ) and (max-width: 1440px) {
  .container{
    width: 70%;
    margin: auto
  }
}

@media (min-width: 1441px ) and (max-width: 2560px) {
  .container{
    width: 70%;
    margin: auto
  }
}

@media (min-width: 2561px ) {
  .container{
    width: 60%;
    margin: auto
  }
}

/* font  */
@media (min-width:600px) {
  body {
    font-size: 16px;
  }
}

@media (min-width:800px) {
  body {
    font-size: 18px;
  }
}

@media (min-width:1000px) {
  body {
    /* Never get larger than this */
    font-size: 20px;
  }
}
</style>
