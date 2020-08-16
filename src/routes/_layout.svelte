<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>


<div class="p-6">

	<Nav {segment}/>
</div>
	
	<main class="bg-p1 w-full">
		<slot></slot>
	</main>