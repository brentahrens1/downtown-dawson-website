<template>
  <div class="homepage">
    <div class="homepage__content">
        <div class="homepage__content-cover">
            <img src="../assets/images/covers/cyclops.jpg">
        </div>
        <div class="homepage__content-info">
            <h1>Cyclops EP</h1>
            <button>Listen Now</button>
        </div>
    </div>
  </div>
</template>

<script>
export default {

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
        margin-bottom: 2rem;
        animation: fade .8s ease-in;
    }

    .homepage__content-cover {
        width: 400px;
        height: 400px;

        img {
            width: 100%;
        }
    }

    .homepage__content-info {
        text-align: center;

        h1 {
            font-size: 4rem;
            margin: 0;
            text-transform: uppercase;
            font-weight: 900;
            margin-top: .5rem;
            color: #000;
        }

        button {
            width: 15rem;
            padding: .5rem;
            background: transparent;
            border: 3px solid #000;
            font-size: 1.3rem;
            font-weight: 700;;
            text-transform: uppercase;
            cursor: pointer;
            margin-top: .5rem;
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