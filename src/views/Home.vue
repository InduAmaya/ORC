<template>
  <div id="slide">
    <b-carousel
      id="carousel-fade"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      style="text-shadow: 10% 0px 2px #000, padding: 20px"
      height="300px"
      fade
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      
      <!-- Slides with image only -->
      <b-carousel-slide height="300px" img-src="../assets/mount.jpg"></b-carousel-slide>
      <b-carousel-slide height="300px" img-src="../assets/hiking.jpg"></b-carousel-slide>
      <b-carousel-slide height="300px" img-src="../assets/rafting.jpg"></b-carousel-slide>
      <b-carousel-slide height="300px" img-src="../assets/abseiling.jpg"></b-carousel-slide>
      <b-carousel-slide height="300px" img-src="../assets/camp.jpg"></b-carousel-slide>
      
    </b-carousel>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        sliding: null
      }
    },
    methods: {
      onSlideStart() {
        this.sliding = true
      },
      onSlideEnd() {
        this.sliding = false
      }
    }
  }

</script>

<script>
// @ is an alias to /src

export default {
  name: "home",
  components: {}
};
</script>
