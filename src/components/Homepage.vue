<template>
  <div class="homepage">
    <div class="homepage__content">
        <div class="homepage__content-cover">
            <a href="http://hyperurl.co/hht8js/" target="_blank"><img src="../assets/images/covers/cyclops.jpg"></a>
        </div>
        <div class="homepage__content-info">
            <h1>Cyclops EP</h1>
            <a href="http://hyperurl.co/hht8js/" target="_blank"><button>Listen Now</button></a>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name: "Homepage"
}
</script>

<style lang="scss" scoped>
    .homepage {
        width: 100%;
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        background: #fff;
    }

    .homepage__content {
        margin-top: 8rem;
        margin-bottom: 6rem;
        animation: fade .8s ease-in;
    }

    .homepage__content-cover {
        width: 450px;
        height: 450px;

        img {
            width: 100%;
        }
    }

    .homepage__content-info {
        text-align: center;

        h1 {
            font-size: 3.8rem;
            margin: 1rem;
            margin-top: 1rem;
            font-weight: 900;
            margin-top: .5rem;
            color: #000;
        }

        button {
            font-family: 'Ramabhadra', sans-serif;
            width: 15rem;
            padding: .5rem;
            background: transparent;
            border: 3px solid #000;
            font-size: 1.3rem;
            font-weight: 700;;
            text-transform: uppercase;
            cursor: pointer;
            transition: all .3s ease-in-out;
        }
        button:hover {
            background: #000;
            color: #fff;
        }
    }

    @media (max-width: 650px) {
        .homepage__content-cover {
            width: 100%;
            height: auto;
        }

        .homepage__content-info h1 {
            font-size: 3.1rem;
        }

        .homepage__content-info button {
            width: 15rem;
        }
        .homepage__content {
            margin-bottom: 8rem;
        }
    }

    @media (min-width: 1600px) {
        .homepage__content-cover {
            width: 600px;
            height: 600px;
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