<script>
	import StandardPadding from '../components/StandardPadding.svelte';
	import Subheading from '../components/Subheading.svelte';
	let image = "images/bg-pattern-home-2.svg";
	let image2 = "images/bg-pattern-home-1.svg";
	let image3 = "images/bg-pattern-home-3.svg";
	let person = "images/icon-person.svg";

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
					<h2 class="text-3xl pt-8 leading-8 pr-24 sm:pr-0 max-w-md">Build &  manage distributed teams like no  one else.</h2>

				</div>
				<img src={image3} alt="" class="absolute right-0 -mr-24">
			</div>
			<div class="flex flex-col mt-12">
				<Subheading 
					icon="person"
					heading="Experienced Individuals"
					copy="Our network is made up of highly experienced professionals who are passionate about what they do."
				/>
				<div class="mt-8">

					<Subheading 
					icon="cog"
					heading="Easy to Implement"
					copy="Our processes have been refined over years of implementation meaning our teams always deliver."
					/>
				</div>
				<div class="mt-8">

					<Subheading 
					icon="chart"
					heading="Enhanced Productivity"
					copy="Our customized platform with in-built analytics helps you manage your distributed teams."
					/>
				</div>
			</div>
		</div>
	</StandardPadding>

</section>

