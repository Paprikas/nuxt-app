<template>
  <div>
    <h1>Events</h1>
    <EventCard v-for="(event, index) in events" :key="index" :data-index="index" :event="event"/>
  </div>
</template>
<script setup>
import EventService from '../services/EventService'

const { data: events } = await EventService.getEvents()
useHead({
  title: 'Events Listing'
})
</script>
