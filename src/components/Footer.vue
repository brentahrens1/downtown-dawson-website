<template>
    <div class="footer">
        <div class="footer__contact">
            <h2>Booking: <a href="#">briandawson@gmail.com</a></h2>
        </div>
        <div class="footer__socials">
            <div class="footer__socials-icon">
                <a href="https://www.instagram.com/downtown_dawson/" target="_blank"><img src="../assets/images/instagram-512.png"></a>
            </div>
            <div class="footer__socials-icon">
                <a href="https://www.instagram.com/downtown_dawson/" target="_blank"><img src="../assets/images/twitter-512.png"></a>
            </div>
            <div class="footer__socials-icon">
                <a href="https://soundcloud.com/lastnamedawson" target="_blank"><img src="../assets/images/soundcloud-512.png"></a>
            </div>
            <div class="footer__socials-icon">
                <a href="https://open.spotify.com/artist/6nLgTQYfpeseVLbZ9raSW3?si=Z_kfUFJpRXyrya233uFjjw" target="_blank"><img src="../assets/images/spotify-512.png"></a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Footer'
    
}
</script>

<style lang="scss" scoped>
    .footer {
        width: 100%;
        height: 9rem;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        align-items: center;
        flex-wrap: wrap;
        background: #000;
        color: #fff;

        a:link, a:visited {
            color: #fff;
        }

        &__socials {
            width: 16rem;
            display: flex;
            justify-content: space-between;
        }

        &__socials-icon {
            width: 40px;
            height: 40px;

            img {
                width: 100%;
            }
        }

        h2 {
            margin: 0;
        }
    }

    @media (max-width: 750px) {
        .footer {
            height: 12rem;

            h2 {
                text-align: center;
            }
        }
    }
</style>