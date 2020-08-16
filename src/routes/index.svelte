<script>
	import StandardPadding from '../components/StandardPadding.svelte';
	let image = "images/bg-pattern-home-2.svg";
	let image2 = "images/bg-pattern-home-1.svg";
	let image3 = "images/bg-pattern-home-3.svg";

</script>

<svelte:head>
	<title>Sapper project template</title>
</svelte:head>


<div class="flex flex-col items-center lg:items-end max-w-4xl lg:max-w-5xl mx-auto mt-20 md:mt-24 lg:mt-32">
	<img src={image2} class="absolute left-0 -ml-24 hidden xl:block" alt="">
<StandardPadding>

<div class="flex flex-col lg:flex-row justify-between lg:items-end">
	
	<h1 class="leading-none text-center lg:text-left md:text-6xl lg:w-full lg:text-7xl min-w-1/3">Find the <br /> <span class="whitespace-no-wrap">best <span class="text-p2">talent</span></span></h1>
	<p class="text-white text-lg mt-5 lg:mt-0 md:mt-6 leading-relaxed text-center lg:min-w-2/3 lg:text-left lg:ml lg:max-w-2xl">
		Finding the right people and building high performing teams can be hard. Most companies aren’t tapping into the abundance of global talent. We’re about to change that.
	</p>
</div>
</StandardPadding>		
	<img src={image} alt="" class="mx-2 mt-24 ">
</div>
<section class="bg-s4 relative overflow-hidden">
	<StandardPadding>

		<div class="flex flex-col">
			<div class="flex items-start">
				<div class="flex flex-col pt-16">
					<div class="w-12 h-1 bg-p2"></div>
					<h2 class="text-3xl pt-8 leading-8 max-w-xs sm:max-w-lg">Build & <br class="sm:hidden"/> manage <br class="sm:hidden"/>distributed <br class="sm:hidden"/>teams like no  <br class="sm:hidden"/>one else.</h2>

				</div>
				<img src={image3} alt="" class="absolute right-0 -mr-24">
			</div>
			<div class="flex flex-col">
				<p>media</p>
				<p>media</p>
				<p>media</p>
				
			</div>
		</div>
	</StandardPadding>

</section>

