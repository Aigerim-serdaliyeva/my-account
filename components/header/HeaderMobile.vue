<template>
    <div class="header-mobile">
        <div
            class="header-mobile__menu"
            :class="{ active: isMenuShown }"
        >
            <div class="container">
                <MainMenu @onMenuSelect="closeMenu" />
            </div>
        </div>

        <div class="container">
            <div
                class="header-mobile__content"
            >
                <nuxt-link
                    to="/"
                    class="logo"
                >
                </nuxt-link>

                <Burger @click="toggleMenu" :isOpen="isMenuShown" />                
            </div>            
        </div>
    </div>
</template>

<script>
import MainMenu from './MainMenu.vue';
import Burger from './Burger.vue';

export default {
    components: { MainMenu, Burger },
    data() {
        return {
            isMenuShown: false
        };
    },
    methods: {
        toggleMenu() {
            this.isMenuShown = !this.isMenuShown;
        },
        closeMenu() {
            this.isMenuShown = false;
        }
    }
};
</script>

<style lang="scss">
.header {
    &-mobile {
        position: relative;
        z-index: 98;
        &__content {
            position: relative;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: #e3e4e4;
            padding: 10px 0;
            z-index: 1;
        }

        &__menu {
            position: absolute;
            top: 70px;
            left: 0;
            transform: translateY(-100%);
            transition: 0.4s all ease-in-out;
            height: auto;
            width: 100%;
            &.active {
                transform: translateY(0);
            }
        }
    }
}
</style>
