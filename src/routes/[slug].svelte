<script context="module">
	export async function load({ page, fetch, session, context }) {
        let counter;

		if (page.path === '/blue-counter') {
			counter = (await import('$lib/BlueCounter.svelte')).default;
		} else {
			counter = (await import('$lib/Counter.svelte')).default;
		}

		return { props: { counter, text: page.path } };
	}
</script>

<script lang="ts">
	export let counter;
	export let text;

	import '../app.css';
</script>

<main>
    <a href="/blue-counter">Blue</a>
    <a href="/red-counter">Red</a>

    <svelte:component this="{counter}" text="{text}" />
</main>
