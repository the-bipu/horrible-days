<script lang="ts">
	import Header from './Header.svelte';
	import '../app.css';
	import { theme } from '../stores/theme';
  	import SideBar from './SideBar.svelte';

	let { children } = $props();
</script>

<div class={`flex flex-col min-h-screen ${$theme == 'dark' ? 'bg-[#1a1a1a] text-[#eee]' : 'bg-[#eaeaea] text-[#1a1a1a]'}`}>
	<Header />

	<main class="flex-1 flex flex-col p-4 w-full bg-anime">
		{@render children()}
	</main>

	<SideBar />

	<!-- <footer class="absolute bottom-4 right-4 text-white flex flex-col justify-center items-center p-3">
		<p>
			visit <a href="https://github.com/the-bipu/">the-bipu</a> for more help.
		</p>
	</footer> -->
</div>
