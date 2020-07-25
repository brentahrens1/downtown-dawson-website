<template>
    <div class="music">
        <h1>Catalog</h1>
        <div class="music__grid">
            <div class="music__block">
                <div class="music__block-image">
                    <img src="../assets/images/covers/cyclops.jpg">
                </div>
                <h3><a href="#">Cyclops EP</a></h3>
            </div>
            <div class="music__block">
                <div class="music__block-image">                    
                    <img src="../assets/images/covers/smolder.jpg">
                </div>
                <h3><a href="#">Smolder EP</a></h3>
            </div>
            <div class="music__block">
                <div class="music__block-image">                   
                    <img src="../assets/images/covers/clustered.jpg">
                </div>
                <h3><a href="#">Clustered Spires LP</a></h3>
            </div>
            <div class="music__block">
                <div class="music__block-image">  
                    <img src="../assets/images/covers/orare.jpg">
                </div>
                <h3><a href="#">Orare LP</a></h3>
            </div>
            <div class="music__block">
                <div class="music__block-image">  
                    <img src="../assets/images/covers/lexus.jpg">
                </div>
                <h3><a href="#">Lexus Hybrid - Single</a></h3>
            </div>
            <div class="music__block">
                <div class="music__block-image">
                    <img src="../assets/images/covers/gro.jpg">
                </div>
                <h3><a href="#">G.R.O - Single</a></h3>
            </div>
            <div class="music__block">
                <div class="music__block-image">
                    <img src="../assets/images/covers/float.jpg">
                </div>
                <h3><a href="#">Float - Single</a></h3>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "CatalogSection"
}
</script>

<style lang="scss" scoped>

    .music {
        background: #fff;
        background-size: cover;
        padding: 1rem;
        margin-top: 6rem;
        animation: fade 700ms ease-in-out;

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
        display: flex;
        flex-direction: column;
        text-align: center;
        text-transform: uppercase;
        overflow: hidden;

        .music__block-image {
            height: 100%;
            width: 100%;
            overflow: hidden;

            &:hover img {
            transform: scale(1.1);
            }

            img {
                width: 100%;
                cursor: pointer;
                transition: transform .5s ease-in-out;
            }
        }

        h3 {
            position: relative;
            
            a:link, a:visited {
                position: relative;
                display: block;
                padding: .3rem;
                z-index: 999;
                transition: all 700ms ease-in-out;

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

    @keyframes fade {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }
</style>