<template>
    <div class="music">
        <h1>Catalog</h1>
        <div class="music__grid">
            <div class="music__block">
                <img src="../assets/images/covers/cyclops.jpg">
            </div>
            <div class="music__block">
                <img src="../assets/images/covers/smolder.jpg">
            </div>
            <div class="music__block">
                <img src="../assets/images/covers/clustered.jpg">
            </div>
            <div class="music__block">
                <img src="../assets/images/covers/orare.jpg">
            </div>
            <div class="music__block">
                <img src="../assets/images/covers/lexus.jpg">
            </div>
            <div class="music__block">
                <img src="../assets/images/covers/gro.jpg">
            </div>
            <div class="music__block">
                <img src="../assets/images/covers/float.jpg">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>

    .music {
        margin-top: 6rem;
        background: orange;
        padding: 1rem;

        h1 {
            text-align: center;
            text-transform: uppercase;
            font-size: 2.5rem;
        }
    }

    .music__grid {
        width: 100%;
        height: 100%;
        padding:.5rem;
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-template-rows: repeat(auto, auto);
        grid-gap: 10px;
    }

    .music__block {
       

        img {
            width: 100%;
            cursor: pointer;
        }
    }
    
    @media (max-width: 1150px) {
        .music__grid {
            grid-template-columns: repeat(3, 1fr);
        }
    }

    @media (max-width: 750px) {
        .music__grid {
            grid-template-columns: repeat(2, 1fr);
        }
    }

</style>