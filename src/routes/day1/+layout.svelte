<script>
	import Circle from '$lib/components/icons/Circle.svelte';
	import { page } from '$app/stores';
</script>

<div
	class="flex h-screen w-full items-center justify-center bg-gradient-to-br from-[#F3F7FF] to-[#FEE2F6] p-8"
>
	<div
		class="flex min-w-[750px] flex-col gap-4 rounded-2xl border-8 border-white bg-[#F1E2F5] p-8 text-blue-950 shadow-2xl"
	>
		<slot />
	</div>
</div>

<nav class="absolute left-0 top-0 flex w-full items-center justify-between p-6">
	<Circle />
	<ul class="flex gap-2 text-blue-950">
		<li>
			<a href="/day1/tags" class:active={$page.url.pathname === '/day1/tags'}>Tags</a>
		</li>
		<li>
			<a href="/day1/search" class:active={$page.url.pathname === '/day1/search'}>Search</a>
		</li>
		<li>
			<a href="/day1/recent" class:active={$page.url.pathname === '/day1/recent'}>Recent</a>
		</li>
	</ul>
</nav>

<style lang="postcss">
	ul li a {
		@apply relative p-1 hover:text-blue-800;
	}
	ul li a.active::after {
		content: ' ';
		@apply absolute bottom-0 left-0 h-[4px] w-full rounded-full bg-slate-400;
	}
</style>
