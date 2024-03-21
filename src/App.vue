<script>
import Calendar from "./components/Calendar.vue";
import { getData } from "./data";

export default {
  components: { Calendar },
  data() {
    return {
      records: getData(),
      date: new Date(2024, 5, 10),
    };
  },
};
</script>

<template>
  <Calendar :events="records" :date="date" />
</template>
