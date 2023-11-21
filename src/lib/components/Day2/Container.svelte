<script lang="ts">
	export let color = '#abc';
	const applyColor = `bg-[${color}]`;
</script>

<div class="flex h-screen w-full items-center justify-center {applyColor}"><slot /></div>
