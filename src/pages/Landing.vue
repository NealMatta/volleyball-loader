<template>
  <div class="container">
    <h1 class="title is-size-1">Volleyball Rotations</h1>
    <div class="columns">
      <InputNames />

      <Court />
    </div>
  </div>
</template>

<script>
import InputNames from "@/components/enterNames.vue";
import Court from "@/components/court.vue";

export default {
  data() {
    return {};
  },
  methods: {},
  components: {
    InputNames,
    Court
  },
  mounted() {}
};
</script>

<style>
.title {
  text-decoration: underline;
}
</style>
