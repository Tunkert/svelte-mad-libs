<script>
	export let charName;
	export let charJob;
	export let charPlace;
	export let charAction;
	export let charLandPlace;
	export let charAnimal;
	export let charPar;
</script>

<style>
	.madlibs-container {
		max-width: 440px;
		padding: 10px 30px;
		margin: 0 auto;
	}

	.madlibs {
		margin-left: 10px;
	}

	.d-none {
		display: none;
	}
</style>

<div class="madlibs-container d-none" id="{charPar}">
	<p class="madlibs">Hi, my name is {charName}. I work as a {charJob}. My favorite place to travel to is {charPlace}. I like {charAction} on the {charLandPlace}. I like to have {charAnimal} as pets.</p>
</div>