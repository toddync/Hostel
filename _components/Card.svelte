<script lang="ts">
  // @ts-nocheck
</script>

<div class="h-m lg:h-fit w-full glass rounded-xl p-1 my-auto">
  <!-- svelte-ignore a11y-missing-attribute -->
  <!-- svelte-ignore a11y-click-events-have-key-events -->
  <!-- svelte-ignore a11y-no-static-element-interactions -->
  <a class="grid grid-rows-2" on:click={() => document.querySelector('#modal-window').classList.add('showModal')}>
    <div class="h-36 lg:h-28 glass rounded-lg">
      <img alt="Hotel" />
    </div>
    <div class="my-auto h-fit w-fit pl-2 pr-2 grid">
      <div class="card-text big max-h-10 break-words overflow-hidden mb-2">The Grand Canyon Hotel</div>
      <div class="text-gray-300 text-sm">Stockton Street</div>
      <div class="text-gray-300 text-sm">
        Starts from:
        <span class="card-price"> $1500</span>
      </div>
    </div>
  </a>
</div>
