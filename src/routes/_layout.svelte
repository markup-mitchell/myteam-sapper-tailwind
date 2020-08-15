<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>


<div class="p-6">

	<Nav {segment}/>
</div>
	<div class="p-6 md:p-24">
	<main class="bg-p1 w-full">
		<slot></slot>
	</main>
</div>