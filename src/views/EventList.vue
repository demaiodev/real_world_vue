<template>
  <div>
    <h1>Events Listing</h1>
    <EventCard :key="event.id" v-for="event in events" :event="event" />
    <BaseIcon></BaseIcon>
  </div>
</template>

<script>
import EventCard from '@/components/EventCard.vue'
import EventService from '@/services/EventService.js'
export default {
  components: {
    EventCard
  },
  data() {
    return {
      events: []
    }
  },
  created() {
    EventService.getEvents()
      .then(res => {
        this.events = res.data
        console.log(this.events)
      })
      .catch(error => console.log(error))
  }
}
</script>

<style></style>
