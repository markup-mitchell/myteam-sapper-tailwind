<script>
	import StandardPadding from "../components/StandardPadding.svelte";
	let bg1 = "images/bg-pattern-about-1-mobile-nav-1.svg";
</script>

<svelte:head>
	<title>About</title>
</svelte:head>


<div class="relative">

	<div class="text-center text-white pt-20 pb-32">
		<StandardPadding>
			
			<h1>About</h1>
			<p class="mt-4 tracking-wide leading-7">
				We help companies build dynamic teams made up of top global talent. Using our network of passionate professionals we drive innovation and deliver incredible outcomes. Talented, diverse teams shape the best products and experiences. We’ll bring those teams to you.
			</p>
		</StandardPadding>
	</div>
	<img src={bg1} alt="" class="w-48 h-48 absolute bottom-0 right-0 -mb-24 -mr-24">
	
</div>
