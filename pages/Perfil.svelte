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
	class="mx-auto my-auto h-[94svh] w-[97svw] max-w-[1500px] lg:max-h-[850px]
    rounded-2xl glass bg-gray-100/5
    border border-gray-500/50
    overflow-y-auto grid grid-rows-[2rem_1fr]"
>
	<Header noPFP>
		<HeaderLink href="/">Vagas</HeaderLink>
		<HeaderLink href="/Deals">Ofertas</HeaderLink>
		<HeaderLink active>Perfil</HeaderLink>
	</Header>

	<section class="mt-10">
		<div
			class="w-5/6 h-fit py-5 glass rounded-2xl mx-auto grid grid-cols-3 grid-rows-1"
		>
			<div
				class="bg-lime-400 rounded-full w-60 aspect-square mx-auto my-auto"
			/>
			<div class="col-span-2 p-10 grid grid-rows-1 gap-2">
				<div class="h-fit my-auto">
					<div class="flex gap-2">
						<span class="text-2xl font-extrabold">Nome:</span>
						<div class="text-xl">Ryan Evans</div>
					</div>
					<div class="flex gap-2">
						<span class="text-2xl font-extrabold">E-mail:</span>
						<div class="text-xl">ryan@gmail.com</div>
					</div>
					<div class="flex gap-2">
						<span class="text-2xl font-extrabold">CPF:</span>
						<div class="text-xl">123.456.789-00</div>
					</div>
					<div class="flex gap-2">
						<span class="text-2xl font-extrabold"
							>Nacionalidade:</span
						>
						<div class="text-xl">Brasileiro</div>
					</div>
					<div class="flex gap-2">
						<span class="text-2xl font-extrabold">Endereço:</span>
						<div class="text-xl">
							Rua das Flores, 123, Centro, Cidade
						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="glass mt-5 mx-auto w-5/6 rounded-2xl">
			<div class="text-3xl p-5">Reservas ativas:</div>
			<div></div>
		</div>
	</section>
</div>

<Modal />
