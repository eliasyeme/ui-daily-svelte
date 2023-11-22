<script>
	import Container from '$lib/components/Day2/Container.svelte';
	const textColor = `text-[#002167]`;
</script>

<Container color={'bg-[#C6CCE0]'}>
	<div class="flex flex-col gap-y-4 rounded-2xl bg-white p-8 md:min-w-[1134px] {textColor}">
		<div class="flex flex-col">
			<nav>
				<ul class="flex">
					<li class="active">
						<button>My parameters</button>
					</li>
					<li>
						<button>Public</button>
					</li>
					<li>
						<button>Configuration</button>
					</li>
				</ul>
			</nav>
		</div>
	</div>
</Container>

<style lang="postcss">
	ul li {
		@apply p-4 text-[#5a6793];
	}

	ul li.active {
		@apply border-b-4 border-[#002167] text-inherit;
	}
</style>
