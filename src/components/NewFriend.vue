<template>
    <form @submit.prevent="addContact">
        <div>
            <label>Name:</label>
            <input type="text" v-model="name">
        </div>
        <div>
            <label>Number:</label>
            <input type="tel" v-model="phone">
        </div>
        <div>
            <label>Email:</label>
            <input type="email" v-model="email">
        </div>
        <div>
            <button type="submit">Add Friend</button>
        </div>
    </form>
</template>
<script>
export default {
    data(){
        return {
            name:'',
            phone:'',
            email:''
        }
    },
    events: ['add-contact'],
    methods:{
        addContact(){
            this.$emit('add-contact',this.name,this.phone,this.email)
        }
    }
}
</script>