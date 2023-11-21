<script>
	import Circle from '$lib/components/icons/Circle.svelte';
	import { page } from '$app/stores';
	import Close from '$lib/components/icons/Close.svelte';
	import Hamberger from '$lib/components/icons/Hamberger.svelte';
	let isNavShowing = false;
</script>

<div
	class="flex h-screen w-full items-center justify-center bg-gradient-to-br from-[#F3F7FF] to-[#FEE2F6] p-8"
>
	<div class="mt-16">
		<slot />
	</div>
</div>

<nav
	class="absolute left-0 top-0 flex w-full items-start justify-between p-6 md:items-center"
	class:bg-white={isNavShowing}
>
	<a href="/day1" class:hidden={isNavShowing}>
		<Circle content={'day1'} />
	</a>

	<div class="md:block" class:hidden={!isNavShowing}>
		<ul class="flex flex-col gap-2 text-blue-950 md:flex-row">
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
	</div>

	<button on:click={() => (isNavShowing = !isNavShowing)} class="text-blue-950 md:hidden">
		{#if isNavShowing}
			<Close />
		{:else}
			<Hamberger />
		{/if}
	</button>
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
