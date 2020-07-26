<template>
  <div class="contact">
    <div class="contact__left">
      <ul class="contact__list">
        <li class="contact__list-item"><a href="https://open.spotify.com/artist/6nLgTQYfpeseVLbZ9raSW3?si=Z_kfUFJpRXyrya233uFjjw" target="_blank">Spotify</a></li>
        <li class="contact__list-item"><a href="https://music.apple.com/us/artist/downtown-dawson/1428338997" target="_blank">Apple Music</a></li>
        <li class="contact__list-item"><a href="https://downtowndawson.bandcamp.com/" target="_blank">Bandcamp</a></li>
        <li class="contact__list-item"><a href="https://soundcloud.com/lastnamedawson" target="_blank">Soundcloud</a></li>
        <li class="contact__list-item"><a href="https://www.instagram.com/downtown_dawson/" target="_blank">Instagram</a></li>
        <li class="contact__list-item"><a href="https://www.twitter.com/lastnamedawson" target="_blank">Twitter</a></li>
      </ul>
    </div>
    <div class="contact__right">
      <img src="../assets/images/dawson-street.png">
        <h5>Booking inquiries: <a href="mailto:downtowndawson@gmail.com" target="_blank">downtowndawson@gmail.com</a></h5>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Contact',
}
</script>

<style lang="scss" scoped>
  .contact {
    margin-top: 5rem;
    padding: 1rem;
    width: 100%;
    align-items: center;
    justify-content: space-around;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    text-transform: uppercase;
    animation: fade 700ms ease-in-out;
  }

  .contact__right {
    width: 40%;
    min-width: 400px;
    display: flex;
    flex-direction: column;
    text-align: center;

    img {
      width: 100%;
    }

    a {
      font-size: 1rem;
    }
  }

  .contact__left {

    font-size: 2.3rem;

    .contact__list-item {
      position: relative;
      text-align: center;

      a:link, a:visited {
        position: relative;
        display: block;
        padding: .4rem 20px;
        z-index: 999;
        transition: all 400ms ease-in-out;

        &:hover {
          color: #fff;
        }
      }

      &::after {
        content: "";
        width: 0;
        height: 100%;
        background: #000;
        position: absolute;
        top: 0;
        left: 0;
        transition: all 200ms ease-in-out;
      }

      &:hover::after {
          width: 100%;
      }
    }
  }

  @media (max-width: 700px) {
    .contact__right {
      width: 90vw;

      h5, a {
        display: none;
      }
    }
  }

  @keyframes fade {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
    }
  }
</style>
