<template>
    <div class="section">
        <div class="container">
            <div class="row">
                <div    
                    class="col-lg-4 col-md-6"
                    v-for="user in users"
                    :key="user.id"
                >
                    <User 
                        :name="user.name"
                        :email="user.email"
                        :address="user.address && user.address.street"
                        :phone="user.phone"
                    />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import User from '../../components/User.vue';

export default {
    components: { User },
    async asyncData ({ $axios }) {
        const response = await $axios.get('https://jsonplaceholder.typicode.com/users')
        const users = response.data
        return { users }
    }
}
</script>