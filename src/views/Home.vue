<template>
  <div class="home">
    <Homepage />
    <Video />
    <MusicSection class="home__music" />
  </div>
</template>

<script>
import Homepage from '../components/Homepage'
import MusicSection from '../components/MusicSection'
import Video from '..//components/Video'
export default {
  name: 'Home',
  components: {
    Homepage: Homepage,
    MusicSection: MusicSection,
    Video: Video
  }
}
</script>

<style lang="scss" scoped>
  .home__music {
    margin-top: 0;
  }
</style>
