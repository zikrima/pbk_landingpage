<template>
  <q-carousel
    v-model="activeSlide"
    animated
    infinite
    swipeable
    height="300px"
    :arrows="true"
    :navigation="true"
  >
    <!-- Menggunakan path relatif ke gambar di dalam direktori public/images -->
    <q-carousel-slide v-for="(slide, index) in slides" :key="index" :img-src="`/images/${slide}`" />
  </q-carousel>
</template>

<script>
export default {
  props: {
    slides: {
      type: Array,
      required: true
    }
  },
  data() {
    return {
      activeSlide: 0
    };
  }
};
</script>
