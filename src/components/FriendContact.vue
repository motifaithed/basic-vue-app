<template>
  <li>
    <h2>{{ friend.name }}</h2>
    <button @click="toggleDetail">{{isDetailVisible === true ? 'Hide Details' : 'Toggle Details'}}</button>
    <ul v-if="isDetailVisible">
      <li><strong>Phone:</strong>{{ friend.phone }}</li>
      <li><strong>Email:</strong>{{ friend.email }}</li>
    </ul>
  </li>
</template>
<script>
export default {
  data() {
    return {
      friend: {
        id: "Manu",
        name: "Manuel Lorenz",
        phone: "09088952681",
        email: "manuellorenz@gmail.com",
      },
      isDetailVisible: false
    };
  },
  methods:{
    toggleDetail(){
        this.isDetailVisible = !this.isDetailVisible;
    }
  }
};
</script>
