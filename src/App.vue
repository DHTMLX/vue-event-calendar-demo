<script>
import EventCalendar from "./components/EventCalendarComponent.vue";
import { getData } from "./data";

export default {
    components: { EventCalendar },
    data() {
        return {
            records: getData(),
            date: new Date(2024, 5, 10),
        };
    },
};
</script>

<template>
    <EventCalendar :events="records" :date="date" />
</template>
