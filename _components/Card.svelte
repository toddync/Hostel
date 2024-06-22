<script lang="ts">
  //@ts-nocheck
</script>

<div class="h-fit w-full glass rounded-xl p-1 my-auto">
  <!-- svelte-ignore a11y-missing-attribute -->
  <!-- svelte-ignore a11y-click-events-have-key-events -->
  <!-- svelte-ignore a11y-no-static-element-interactions -->
  <a class="grid grid-rows-2" on:click={() => document.querySelector('#modal-window').classList.add('showModal')}>
    <div class="card-image-wrapper h-full glass !bg-black/30">
      <img alt="Hotel" />
    </div>
    <div class="my-auto h-fit w-fit pl-2 pr-2 grid">
      <div class="card-text big max-h-10 break-words text-ellipsis overflow-hidden mb-2">The Grand Canyon Hotel</div>
      <div class="card-text small">Stockton Street</div>
      <div class="card-text small">
        Starts from:
        <span class="card-price"> $1500</span>
      </div>
    </div>
  </a>
</div>
