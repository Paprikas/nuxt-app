<template><h1>Event #{{ id }}</h1></template>
<script setup>
const id = useRoute().params.id

useHead({
  title: 'Event #' + id,
  meta: [
    {
      hid: 'description',
      name: 'description',
      content: 'Where you you need to know about Event #' + id
    }
  ]
})

</script>
