<template>
	<div class="column is-4">
		<h2 class="subtitle">Enter all Relevant Information</h2>
		<div class="field">
			<label class="label">How Many Players</label>
			<p class="subLabel">
				List the players in order with regards to the diagram
			</p>
			<div class="control">
				<textarea
					class="textarea"
					rows="10"
					type="textarea"
					v-model="allPlayers"
					placeholder="Enter players seperated by a newline"
				></textarea>
			</div>
		</div>

		<div class="field is-grouped">
			<div class="control">
				<button class="button is-link" @click="submit">Submit</button>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	// @keyup.enter="submit"
	// Can use this for instant filling

	data() {
		return {
			allPlayers: null,
			playersList: []
		};
	},
	methods: {
		submit() {
			this.playersList = this.allPlayers.split("\n");
			this.$emit("playersList", this.playersList)
			// eslint-disable-next-line
			// console.log(this.playersList);
		}
	},
	components: {},
	mounted() {}
};
</script>

<style>
.label {
	text-align: left;
	margin-bottom: 0.1em !important;
}
.subLabel {
	text-align: left;
	margin-bottom: 0.5em;
}
</style>

