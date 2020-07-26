<template>
    <div class="footer">
        <div class="footer__contact">
            <h3>Booking Inquiries: <a href="mailto:downtowndawson@gmail.com">downtowndawson@gmail.com</a></h3>
        </div>
        <div class="footer__socials">
            <div class="footer__socials-icon">
                <a href="https://www.instagram.com/downtown_dawson/" target="_blank"><img src="../assets/images/instagram-512.png"></a>
            </div>
            <div class="footer__socials-icon">
                <a href="https://www.twitter.com/lastnamedawson" target="_blank"><img src="../assets/images/twitter-512.png"></a>
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
            font-size: 1.4rem;
        }

        &__socials {
            width: 18rem;
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

        h3 {
            margin: 0;
        }
    }

    @media (max-width: 800px) {
        .footer {
            height: 12rem;

            h3 {
                text-align: center;
            }
        }
    }
</style>