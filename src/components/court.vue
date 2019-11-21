<template>
	<div class="column is-8 ">
        <div class="net">
            <p>This will be the net</p>
        </div>
        <div class="columns is-centered is-vcentered court">
            <div class="onCourt column is-9 ">
                <div class="columns is-multiline" > 
                    <Player v-for="index in 6" :key="index" class="onCourtPlayers is-3" :name="playersList[index - 1]"/>
                </div>
            </div>
            <div class="offCourt column">
                <div class="columns is-multiline">
                    <Player v-for="index in this.numBenchPlayers" :key="index" class="is-12" :name="playersList[index + 5]"/>
                </div>                
            </div>  
        </div>
	</div>
</template>

<script>
import Player from "@/components/player.vue";

export default {
    props: ["playersList"],
	data() {
		return {
			allPlayers: null,
            numBenchPlayers: null,
		};
	},
	methods: {
	},
	components: {
        Player,
    },
    watch: {
        playersList: function(){
            // alert(this.playersList.length);
            this.numBenchPlayers = this.playersList.length - 6;
        },
    },
	mounted() {
    }
};
</script>


<style scoped>
    .center {
        margin: 0 auto;
    }
    .net {
        /* background: red; */
        height: 7vh;
        border: solid 1px black;
        vertical-align: middle;
        text-align: center;
    }
    .court { 
        padding: 1.5rem;
    }
    .onCourt {
        border-right: solid black 1px;
    }
    .onCourtPlayers { 
        margin: 20px;
    }

</style>
