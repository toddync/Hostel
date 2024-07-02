<script lang="ts">
	//@ts-nocheck
	import { writable } from "svelte/store";
	import showRoomModal from "../stores/ShowRoomModal";
	import { pb } from "../pb";

	let data = writable({
		quarto: "",
		diaria: 40,
		detalhes: "",
		logo: {},
	});

	async function create() {
		await pb.collection("quartos").create($data);
		$showRoomModal = false;
	}
</script>

{#if $showRoomModal}
	<div
		class="absolute h-svh w-svw bg-black/20 backdrop-blur-sm flex"
		on:click={(e) => {
			e.stopPropagation();
			if (e.target != e.currentTarget) return;
			$showRoomModal = false;
		}}
	>
		<div
			class="w-2/5 h-5/6 max-h-[600px] min-w-[600px]
			bg-black/40 rounded-xl backdrop-blur-sm mx-auto mt-48 lg:my-auto border border-white/30 transition-all p-5"
		>
			<div class="size-full flex flex-col gap-5">
				<label>
					<span class="text-xl">Logo:</span>
					<input
						type="file"
						on:input={(e) => ($data.logo = e.target.files[0])}
						accept=".jpg, .png, .jpeg"
						class="bg-transparent border border-white/50
					w-full p-3 rounded-lg
					focus:outline-none"
					/>
				</label>
				<label>
					<span class="text-xl">Quarto:</span>
					<input
						type="text"
						value={$data.quarto}
						on:input={(e) => ($data.quarto = e.target.value)}
						class="bg-transparent border border-white/50
					w-full p-3 rounded-lg
					focus:outline-none"
					/>
				</label>
				<label>
					<span class="text-xl">Diaria:</span>
					<input
						type="number"
						value={$data.diaria}
						on:input={(e) => ($data.diaria = e.target.value)}
						class="bg-transparent border border-white/50
					w-full p-3 rounded-lg
					focus:outline-none"
					/>
				</label>
				<label>
					<span class="text-xl">Detalhes:</span>
					<textarea
						value={$data.detalhes}
						on:input={(e) => ($data.detalhes = e.target.value)}
						class="bg-transparent border border-white/50
					w-full h-full p-3 rounded-lg resize-none
					focus:outline-none"
					/>
				</label>
				<button
					on:click={create}
					class="p-3 rounded-sm mx-auto mt-auto w-fit border border-white/40"
				>
					+ Create
				</button>
			</div>
		</div>
	</div>
{/if}
