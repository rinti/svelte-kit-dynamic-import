<script lang="ts">
    export let text;
	let count = 0;

	const increment = (): void => {
		count += 1;
	};
</script>

<button on:click={increment}>
    i am {text}, clicks: {count}
</button>

<style>
	button {
		font-family: inherit;
		font-size: inherit;
		padding: 1em 2em;
		color: blue;
		background-color: rgba(0, 62, 255, 0.1);
		border-radius: 2em;
		border: 2px solid blue;
		outline: none;
		font-variant-numeric: tabular-nums;
	}

	button:hover {
		border: 3px solid blue;
	}

	button:active {
		background-color: rgba(0, 62, 255, 0.2);
	}
</style>
