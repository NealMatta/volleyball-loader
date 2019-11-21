<template>
    <div class="column">
        <div class="PlayerBox">
    	    {{ name }}
        </div>
    </div> 
</template>

<script>
export default {
    props: ['name'],
	data() {
		return {
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

<style scoped>
    .PlayerBox {
        padding: 20px;
        border: solid 1px rgb(218, 218, 218);
        border-radius: 5%;
        /* background: red; */
    }
</style>
