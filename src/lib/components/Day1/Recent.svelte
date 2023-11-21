<script lang="ts">
	import Container from './Container.svelte';

	const titles: Array<string> =
		" but our newbie-proof administration and simple configuration, We understand that it is better to target 'micro-efficiently', It may seem confounding to you, that's because it is, If you incentivize proactively then you may also magnetically.".split(
			','
		);
</script>

<Container>
	<h1 class="mb-2 font-serif text-2xl font-bold">Recent posts</h1>
	<div class="flex flex-col gap-2">
		{#each titles as title}
			<button
				class="truncate rounded-xl px-4 py-2 text-left font-semibold text-blue-950 hover:bg-white"
			>
				{title}
			</button>
		{/each}
	</div>
</Container>
