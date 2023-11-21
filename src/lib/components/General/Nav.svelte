<script lang="ts">
	import Circle from '../icons/Circle.svelte';
	import Close from '../icons/Close.svelte';
	import Hamberger from '../icons/Hamberger.svelte';

	export let navItems = ['Home', 'About', 'Contact'];
	export let logo = 'logo';
	export let path = '/';

	let isNavShowing = false;
</script>

<nav
	class="fixed flex w-full justify-between bg-white p-8 text-slate-900"
	class:border-b={isNavShowing}
	class:shadow={isNavShowing}
>
	<div class:hidden={isNavShowing}>
		<Circle content={logo} />
	</div>

	<div class="md:block" class:hidden={!isNavShowing}>
		<ul class="flex gap-x-4">
			{#each navItems as navItem}
				<li>
					<a href={`${path}/${navItem}`}>{navItem}</a>
				</li>
			{/each}
		</ul>
	</div>

	<button class="text-slate-900 md:hidden" on:click={() => (isNavShowing = !isNavShowing)}>
		{#if isNavShowing}
			<Close />
		{:else}
			<Hamberger />
		{/if}
	</button>
</nav>
