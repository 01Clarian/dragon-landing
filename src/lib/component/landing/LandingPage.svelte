<script lang="ts">
	import Nav from './Nav.svelte';
	import NFTStoreFront from './NFTStoreFront.svelte';
	import Footer from './Footer.svelte';
</script>

<div
	class="leading-normal tracking-normal text-white gradient"
	style="font-family: 'Source Sans Pro', sans-serif;"
>
	<Nav />

	<NFTStoreFront />

	<Footer />
</div>

<style>
	.gradient {
		 background: radial-gradient(circle, #c7b513, #2f0807, #0c0520, #000)
	}
</style>
