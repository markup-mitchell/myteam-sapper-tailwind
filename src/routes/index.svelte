<script>
	import StandardPadding from '../components/StandardPadding.svelte';
	import Subheading from '../components/Subheading.svelte';
	import Testimonial from '../components/Testimonial.svelte';
	import GetStarted from '../components/GetStarted.svelte';
	let image = "images/bg-pattern-home-2.svg";
	let image2 = "images/bg-pattern-home-1.svg";
	let image3 = "images/bg-pattern-home-3.svg";
	let image4 = "images/bg-pattern-home-4-about-3.svg";
	let image5 = "images/bg-pattern-home-5.svg";

	let person = "images/icon-person.svg";

</script>

<style>
	@media (min-width: 1024px) {
	
	:global( .spacer > *+*) {
		margin-left: 30px;
	}
}
</style>

<svelte:head>
	<title>Sapper project template</title>
</svelte:head>


<div class="flex flex-col items-center lg:items-end max-w-4xl lg:max-w-5xl mx-auto mt-20 md:mt-24 lg:mt-32">
	<img src={image2} class="absolute left-0 -ml-24 hidden xl:block" alt="">
<StandardPadding>

<div class="flex flex-col lg:flex-row justify-between h-full">
	
	<h1 class="text-white leading-none text-center sm:text-5xl md:text-6xl lg:text-7xl lg:text-left lg:w-full min-w-1/3">Find the <br /> <span class="whitespace-no-wrap">best <span class="text-p2">talent</span></span></h1>

	<div class="flex flex-col justify-between">
		<div class="hidden lg:block w-12 h-1 bg-s1"></div>
		<p class="text-white text-lg mt-5 lg:mt-0 md:mt-6 leading-relaxed text-center lg:min-w-2/3 lg:text-left lg:ml lg:max-w-2xl">
			Finding the right people and building high performing teams can be hard. Most companies aren’t tapping into the abundance of global talent. We’re about to change that.
		</p>
	</div>
</div>
</StandardPadding>		
	<img src={image} alt="" class="mx-2 mt-24 ">
</div>
<section class="bg-s4 relative overflow-hidden pt-16  md:pt-24 pb-16 md:pb-32 lg:pt-32 lg:pb-40">
	<img src={image3} alt="" class="absolute right-0 top-0 lg:top-auto lg:bottom-0 -mr-24">
	<StandardPadding>

		<div class="flex flex-col lg:flex-row lg:justify-between">
			<div class="flex items-start max-w-md lg:max-w-xs">
				<div class="flex flex-col">
					<div class="w-12 h-1 bg-p2"></div>
					<h2 class="text-white text-3xl lg:text-4xl mt-8 lg:mt-12 leading-8 lg:leading-none pr-24 sm:pr-0   ">Build &  manage distributed teams like no  one else.</h2>

				</div>
			</div>
			
			<div class="flex flex-col mt-8 lg:max-w-xl">
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
<section class="py-32 bg-s3 relative">
	<img src={image4} alt="" class="absolute top-0 left-0">
	<img src={image5} alt="" class="absolute bottom-0 right-0">
	<StandardPadding>
		
		<h2 class="text-3xl lg:text-5xl leading-none text-center text-white">
			Delivering real results for top companies. Some of our 
			<span class="text-s1">
				success stories.
			</span>
		</h2>
		<div class="spacer lg:flex justify-between">
			<Testimonial 
				quote='“The team perfectly fit the specialized skill set required. They focused on the most essential features helping us launch the platform eight months faster than planned.”'
				name="Kady Baker"
				jobTitle="Product Manager at Bookmark"
				avatar="kady"
			/>
			<Testimonial 
				quote='“We needed to automate our entire onboarding process. The team came in and built out the whole journey. Since going live, user retention has gone through the roof!”'
				name="Aiysha Reese"
				jobTitle="Founder of Manage"
				avatar="aiysha"
			/>
			<Testimonial 
				quote='“Amazing. Our team helped us build an app that delivered a new experience for hiring a physio. The launch was an instant success with 100k downloads in the first month.”'
				name="Arthur Clarke"
				jobTitle="Founder of MyPhysio"
				avatar="arthur"
			/>
	</div>
	</StandardPadding>
</section>

