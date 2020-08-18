<script>
	import StandardPadding from "../components/StandardPadding.svelte";
	let bg1 = "images/bg-pattern-about-1-mobile-nav-1.svg";
	let bg2 = "images/bg-pattern-about-2-contact-1.svg";
	let bg3 = "images/bg-pattern-home-4-about-3.svg";
	let bg4 = "images/bg-pattern-home-3.svg";
</script>

<svelte:head>
	<title>About</title>
</svelte:head>


<section class="relative overflow-x-hidden overflow-y-hidden">
	<div class="text-center text-white pt-20 pb-32 md:max-w-lg lg:max-w-5xl mx-auto bg-p1">
		<StandardPadding>
			<div class="xl:flex justify-between">
				<h1 class="md:text-6xl">About</h1>
				<div class="lg:flex flex-col justify-between items-center xl:items-start">
					<div class="hidden xl:block w-12 h-1 bg-p2"></div>
					<p class="mt-4 xl:mt-10 tracking-wide leading-7 xl:text-left max-w-2xl">
						We help companies build dynamic teams made up of top global talent. Using our network of passionate professionals we drive innovation and deliver incredible outcomes. Talented, diverse teams shape the best products and experiences. We’ll bring those teams to you.
					</p>
				</div>
			</div>
		</StandardPadding>
	</div>
	<img src={bg1} alt="" class="w-48 h-48 absolute bottom-0 right-0 -mb-24 md:mb-0 -mr-24">
</section>
<section class="bg-s3 relative h-64 overflow-y-hidden">
	<StandardPadding>
		<img src={bg2} alt="" class="w-48 h-48 absolute top-0 left-0 -mt-24 -ml-24">
		<img src={bg3} alt="" class="w-40 h-24 absolute bottom-0 right-0">
	</StandardPadding>
</section>
<section class="h-64 bg-s4 overflow-y-hidden relative">
	<StandardPadding>
		<img src={bg4} alt="" class="absolute top-o left-0 w-48 h-56 -ml-24 -mt-32">
	</StandardPadding>
</section>
