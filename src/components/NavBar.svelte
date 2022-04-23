<script>
	import '../app.css';
	import Sidebar from '/src/components/Sidebar.svelte';
let sidebar_show = false;
import { fade } from 'svelte/transition';
</script>

<nav class="z-0 grid grid-cols-2 items-center w-[100vw] h-[100px] bg-[#222] text-white/90 shadow-xl">
      <div class="left">
        <h1 class="ml-[12%] text-3xl font-black">Vite App</h1>
      </div>
      <div class="">
				<div class="md:hidden flex justify-end mr-[12%]">
				
					<button on:click={() => sidebar_show = !sidebar_show}>Toggle Sidebar</button>
          <Sidebar bind:show={sidebar_show} />
				
				</div>
       
        <div class="hidden text-white/90 md:flex justify-end mr-[12%] text-xl uppercase">
          <a class="ml-8" href="/">
          Home
          </a>
          <a class="ml-8" href="/about">
          About
          </a>
          <a class="ml-8" href="/contact">
          contact
          </a>
          <a class="ml-8" href="/blog">
           Blog
          </a>
        </div>
      </div>
</nav>

<style>
.modal-overlay {
  position: absolute;
  top: 0;
  right: 0;
	width:100vw;
	height: 100vh;
  background: rgba(0, 0, 0, 0.5);
 
  display: flex;
  flex-direction: column;
  justify-content: center;
}

</style>

