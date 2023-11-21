<script>
	import Nav from '$lib/components/General/Nav.svelte';
</script>

<Nav logo={'day2'} path={'/day2'} navItems={['login', 'cookie', 'filter', 'card', 'form']} />
<div class="flex h-full flex-col items-center justify-center p-8">
	<slot />
</div>
