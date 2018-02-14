<template>

  <div>
      <v-container
        style="height: 2000px"
      ></v-container>
      <div data-aos="flip-left" data-aos-duration="3000">
        <img src="v.png"/>
      </div>
</div>


</template>

<script>

import AOS from 'aos'
import 'aos/dist/aos.css'

export default {
  create () {
    AOS.init()
  }
}

</script>