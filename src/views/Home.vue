<template>
  <div class="home">
    <Header />
      <HeroSlide />
        <ProductSlide />
          <ProfileInsta />
            <PartnerBrand />
              <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import HeroSlide from '@/components/HeroSlide.vue'
import ProductSlide from '@/components/ProductSlide.vue'
import ProfileInsta from '@/components/ProfileInsta.vue'
import PartnerBrand from '@/components/PartnerBrand.vue'
import Footer from '@/components/Footer.vue'


export default {
  name: 'Home',
  components: {
    Header,
    HeroSlide,
    ProductSlide,
    ProfileInsta,
    PartnerBrand,
    Footer
  }
}
</script>