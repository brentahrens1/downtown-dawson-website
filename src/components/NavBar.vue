<template>
    <div class="nav">
        <div class="hamburger" :class="{'open': isOpen}" @click="isOpen = !isOpen">
            <div class="hamburger__bar"></div>
            <div class="hamburger__bar"></div>
            <div class="hamburger__bar"></div>
        </div>
        <div class="side-drawer">
            <ul class="side-drawer-list">
                <li class="side-drawer-list__item"><router-link to="/">Home</router-link></li>
                <li class="side-drawer-list__item"><router-link to="/music">Music</router-link></li>
            </ul>
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
    }
}
</script>

<style lang="scss" scoped>
    .hamburger {
        width: 4rem;
        height: 2.5rem;
        position: fixed;
        top: 1.5rem;
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
                top: 57%;
                transform: rotate(135deg);
                transition: all .50s ease-in-out;
            }
            .open > &:nth-child(2) {
                opacity: 0;
                left: -60px;
                transition: all .50s ease-in-out;
            }
            .open > &:nth-child(3) {
                transform: rotate(-135deg);
                transition: all .50s ease-in-out;
            }
        }
    }
</style>