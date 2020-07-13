<template>
    <div class="widget">
        <div class="widget__header">
            <div class="widget__flag">
                <img :src="imgPath">
            </div>
            <h3 class="widget__title">
                {{ title }}
            </h3>
        </div>
        <div class="widget__content">
            <slot />
        </div>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
            default: ""
        },
        imgPath: {
            type: String,
            default: ''
        },
    }
}
</script>

<style lang="scss">
.widget {
    background: #eaeaea;
    border: 1px solid #fff;
    border-radius: 5px;
    box-shadow: 0px 1px 4px 0px rgba(0, 0, 0, 0.2);
    min-height: 350px;
    margin: 0 auto 30px;

    &__header {
        display: flex;
        align-items: center;
        padding: 0 10px;
    }

    &__flag {
        position: relative;
        width: 27px;
        height: 59px;
        background-image: url('../assets/images/flag.png');
        margin-right: 10px;
        top: -2px;
        img {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
    }

    &__title {
        font-size: 24px;
        color: $accent;
        border-bottom: 1px solid $accent;
        width: 100%;
        padding: 5px 0;
    }
}

@media (max-width: 768px) {
    .widget {
        min-height: 250px;
        &__title {
            font-size: 18px;
        }
    }
}
</style>