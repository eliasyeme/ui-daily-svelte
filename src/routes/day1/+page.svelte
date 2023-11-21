<script>
	import Recent from '$lib/components/Day1/Recent.svelte';
	import Search from '$lib/components/Day1/Search.svelte';
	import Tags from '$lib/components/Day1/Tags.svelte';
</script>

<div class="flex flex-col gap-y-8">
	<Tags />
	<Search />
	<Recent />
</div>
