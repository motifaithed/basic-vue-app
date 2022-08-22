<template>
  <li>
    <h2>{{ name }} {{ myFavorite == true ? '(Favorite)': '' }}</h2>
    <button @click="toggleDetail">{{isDetailVisible === true ? 'Hide' : 'Show'}}  Details</button>
    <button @click="toggleFavorite">{{myFavorite === true ? 'Remove as' : 'Set as'}}  Favorite</button>
    <ul v-if="isDetailVisible">
      <li><strong>Phone:</strong>{{ phone }}</li>
      <li><strong>Email:</strong>{{ email }}</li>
    </ul>
  </li>
</template>
<script>
export default {
    props:[
        'name', 'phone','email', 'isFavorite'
    ],
  data() {
    return {
      isDetailVisible: false,
      myFavorite: this.isFavorite
    };
  },
  methods:{
    toggleDetail(){
        this.isDetailVisible = !this.isDetailVisible;
    },
    toggleFavorite(){
        this.myFavorite = !this.myFavorite;
    }
  }
};
</script>

