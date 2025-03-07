<script setup>
import { ref, computed } from 'vue';

const props = defineProps({
  category: {
    type: String,
    required: true,
  },
  rating: {
    type: Number,
    required: true,
  },
});

const emit = defineEmits(['update:rating']);

const hoverRating = ref(0);

const setRating = (newRating) => {
  emit('update:rating', newRating); // Update parent's rating
};

const setHoverRating = (newHoverRating) => {
  hoverRating.value = newHoverRating;
};

const computedRating = computed(() => hoverRating.value || props.rating);
</script>

<template>
  <article class="mb4 pa3 bg-white br2 shadow-3" aria-labelledby="category-title">
    <h3 id="category-title" class="f5 fw6 mb3 gray">{{ category }}</h3>
    <div class="flex items-center">
      <button
        v-for="star in 5"
        :key="star"
        @click="setRating(star)"
        @mouseover="setHoverRating(star)"
        @mouseleave="setHoverRating(0)"
        class="f2 pa1 bg-transparent bn pointer"
        :class="star <= computedRating ? 'gold' : 'light-gray'"
        aria-label="Rate {{ star }} stars"
      >
        ★
      </button>
      <span class="ml2 gray fw5">{{ rating }}/5</span>
    </div>
  </article>
</template>