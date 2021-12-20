<script setup>
defineProps({
  eventInfo: {
    type: Object,
    required: true,
  },
});

import { ref } from 'vue';

// Top-level bindings are exposed to template
const event = ref({
  id: 592810,
  category: 'animal welfare',
  title: 'Cat Adoption Day',
  time: '12:00',
  date: 'January 28, 2022',
});
</script>

<template>
  <div class="event-card">
    <span>@ {{ eventInfo.time }} on {{ eventInfo.date }}</span>
    <h2>{{ eventInfo.title }}</h2>
  </div>
</template>

<style scoped>
.event-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #39495c;
  margin-bottom: 18px;
}

.event-card:hover {
  transform: scale(1.05);
  box-shadow: 0 3px 12px 0 rgba(60, 101, 46, 0.5);
}
</style>
