<template>
  <div class="home">
    <Homepage />
    <MusicSection />
  </div>
</template>

<script>
import Homepage from '../components/Homepage'
import MusicSection from '../components/MusicSection'
export default {
  name: 'Home',
  components: {
    Homepage: Homepage,
    MusicSection: MusicSection
  }
}
</script>
