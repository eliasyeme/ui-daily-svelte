<script lang="ts">
	export let color = 'bg-[#abc]';
	const applyColor = `flex h-screen w-screen items-center justify-center ${color}`;
</script>

<!-- <div class="flex h-screen w-screen items-center justify-center {applyColor}"><slot /></div> -->
<div class={applyColor}><slot /></div>
