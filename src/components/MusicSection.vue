<template>
    <div class="music">
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
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>

    .music {
        width: 100%;
        height: 100vh;
        margin-top: 5rem;
        background: green;
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-template-rows: repeat(auto, auto);
    }

</style>