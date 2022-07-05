<template><h1>{{ event.title }}</h1></template>
<script setup>
const id = useRoute().params.id

const { data: event } = await useFetch('http://localhost:3001/events/' + id)

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
