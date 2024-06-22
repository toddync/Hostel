<script lang="ts">
  //@ts-nocheck
  import Header from '_components/Header.svelte';
  import Card from './_components/Card.svelte';
  import Modal from './_components/Modal.svelte';
  import Nav from './_components/Nav.svelte';
  import { onMount } from 'svelte';

  // onMount(() => (document.getElementById('app').classList = 'flex inset-0'));
</script>

<div class="inset-0 absolute bg" />

<div
  class="absolute mt-[3svh] ml-[1.5svw] h-[94svh] w-[97svw] rounded-2xl
  glass bg-gray-100/5
  border border-gray-500/50"
>
  <Header />
  <Nav />
  <section class="grid grid-cols-[60svw_1fr] pl-10 pr-10 gap-3 overflow-y-scroll">
    <div class="w-full p-4 rounded-2xl grid grid-cols-3 gap-2 glass">
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
      <Card />
    </div>

    <div class="rounded-2xl glass bg-gray-100/5 border border-gray-500/50 glass p-4">
      <div class="w-full text-white flex mb-2">
        <span class="w-fit text-3xl">Latest Deals</span>
        <i class="ml-auto">See More</i>
      </div>
      <Card />
    </div>
  </section>
</div>

<Modal />
