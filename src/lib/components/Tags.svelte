<script>
	const tags = [
		'Blender',
		'Browser',
		'cross-platform',
		'Holo-lens',
		'Microsoft',
		'Mixed Reality',
		'modeling',
		'MR',
		'nodejs',
		'stream-socket',
		'unity',
		'unity3D',
		'unreal engine',
		'VR',
		'websocket'
	];
</script>

<div
	class="flex h-screen w-full items-center justify-center bg-gradient-to-br from-blue-200 to-pink-200"
>
	<div
		class="w-[624px] rounded-2xl border-8 border-white bg-gradient-to-br from-pink-200 to-indigo-100 p-8 text-blue-950 shadow-2xl"
	>
		<h1 class="mb-2 font-serif text-2xl font-bold">Tags</h1>
		<div class="flex flex-wrap gap-2">
			{#each tags as tag}
				<button class="rounded-xl bg-white px-4 py-2 hover:bg-blue-950 hover:text-white"
					>{tag}</button
				>
			{/each}
		</div>
	</div>
</div>
