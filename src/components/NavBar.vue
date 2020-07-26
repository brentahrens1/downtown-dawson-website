<template>
    <div class="nav">
        <div class="nav-header">
            <router-link to="/"><h2>Downtown Dawson</h2></router-link>
        </div>
        <div class="hamburger" :class="{'open': isOpen}">
            <div class="hamburger__bar"></div>
            <div class="hamburger__bar"></div>
            <div class="hamburger__bar"></div>
        </div>
        <div class="side-drawer" :class="{'show': isOpen}">
            <ul class="side-drawer-list">
                <li @click="doClose" class="side-drawer-list__item"><router-link to="/catalog">Catalog</router-link></li>
                <li @click="doClose" class="side-drawer-list__item"><router-link to="/contact">Contact</router-link></li>
            </ul>
            <div class="socials">
                <div class="socials-icon">
                    <a href="https://www.instagram.com/downtown_dawson/" target="_blank"><img src="../assets/images/instagram-black.png"></a>
                </div>
                <div class="socials-icon">
                    <a href="https://twitter.com/lastnamedawson" target="_blank"><img src="../assets/images/twitter-black.png"></a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "NavBar",
    data() {
        return {
            isOpen: false        
        }
    },
    methods: {
        doClose() {
            this.isOpen = !this.isOpen
        },
    },
    mounted: function() {
        window.onclick = (e) => {
            if (e.target.className !== "hamburger__bar" && e.target.className !== "hamburger") {
                this.isOpen = false
            } else {
                this.isOpen = !this.isOpen
            }
        }
    }
}
</script>

<style lang="scss" scoped>
    .nav {
        width: 100%;
        height: 5rem;
        position: fixed;
        top: 0;
        left: 0;
        display: flex;
        justify-content: space-between;
        align-items: center;
        z-index: 1000;
        animation: fade .8s ease-in;
    }

    .nav-header {
        position: absolute;
        left: 1rem;

        img {
            width: 100%;
        }
    }

    .hamburger {
        width: 4rem;
        height: 2.1rem;
        position: absolute;
        right: 1rem;
        z-index: 1000;
        cursor: pointer;

        &__bar {
            width: 3rem;
            height: .3rem;
            position: absolute;
            left:0;
            background: #000;
            transition: all .50s ease-in-out;

            &:nth-child(1) {
                top: 0;
            }
            &:nth-child(2) {
                top: 12px;
            }
            &:nth-child(3) {
                top: 24px;
            }
            .open > & {
                transition: all 1s ease-in-out;
            }
            .open > &:first-child {
                top: 1rem;
                transform: rotate(50deg);
                transition: all .50s ease-in-out;
            }
            .open > &:nth-child(2) {
                opacity: 0;
                transition: all .50s ease-in-out;
            }
            .open > &:nth-child(3) {
                top: 1rem;
                transform: rotate(-410deg);
                transition: all .50s ease-in-out;
            }
        }
    }
    .side-drawer {
    height: 100%;
    width: 25rem;
    position: fixed;
    background: orange;
    top: 0;
    right:-40rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    transition: right .75s ease-in-out;
    
        .side-drawer-list {

            &__item {
                font-size: 2rem;
                text-transform: uppercase;
                padding: 15px 20px;
            }
            &__item a:hover {
                color: #fff;
            }
        }
        &.show {
            right: 0;
        }
        .socials {
            width: 50%;
            display: flex;
            position: absolute;
            justify-content: space-around;
            bottom: 2rem;
            text-transform: uppercase;

            .socials-icon {
                width: 40px;
                height: 40px;

                img {
                    width: 100%;
                }
            }
        }
    }

    @media (max-width: 650px) {
        .side-drawer {
            width: 100%;
        }

        .nav-header {
            font-size: .7rem;
        }
    }

    @keyframes fade {
        from {
            opacity: 0;
            transform: translateY(-2rem);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }
</style>