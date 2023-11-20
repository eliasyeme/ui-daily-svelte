<script lang="ts">
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

<h1 class="mb-2 font-serif text-2xl font-bold">Tags</h1>
<div class="flex flex-wrap gap-2 md:max-w-[750px]">
	{#each tags as tag}
		<button class="rounded-xl bg-white px-4 py-2 hover:bg-blue-950 hover:text-white">
			{tag}
		</button>
	{/each}
</div>
