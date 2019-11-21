<template>
	<div class="container">
		<h1 class="title is-size-1">Volleyball Rotations</h1>
		<div class="columns">
			<InputNames @playersList="generateList"/>
			<Court :playersList="this.outputData"/>
		</div>
	</div>
</template>

<script>
import InputNames from "@/components/enterNames.vue";
import Court from "@/components/court.vue";

export default {
  data() {
	return {
		outputData: "",
	};
  },
  methods: {
	  generateList(variable) {
		  this.outputData = variable;
			// eslint-disable-next-line
		console.log(this.outputData);
	  }
  },
  components: {
	InputNames,
	Court
  },
  mounted() {

  }
};
</script>

<style>
.title {
  text-decoration: underline;
}
</style>
