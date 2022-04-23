{#if show}
  <nav transition:fly={{x: 450, opacity: 1}}>
    <div class="w-[100vw] flex flex-row flex-end">
     
    <button class="text-4xl" on:click={() => {sidebar_show = false; show = false;}}>X</button>
    </div>
  </nav>
{/if}

<Modal bind:show={modal_show} />

<script>
import { fly } from 'svelte/transition';
import Modal from './Modal.svelte';
let sidebar_show = false;
export let show = false;
let modal_show = false;
</script>
		
<style>
nav {
  position: fixed;
  top: 0;
  right: 0;
  height: 100%;
  padding: 2rem 1rem 0.6rem;
  border-left: 2px solid #aaa;
  background: #fff;
  overflow-y: auto;
	width: 25rem;
  color: black;
}
</style>