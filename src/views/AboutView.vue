<script setup>
import HelloWorld from '../components/HelloWorld.vue';
</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
  <div class="wrapper">
    <HelloWorld msg="You did it!" />
  </div>
</template>

<style>
.about {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
