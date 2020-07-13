<template>
    <div class="header">
        <div class="container">
            <div class="header__content">
                <nuxt-link 
                    class="logo"
                    to="/"
                ></nuxt-link>
                <div class="header__block">
                    <h1 class="header__title">My Account</h1>
                    <MainMenu />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import MainMenu from './MainMenu.vue';

export default {
    components: {
        MainMenu
    }
}
</script>

<style lang="scss">
    .header {
        &__content {
            display: flex;
            align-items: center;
            padding: 15px 0;
            z-index: 98;
        }

        &__block {
            width: 100%;
        }

        &__title {
            font-size: 24px;
            color: $accent;
            margin-bottom: 10px;
        }
    }
</style>