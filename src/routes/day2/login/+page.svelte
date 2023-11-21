<script>
	import Container from '$lib/components/Day2/Container.svelte';
	import profile from '$lib/assets/profile-unsplash.jpg';
	import Lock from '$lib/components/icons/Lock.svelte';
	import Hide from '$lib/components/icons/Hide.svelte';
	import Switch from '$lib/components/General/Switch.svelte';
</script>

<Container color={'#f6f7f8'}>
	<div
		class="mx-8 flex flex-col gap-y-8 rounded-2xl bg-white p-20 text-[#132b50] shadow-2xl md:max-w-[584px]"
	>
		<!-- title  -->
		<h1 class=" text-[32px] font-bold">Enter your password</h1>

		<!-- profile -->
		<div class=" flex items-center gap-4">
			<div
				class="h-[72px] w-[72px] rounded-full bg-cover"
				style="background-image: url({profile});"
			></div>
			<div>
				<p class="text-sm">Business Accountant</p>
				<h3 class="text-lg font-bold">Sarah Bills</h3>
			</div>
		</div>

		<!-- inputs-->
		<div>
			<h4 class="text-sm font-bold">Password</h4>
			<div class="relative flex items-center gap-4">
				<div class="pointer-events-none absolute left-3 top-3">
					<Lock />
				</div>
				<input
					type="password"
					class="flex-1 flex-grow rounded-lg border border-[#132b50] px-14 py-4"
				/>

				<div>
					<Hide />
				</div>
			</div>
		</div>
		<div class="mr-12 flex items-center justify-between">
			<div class="flex items-center gap-x-2">
				<Switch color={{ fill: 'bg-[#132b50]', stroke: 'border-[#132b50]' }} />
				<span class="font-bold">Stay signed in</span>
			</div>
			<button class="rounded-lg bg-[#132b50] p-4 font-bold text-white">Continue</button>
		</div>

		<!-- reset password  -->
		<button class="mt-8 text-left font-semibold underline">Reset password</button>
	</div>
</Container>
