<template>
  <div>
    <Navbar />
    <Nuxt />
    <FooterBar />
  </div>
</template>
<script>
import Navbar from '@/components/Navbar.vue'
import FooterBar from '@/components/FooterBar.vue'

export default {
  components: {
    Navbar,
    FooterBar
  }
}
</script>