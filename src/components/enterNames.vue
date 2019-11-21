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
				<button class="button is-link" @click="testing">Submit</button>
			</div>
			<div class="control">
				<button class="button is-link is-light">Cancel</button>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			allPlayers: null,
			playersList: []
		};
	},
	methods: {
		testing() {
			this.playersList = this.allPlayers.split("\n");
			// eslint-disable-next-line
			console.log(this.playersList);
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
