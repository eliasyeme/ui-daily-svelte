<script lang="ts">
	export let color = { fill: 'bg-[#018]', stroke: 'border-[#018]' };
	let on = false;
</script>

<button
	class="flex h-9 w-[60px] items-center rounded-full border p-2 {color.stroke}"
	class:justify-end={on}
	on:click={() => (on = !on)}
>
	<div class="h-[22px] w-[22px] {color.fill} rounded-full"></div>
</button>
