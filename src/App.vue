<script>
import EventCalendar from "./components/EventCalendar.vue";
import { getData } from "./data";

export default {
    components: { EventCalendar },
    data() {
        const events = getData();
        const date = new Date(2024, 5, 10);
        return { events, date};
    },
};
</script>

<template>
    <EventCalendar :events="events" :date="date" />
</template>
