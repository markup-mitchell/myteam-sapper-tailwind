<script>
	import Nav from '../components/Nav.svelte';
	import StandardPadding from '../components/StandardPadding.svelte';
	import GetStarted from '../components/GetStarted.svelte';
	export let segment;
</script>


<div class="p-6">

	<Nav {segment}/>
</div>
	
	<main class="bg-p1 w-full">
		<slot></slot>
		<aside class="bg-p2 relative">
			<StandardPadding>
		
				<GetStarted/>
			</StandardPadding>
		</aside>
	</main>
	