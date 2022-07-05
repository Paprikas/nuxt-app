<template>
  <div>
    <h1>Events</h1>
    <EventCard v-for="(event, index) in events" :key="index" :data-index="index" :event="event"/>
  </div>
</template>
<script setup>
const { data: events } = await useFetch('http://localhost:3001/events')
useHead({
  title: 'Events Listing'
})
</script>
