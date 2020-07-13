<template>
    <div
        class="burger"
        :class="{ active: isOpen }"
        @click="$emit('click')"
    >
        <div
            class="burger__inner burger__inner--1"
        ></div>
        <div
            class="burger__inner burger__inner--2"
        ></div>
        <div
            class="burger__inner burger__inner--3"
        ></div>
    </div>
</template>

<script>
export default {
    props: {
        isOpen: {
            type: Boolean,
            default: false
        }
    }
}
</script>

<style lang="scss">
.burger {
    width: 27px;
    height: 22px;
    position: relative;
    transform: rotate(0deg);
    transition: 0.5s ease-in-out;
    cursor: pointer;
    &__inner {
        position: absolute;
        width: 27px;
        height: 3px;
        background-color: #fff;
        border-radius: 6px;
        margin-bottom: 5px;
        transform: rotate(0deg);
        transition: 0.25s ease-in-out;
        &--2 {
            top: 8px;
        }
        &--3 {
            top: 16px;
        }
    }
    &.active {
        .burger__inner {
            &--1 {
                top: 6px;
                transform: rotate(135deg);
            }
            &--2 {
                opacity: 0;
            }
            &--3 {
                top: 6px;
                transform: rotate(-135deg);
            }
        }
    }
}
</style>