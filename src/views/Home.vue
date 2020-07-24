<template>
  <div class="home">
    <Homepage />
    <Video />
    <CatalogSection class="home__music" />
  </div>
</template>

<script>
import Homepage from '../components/Homepage'
import CatalogSection from '../components/CatalogSection'
import Video from '../components/Video'
export default {
  name: 'Home',
  components: {
    Homepage,
    CatalogSection,
    Video,
  }
}
</script>

<style lang="scss" scoped>
  .home__music {
    margin-top: 0;
  }
</style>
