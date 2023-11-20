<script>
	import Search from '../icons/Search.svelte';
</script>

<div class="flex justify-between gap-2">
	<div class="flex w-full">
		<div class="grid h-16 place-content-center rounded-l-xl bg-white fill-blue-950 p-4">
			<Search />
		</div>
		<input
			class="h-16 w-full rounded-r-xl py-4 placeholder:text-slate-400"
			type="text"
			placeholder="Search articles, topics, etc"
		/>
	</div>
	<button class="h-16 rounded-xl bg-blue-950 p-4 text-white hover:bg-blue-900">Search</button>
</div>
