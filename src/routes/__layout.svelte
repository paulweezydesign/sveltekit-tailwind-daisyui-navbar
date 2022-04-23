<script>
	import '../app.css';
	import Sidebar from '/src/components/Sidebar.svelte';
let sidebar_show = false;
import { fade } from 'svelte/transition';
import NavBar from '/src/components/NavBar.svelte';

</script>

<NavBar />
 

<slot />
