<script>
	import StandardPadding from "../components/StandardPadding.svelte";
	import ContactForm from "../components/ContactForm.svelte";
	let bg = "images/bg-pattern-about-2-contact-1.svg";
	let bg2 = "images/bg-pattern-contact-2.svg";
	let iconPerson = "images/icon-person.svg";
	let iconCog = "images/icon-cog.svg";
	let iconChart = "images/icon-chart.svg";
</script>

<svelte:head>
	<title>Contact</title>
</svelte:head>

<section class="mx-auto relative overflow-hidden">

	<StandardPadding>
<div class="max-w-5xl pt-20 pb-32 md:max-w-lg lg:max-w-5xl mx-auto bg-p1">

	<h1 class="text-white text-center">Contact</h1>
	<p class="text-3xl text-p2 text-center  ">
		Ask us about
	</p>
	<div class="flex flex-col mt-10 space-y-6 text-white text-xl" >

		<div class="flex items-center">
			<img src={iconPerson} alt="">
			<p class="ml-6">The quality of our talent network</p>
		</div>

		<div class="flex items-center">
			<img src={iconCog} alt="">
			<p class="ml-6">Usage & implementation <br class="sm:hidden" />of our software</p>
		</div>

	<div class="flex items-center">
		<img src={iconChart} alt="">
		<p class="ml-6">How we help drive <br class="sm:hidden" />innovation</p>
	</div>


	</div>
	<div class="mt-16">

		<ContactForm></ContactForm>
	</div>
</div>
	</StandardPadding>
	<img src={bg2} alt="" class="absolute bottom-0 right-0 -mr-24 -mb-24">
</section>