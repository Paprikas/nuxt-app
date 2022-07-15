<template><h1>{{ event.title }}</h1></template>
<script setup>
import EventService from '../../services/EventService'

const id = useRoute().params.id

const { data: event } = await EventService.getEvent(id)

useHead({
  title: event.title,
  meta: [
    {
      hid: 'description',
      name: 'description',
      content: 'Where you you need to know about ' + event.title
    }
  ]
})

</script>
