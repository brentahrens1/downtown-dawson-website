<template>
  <div class="home">
    <Homepage />
    <Video />
    <Catalog class="home__music" />
  </div>
</template>

<script>
import Homepage from '../components/Homepage'
import Catalog from '../components/Catalog'
import Video from '../components/Video'
export default {
  name: 'Home',
  components: {
    Homepage: Homepage,
    Catalog: Catalog,
    Video: Video,
  }
}
</script>

<style lang="scss" scoped>
  .home__music {
    margin-top: 0;
  }
</style>
