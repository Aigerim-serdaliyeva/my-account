<template>
    <ul class="main-menu">
        <nuxt-link
            v-for="link in links"
            :key="link.text"
            class="main-menu__item"
            active-class="active"
            :to="{ path: link.to }"
            tag="li"
            exact
            @click.native="select(link)"
        >
            <a>
                {{ link.text }}
            </a>
        </nuxt-link>
    </ul>
</template>


<script>
export default {
    data() {
        return {
            links: [
                {
                    text: "Главная",
                    to: "/"
                },
                {
                    text: "О нас",
                    to: "/about"
                },
                {
                    text: "Контакты",
                    to: "/contacts"
                }
            ]
        }
    },

    methods: {
        select(link) {
            this.$emit('onMenuSelect', link)
        }
    }
}
</script>

<style lang="scss">

    .main-menu {
        margin: 0;
        padding: 0;
        list-style: none;
        border-radius: 5px;
        background-image: -moz-linear-gradient( 90deg, rgb(203,203,203) 0%, rgb(231,231,231) 100%);
        background-image: -webkit-linear-gradient( 90deg, rgb(203,203,203) 0%, rgb(231,231,231) 100%);
        background-image: -ms-linear-gradient( 90deg, rgb(203,203,203) 0%, rgb(231,231,231) 100%);
        background-image: linear-gradient( 90deg, rgb(203,203,203) 0%, rgb(231,231,231) 100%);
        box-shadow: 0px 1px 3px 0px rgba(0, 0, 0, 0.35),inset 0px 1px 0px 0px rgba(255, 255, 255, 0.004);
        display: flex;
        justify-content: space-between;
        align-items: center;
        max-width: 1057px;
        width: 100%;

        &__item {
            width: 33.333%;
            font-size: 14px;
            text-align: center;
            position: relative;
            cursor: pointer;

            &::after {
                content: "";
                position: absolute;
                width: 2px;
                height: 37px;
                background-image: url('../../assets/images/line.png');
                top: 50%;
                transform: translateY(-50%);
                right: 0;
            }

            &:last-child::after {
                display: none;
            }

            &:hover, &.active {
                background-image: linear-gradient(0deg, #cbcbcb 0%, #e7e7e7 50%, #cbcbcb 100%);
            }

            a {
                display: block;
                color: #4c4c4c; 
                text-decoration: none;
                padding: 15px 25px;
            }
        }
    }

    @media (max-width: 768px) {
        .main-menu {
            flex-direction: column;
            box-shadow: none;
            overflow: hidden;

            &__item {
                width: 100%;
                box-shadow: 0px 1px 3px 0px rgba(0, 0, 0, 0.35),inset 0px 1px 0px 0px rgba(255, 255, 255, 0.004);
                &:after {
                    display: none;
                }
                a {
                    padding: 10px 20px;
                }
            }
        }
    }

</style>