<script>
	import StandardPadding from "../components/StandardPadding.svelte";
	import TransitionWrapper from "../components/TransitionWrapper.svelte";
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

<TransitionWrapper>
<section class="mx-auto relative overflow-hidden pt-20 pb-24">
	<div class="relative">
		<StandardPadding>
			<div class="max-w-5xl mx-auto  md:max-w-lg lg:max-w-5xl bg-p1">
				<div class="lg:flex justify-between lg:space-x-8">
					<div class="lg:whitespace-no-wrap">
						<h1 class="text-white text-center lg:text-left lg:text-6xl">
							Contact
						</h1>
						<p class="text-3xl text-p2 text-center lg:text-left">
							Ask us about
						</p>
						<div class="flex flex-col mt-10 space-y-6 text-white text-xl" >
							<div class="flex items-center">
								<img src={iconPerson} alt="" >
								<p class="ml-6">The quality of our talent network</p>
							</div>
							<div class="flex items-center">
								<img src={iconCog} alt="">
								<p class="ml-6">
									Usage & implementation <br class="sm:hidden" />of our software
								</p>
							</div>
							<div class="flex items-center">
								<img src={iconChart} alt="">
								<p class="ml-6">
										How we help drive <br class="sm:hidden" />innovation
								</p>
							</div>	
						</div>
					</div>
					<div class="mt-16 lg:mt-8 lg:w-full lg:max-w-md">
						<ContactForm/>
					</div>
				</div>

			</div>
		</StandardPadding>
		<img src={bg} alt="" class="hidden md:block lg:hidden xl:block absolute top-0 left-0 h-48 w-auto -ml-24  lg:mt-0">
	</div>
	<img src={bg2} alt="" class="absolute bottom-0 right-0 -mr-24 -mb-32 md:mb-0 lg:-mb-32 xl:mb-0 h-64 md:h-56 w-auto">
</section>
</TransitionWrapper>