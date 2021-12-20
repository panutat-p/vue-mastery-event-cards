<script setup>
// Values in the scope of <script setup> can also be used directly as custom component tag names
import CardItem from '../components/CardItem.vue';
import { ref } from 'vue';
import axios from 'axios';

const events = ref({});

const getEvents = async () => {
  const res = await axios.get("https://my-json-server.typicode.com/Code-Pop/Real-World_Vue-3/events")
  console.log(res.data);
  events.value = res.data
}

getEvents();

</script>

<template>
  <div class="events">
    <CardItem
      v-for="event in events"
      v-bind:key="event.id"
      v-bind:eventInfo="event"
    />
  </div>
</template>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
