<script lang="ts">
	//@ts-nocheck
	import showSpotModal from "../stores/ShowSpotModal";
	export let Vagas = [];
	export let Quartos = [];
</script>

<div class="cards-wrapper" style="--delay: .6s">
	<div class="cards-header">
		<div class="cards-view !block">Vagas</div>

		<button
			on:click={() => ($showSpotModal = true)}
			class="cards-button button !flex ml-auto cursor-pointer hover:scale-105 transition-all"
		>
			<svg
				viewBox="0 0 24 24"
				fill="none"
				stroke="currentColor"
				stroke-width="2"
				stroke-linecap="round"
				stroke-linejoin="round"
				class="feather feather-plus"
			>
				<path d="M12 5v14M5 12h14" />
			</svg>
			Create
		</button>
	</div>
	<div class="cards card overflow-scroll hover:scale-100">
		<table class="table">
			<colgroup>
				<!-- <col span="1" class="w-24" /> -->
				<col span="1" class="w-20" />
				<col span="1" class="w-3" />
				<col span="1" />
				<col span="1" class="w-10" />
				<col span="1" class="w-3" />
				<col span="1" class="w-14" />
			</colgroup>
			<thead>
				<tr>
					<th class="text-start">Tipo</th>

					<th />
					<th>Quarto</th>
					<th>Diária</th>
				</tr>
			</thead>
			<tbody>
				{#each $Vagas as vaga}
					<tr class="border-b border-white/40">
						<td class="flex">
							<span class="mx-auto whitespace-nowrap"
								>{vaga.tipo}</span
							>
						</td>
						<td />
						<td>
							{$Quartos.find((q) => q.id == vaga.quarto).quarto}
						</td>
						<td class="whitespace-nowrap">R$ {vaga.diaria}</td>
						<td />
						<td>
							<div class="flex gap-2">
								<button
									class="border border-white/30 hover:bg-violet-900/30 hover:border-none transition-all rounded p-1"
								>
									<svg
										xmlns="http://www.w3.org/2000/svg"
										height="24px"
										viewBox="0 -960 960 960"
										width="24px"
										fill="currentColor"
									>
										<path
											d="M240-400q-33 0-56.5-23.5T160-480q0-33 23.5-56.5T240-560q33 0 56.5 23.5T320-480q0 33-23.5 56.5T240-400Zm240 0q-33 0-56.5-23.5T400-480q0-33 23.5-56.5T480-560q33 0 56.5 23.5T560-480q0 33-23.5 56.5T480-400Zm240 0q-33 0-56.5-23.5T640-480q0-33 23.5-56.5T720-560q33 0 56.5 23.5T800-480q0 33-23.5 56.5T720-400Z"
										/>
									</svg>
								</button>
								<button
									class="border border-white/30 hover:bg-lime-400/30 hover:border-none transition-all rounded p-1"
								>
									<svg
										xmlns="http://www.w3.org/2000/svg"
										height="24px"
										viewBox="0 -960 960 960"
										width="24px"
										fill="currentColor"
										><path
											d="M200-200h57l391-391-57-57-391 391v57Zm-80 80v-170l528-527q12-11 26.5-17t30.5-6q16 0 31 6t26 18l55 56q12 11 17.5 26t5.5 30q0 16-5.5 30.5T817-647L290-120H120Zm640-584-56-56 56 56Zm-141 85-28-29 57 57-29-28Z"
										/></svg
									>
								</button>
								<button
									class="border border-white/30 hover:bg-red-900/30 hover:border-none transition-all rounded p-1"
								>
									<svg
										xmlns="http://www.w3.org/2000/svg"
										height="24px"
										viewBox="0 -960 960 960"
										width="24px"
										fill="currentColor"
										><path
											d="M280-120q-33 0-56.5-23.5T200-200v-520h-40v-80h200v-40h240v40h200v80h-40v520q0 33-23.5 56.5T680-120H280Zm400-600H280v520h400v-520ZM360-280h80v-360h-80v360Zm160 0h80v-360h-80v360ZM280-720v520-520Z"
										/></svg
									>
								</button>
							</div>
						</td>
					</tr>
				{/each}
			</tbody>
		</table>
	</div>
</div>
