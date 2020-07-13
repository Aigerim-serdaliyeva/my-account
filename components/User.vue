<template>
    <div class="user">
        <div class="user__content">
            <div class="user__name">{{ name }}</div>
            <div class="user__email">{{ email }}</div>
            <div class="user__address">{{ address }}</div>
        </div>
        <div class="user__phone">
            <img src="../assets/images/phone.png"> 
            <span>{{ phone }}</span>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        name: {
            type: String,
            default: ''
        },
        email: {
            type: String,
            default: ''
        },
        address: {
            type: String,
            default: ''
        },
        phone: {
            type: String,
            default: ''
        }
    }
}
</script>


<style lang="scss">
.user {
    background: #eaeaea;
    border-radius: 5px;
    border: 1px solid #ffffff;
    box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.15);
    overflow: hidden;
    margin: 0 auto 30px;
    max-width: 400px;
    width: 100%;

    &__content {
        padding: 10px;
    }

    &__name {
        font-size: 24px;
        color: $accent;
        border-bottom: 1px solid $accent;
        width: 100%;
        padding: 5px 0;
        margin: 0 0 15px;
    }

    &__email, &__address {
        margin-bottom: 15px;
    }

    &__phone {
        background: $accent;
        color: #ffffff;
        padding: 10px;
        display: flex;
        align-items: center;
        img {
            margin-right: 10px;
        }
    }
}

@media (max-width: 768px) {
    .user {
        &__name {
            font-size: 20px;
        }
    }
}
</style>