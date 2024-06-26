<script lang="ts">
	//@ts-nocheck
	import Card from "$lib/Card.svelte";
	import Header from "$lib/Header.svelte";
	import HeaderLink from "$lib/HeaderLink.svelte";
	import Modal from "$lib/Modal.svelte";
	import Nav from "$lib/Nav.svelte";
</script>

<div class="inset-0 absolute bg" />

<div
	class="mx-auto my-auto h-[94svh] w-[97svw] max-w-[1500px] rounded-2xl
  glass bg-gray-100/5
  border border-gray-500/50
  overflow-y-auto"
>
	<Header>
		<HeaderLink active>Vagas</HeaderLink>
		<HeaderLink href="/Deals">Ofertas</HeaderLink>
		<HeaderLink href="Perfil">Perfil</HeaderLink>
	</Header>

	<Nav />
	<section
		class="grid g:grid-cols-[60%_1fr] pl-10 pr-10 gap-3 overflow-y-scroll my-auto"
	>
		<div
			class="w-full glass rounded-2xl
      grid grid-cols-2 gap-5 p-10 lg:gap-2 lg:p-4 lg:grid-cols-4"
		>
			<Card />
			<Card />
			<Card />
		</div>
	</section>
</div>

<Modal />
<div
	class="rounded-2xl glass bg-gray-100/5 border border-gray-500/50 glass p-4 hidden g:block"
>
	<div class="w-full text-white flex mb-2">
		<span class="w-fit text-3xl">Latest Deals</span>
		<i class="ml-auto">See More</i>
	</div>
	<Card />
</div>
