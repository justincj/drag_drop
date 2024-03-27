<script>
	import { range } from 'ramda';
	const arr = range(0, 7);
</script>

<div class="chessboardStyles">
	{#each arr as rng1, key1}
		{#each arr as rng2, key2}
			{#if (rng1 + rng2) % 2}
				<div class="squareStyles" style="background-color:black" />
			{/if}
			<div class="squareStyles" />
		{/each}
	{/each}
</div>

<style>
	.chessboardStyles {
		display: grid;
		grid-template-columns: repeat(8, 1fr);
		grid-template-rows: repeat(8, 1fr);
		width: 500px;
		height: 500px;
		border: 3px solid lightgrey;
	}

	.squareStyles {
		width: 100%;
		height: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	/* .imageStyles {
		width: 45;
		height: 45;
		padding: 4;
		border-radius: 6;
		box-shadow:
			1px 3px 3px rgba(9, 30, 66, 0.25),
			0px 0px 1px rgba(9, 30, 66, 0.31);
	}
	.imageStyles:hover {
		background-color: rgba(168, 168, 168, 0.25);
	} */
</style>
