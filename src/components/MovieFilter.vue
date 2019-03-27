<template>
  <div id="movie-filter">
    <h2>Filter Results</h2>
    <h3>By time of day</h3>
    <div class="filter-group">
      <!-- replaced by global event bus -->
      <!-- <check-filter
        category="time"
        v-for="time in times"
        v-bind:title="time"
        v-on:check-filter="checkFilter"
        v-bind:key="time"
      ></check-filter>-->
      <check-filter category="time" v-for="time in times" v-bind:title="time" v-bind:key="time"></check-filter>
    </div>
    <h3>By genre</h3>
    <div class="filter-group">
      <!-- replaced by global event bus -->
      <!-- <check-filter
        category="genre"
        v-for="genre in genres"
        v-bind:title="genre"
        v-on:check-filter="checkFilter"
        v-bind:key="genre"
      ></check-filter>-->
      <check-filter
        category="genre"
        v-for="genre in genres"
        v-bind:title="genre"
        v-bind:key="genre"
      ></check-filter>
    </div>
  </div>
</template>

<script>
import genres from "../util/genres";
import times from "../util/times";
import CheckFilter from "./CheckFilter.vue";

export default {
  data() {
    return {
      genres,
      times
    };
  },
  methods: {
    // replaced by event bus
    // checkFilter(category, title, checked) {
    //   this.$emit("check-filter", category, title, checked);
    // }
  },
  components: {
    CheckFilter
  }
};
</script>
