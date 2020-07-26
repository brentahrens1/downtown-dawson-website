<template>
    <div class="video">
        <div class="hero-wrapper">
        <div class="hero">
            <video loop="loop" muted="muted" autoplay="autoplay">
                <source src="../assets/video/DawsonPromoNew.mp4"/>
            </video>
            <div class="booking-info">
                <h1>Booking</h1>
                <h2>downtowndawson@gmail.com</h2>
            </div>
        </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Video"
}
</script>

<style lang="scss" scoped>

    .hero-wrapper {
        position: relative;
        height: 100vh;
        overflow: hidden;
    }

    .hero {
        position: fixed;
        width: 100vw;
        height: 100vh;
        min-width: 100%;
        min-height: 100%;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        z-index: -999;

        .booking-info {
            position: absolute;
            top: 80%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #fff;
            text-align: center;
            
            h1 {
                font-size: 7rem;
                margin: 0;
            }

            h2 {
                font-size: 2rem;
                margin: 0;
                color: #fff;
            }
        }
    }

    video {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        max-width: 100%;
        height: 100vh;
        object-fit: cover;
    }

    @media (max-width: 800px) {

        .hero {
        .booking-info {
            h1 {
                font-size: 6.8rem;
            }

            a:link, a:visited {
                font-size: 1.5rem;
            }
        }
        }
    }

        @media (max-width: 600px) {

        .hero {
            .booking-info {
                h1 {
                    font-size: 3.5rem;
                }

                h2 {
                    font-size: 1rem; 
                }
            }
        }
    }
</style>