<template>
  <li>
    <h2>{{ name }} {{ isFavorite == true ? "(Favorite)" : "" }}</h2>
    <button @click="toggleDetail">
      {{ isDetailVisible === true ? "Hide" : "Show" }} Details
    </button>
    <button @click="toggleFavorite">
      {{ isFavorite === true ? "Remove as" : "Set as" }} Favorite
    </button>
    <ul v-if="isDetailVisible">
      <li><strong>Phone:</strong>{{ phone }}</li>
      <li><strong>Email:</strong>{{ email }}</li>
    </ul>
  </li>
</template>
<script>
export default {
  props: {
    id: String,
    name: String,
    phone: String,
    email: String,
    isFavorite: Boolean,
  },
  emits: ["toggle-favorite"],
  data() {
    return {
      isDetailVisible: false,
    };
  },
  methods: {
    toggleDetail() {
      this.isDetailVisible = !this.isDetailVisible;
    },
    toggleFavorite() {
      this.$emit("toggle-favorite", this.id);
    },
  },
};
</script>
