<script setup>
import { ref } from 'vue';
import StarRating from './components/StarRating.vue';

// Define categories as an array of objects
const categories = ref([
  { id: 1, name: 'Fits to my Wall', rating: 0 },
  { id: 2, name: "That's my Style", rating: 0 },
  { id: 3, name: 'Enjoy this Artist', rating: 0 },
]);

const submitRatings = () => {
  console.log('Ratings:', categories.value);
};
</script>

<template>
  <div class="min-vh-100 pa4 bg-light-gray">
    <div class="mw6 center">
      <h1 class="f3 fw5 tc mb4">Rate the Artwork</h1>
      <StarRating
        v-for="category in categories"
        :key="category.id"
        :category="category.name"
        v-model:rating="category.rating"
      />
      <button
        @click="submitRatings"
        class="db w-100 mt3 ph3 pv2 white bg-dark-gray bn br2 pointer"
      >
        Submit
      </button>
    </div>
  </div>
</template>