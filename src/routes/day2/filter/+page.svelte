<script>
	import Container from '$lib/components/Day2/Container.svelte';
	import Close from '$lib/components/icons/Close.svelte';
	import LeftArrow from '$lib/components/icons/LeftArrow.svelte';
	import Pencil from '$lib/components/icons/Pencil.svelte';
	import RightArrow from '$lib/components/icons/RightArrow.svelte';
	import Search from '$lib/components/icons/Search.svelte';
	import Setting from '$lib/components/icons/Setting.svelte';
	import Trash from '$lib/components/icons/Trash.svelte';
</script>

<Container color={'bg-day2FilterLightBlue'}>
	<div
		class="m-8 flex flex-col gap-y-4 rounded-2xl bg-white p-8 text-day2FilterDarkBlue shadow-2xl md:min-w-[760px]"
	>
		<div class="flex flex-col gap-y-8">
			<!-- filter header -->
			<div>
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
			</div>

			<!-- parameters  -->
			<div class="flex items-center">
				<h1 class="flex-1 flex-grow text-2xl font-bold">My parameters</h1>
				<div class="flex gap-x-2">
					<button
						class="flex items-center rounded-md border border-day2FilterLightBlue stroke-day2FilterDarkBlue p-4"
					>
						<div class="pr-2">
							<Pencil />
						</div>
						<span>Edit</span>
					</button>
					<button
						class="flex items-center rounded-md border border-day2FilterLightBlue stroke-day2FilterDarkBlue p-4"
					>
						<div class="pr-2">
							<Trash />
						</div>
						<span>Delete</span>
					</button>
					<button class="rounded-md bg-day2FilterDarkBlue p-4 font-medium text-white">
						Create parameter
					</button>
				</div>
			</div>

			<!-- input -->
			<div class="relative flex stroke-day2FilterDarkBlue">
				<input
					type="text"
					placeholder="Search"
					class="flex-1 flex-grow rounded-md border border-day2FilterLightBlue py-4 pl-14"
				/>
				<div class="absolute left-4 top-3">
					<Search />
				</div>

				<div class="flex items-center p-4">
					<LeftArrow />1<RightArrow />
				</div>
				<div class="flex items-center p-4">
					<Setting />
				</div>
			</div>
		</div>
		<!-- tags  -->
		<div class="flex gap-x-2">
			<button class="flex items-center gap-x-2 rounded-md border border-day2FilterDarkBlue p-1"
				>Name:contains:auth0 <span><Close width={22} height={22} /></span></button
			>
			<button class="flex items-center gap-x-2 rounded-md border border-day2FilterLightBlue p-2"
				>Clear filters</button
			>
		</div>
	</div>
</Container>

<style lang="postcss">
	ul li {
		@apply p-4 text-[#5a6793];
	}

	ul li.active {
		@apply border-b-4 border-day2FilterDarkBlue text-inherit;
	}
</style>
