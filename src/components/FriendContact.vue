<template>
  <li>
    <h2>{{ name }}</h2>
    <button @click="toggleDetail">{{isDetailVisible === true ? 'Hide' : 'Show'}}  Details</button>
    <ul v-if="isDetailVisible">
      <li><strong>Phone:</strong>{{ phone }}</li>
      <li><strong>Email:</strong>{{ email }}</li>
    </ul>
  </li>
</template>
<script>
export default {
    props:[
        'name', 'phone','email'
    ],
  data() {
    return {
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

