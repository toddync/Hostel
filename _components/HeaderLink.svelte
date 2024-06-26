<script lang="ts">
	//@ts-nocheck
	export let active = false;
	export let href = "#";
</script>

<a
	{href}
	class="hover:scale-110 transition-all hover:text-black dark:hover:text-white cursor-pointer text-sm whitespace-nowrap {(active &&
		'font-bold dark:text-white') ||
		'text-gray-400'}"><slot /></a
>
