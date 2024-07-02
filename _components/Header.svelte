<script>
	//@ts-nocheck
	export let noPFP = false;
</script>

<section class="flex pl-10 pr-10 pt-5 w-full">
	<span class="text-xl font-extrabold accent">Santa Teresa</span>
	<div class=" mx-auto w-fit flex gap-10">
		<slot />
	</div>

	<div
		class="ml-auto w-fit flex gap-2 {noPFP &&
			'max-h-[1px] overflow-hidden'}"
	>
		<button
			on:click={() => (window.location.href = "Perfil")}
			class="p-2 rounded-full flex gap-2 bg-white/10 backdrop-blur-md border-gray-400/25 border-[1px] h-fit"
		>
			<span class="my-auto">Ryan Evans</span>
			<span class="min-w-8 min-h-8 bg-lime-400 rounded-full" />
		</button>
	</div>
</section>
<!-- <button class="mode-switch my-auto">
  <svg
    class="sun"
    fill="none"
    stroke="#fbb046"
    stroke-linecap="round"
    stroke-linejoin="round"
    stroke-width="2"
    id=" feather-sun"
    viewBox="0 0 24 24"
    ><defs /><circle cx="12" cy="12" r="5" /><path
      d="M12 1v2M12 21v2M4.22 4.22l1.42 1.42M18.36 18.36l1.42 1.42M1 12h2M21 12h2M4.22 19.78l1.42-1.42M18.36 5.64l1.42-1.42"
    /></svg
  >
  <svg
    class="moon"
    fill="none"
    stroke="#ffffff"
    stroke-linecap="round"
    stroke-linejoin="round"
    stroke-width="2"
    id=" feather-moon"
    viewBox="0 0 24 24"><defs /><path d="M21 12.79A9 9 0 1111.21 3 7 7 0 0021 12.79z" /></svg
  >
</button> -->
