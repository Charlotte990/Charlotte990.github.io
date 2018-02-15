<template>
  <div>

    <v-container grid-list-md text-xs-center style="height: 1000px">
    </v-container>
      <div data-aos="fade-up" data-aos-duration="3000">
      </div>
  </div>
</template>

<script>
  import AOS from 'aos'
  import 'aos/dist/aos.css'

  export default {
  create () {
    AOS.init();
    window.addEventListener('load', AOS.refresh);
    },
  }

</script>