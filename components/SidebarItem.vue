<template>
    <div class="sidebar-item">
        <div class="sidebar-item__img">
            <img :src="imgPath">
        </div>
        <h3 class="sidebar-item__title">
            {{ title }}
        </h3>
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
    .sidebar-item {
        background: #eaeaea;
        border-radius: 5px;
        border: 1px solid #ffffff;
        box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.15);
        overflow: hidden;
        margin: 0 auto 30px;
        width: 100%;
        max-width: 170px;

        &__img {
            text-align: center;
        }

        &__title {
            font-size: 12px;
            font-weight: bold;
            color: #ffffff;
            background: $accent;
            padding: 10px;
        }
    }
</style>