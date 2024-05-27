<template>
  <q-layout view="hHh lpR fFf">
    <Navbar />

    <q-page-container>
      <q-page padding>
        <!-- Single Carousel -->
        <Carousel :slides="carouselSlides" />

        <q-separator />

        <!-- Cards Section -->
        <div class="q-pa-md q-gutter-md row items-start">
          <ProductCard
            v-for="card in cards"
            :key="card.title"
            :title="card.title"
            :description="card.description"
            :image="card.image"
          />
        </div>
      </q-page>
    </q-page-container>

    <Footer />
  </q-layout>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Carousel from './components/Carousel.vue'
import ProductCard from './components/ProductCard.vue'
import Footer from './components/Footer.vue'

// Impor gambar-gambar lokal
import product1Image from './assets/images/product1.jpg'
import product2Image from './assets/images/product2.jpg'
import product3Image from './assets/images/product3.jpg'
import product4Image from './assets/images/product4.jpg'
import slide1 from './assets/images/slide1.jpg'
import slide2 from './assets/images/slide2.jpg'
import slide3 from './assets/images/slide3.jpg'


export default {
  components: {
    Navbar,
    Carousel,
    ProductCard,
    Footer
  },
  data () {
    return {
      carouselSlides: [
      '/images/slide1.jpg',
        '/images/slide2.jpg',
        '/images/slide3.jpg'
      ],
      cards: [
        { title: 'Arsenal -- Home Jersey 23/24', description: 'Tersedia ukuran M/L/XL', image: product1Image },
        { title: 'Barcelona Home Jersey 23/24', description: 'Tersedia ukuran M/L/XL', image: product2Image },
        { title: 'Manchester City Home Jersey 22/23', description: 'Tersedia ukuran M/L/XL', image: product3Image },
        { title: 'Real Madrid Home Jersey 23/24', description: 'Tersedia ukuran M/L/XL', image: product4Image }
      ]
    }
  }
}
</script>
