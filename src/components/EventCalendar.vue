<script>
import { EventCalendar } from "@dhx/trial-eventcalendar";
import "@dhx/trial-eventcalendar/dist/event-calendar.css";

export default {
    props: ["events", "date"],

    mounted() {
        this.calendar = new EventCalendar(this.$refs.container, {
            events: this.events,
            date: this.date
        });
    },

    unmounted() {
        this.calendar.destructor();
    }
};
</script>

<template>
    <div ref="container" style="width: 100%; height: 100%"></div>
</template>
