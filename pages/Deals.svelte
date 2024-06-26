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
	class="mx-auto h-[97svh] my-auto w-[98svw] max-w-[1500px] lg:max-h-[850px] rounded-2xl glass bg-gray-100/5 border border-gray-500/50 overflow-y-scroll"
>
	<Header>
		<HeaderLink href="/">Vagas</HeaderLink>
		<HeaderLink active>Ofertas</HeaderLink>
		<HeaderLink href="/Perfil">Perfil</HeaderLink>
	</Header>
	<section
		class="grid g:grid-cols-[60%_1fr] pl-10 pr-10 gap-3 overflow-y-scroll my-auto mt-5"
	>
		<div
			class="w-full glass rounded-2xl grid grid-cols-2 gap-5 p-10 lg:gap-2 lg:p-4 lg:grid-cols-4"
		>
			<Card />
			<Card />
			<Card />
		</div>
	</section>
</div>

<Modal />
