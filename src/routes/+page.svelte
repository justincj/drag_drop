<script>
	import { range } from 'ramda';
	const arr = range(0, 8);
</script>

<div class="chessboard">
	{#each arr as rng1}
		{#each arr as rng2}
			{#if (rng1 + rng2) % 2}
				<div class="square" style="background-color:black" />
			{:else}
				<div class="square" />
			{/if}
		{/each}
	{/each}
</div>

<style>
	.chessboard {
		display: grid;
		grid-template-columns: repeat(8, 1fr);
		grid-template-rows: repeat(8, 1fr);
		gap: 1px;
		width: 500px;
		height: 500px;
		border: 3px solid lightgrey;
	}

	.square {
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
