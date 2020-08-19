<script>
	import StandardPadding from "../components/StandardPadding.svelte";
	import Director from "../components/Director.svelte";
	let bg1 = "images/bg-pattern-about-1-mobile-nav-1.svg";
	let bg2 = "images/bg-pattern-about-2-contact-1.svg";
	let bg3 = "images/bg-pattern-home-4-about-3.svg";
	let bg4 = "images/bg-pattern-home-3.svg";
	let twitterIcon = "images/icon-twitter.svg";
	let linkedinIcon = "images/icon-linkedin.svg";
	let cross = "images/icon-cross.svg";
</script>

<svelte:head>
	<title>About</title>
</svelte:head>

<style>
	:global(.h-gap > * + *){
		margin-left: .75rem;
	}
</style>


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

<section class="bg-s3 relative overflow-y-hidden pt-20 pb-24 lg:pb-40">
	<StandardPadding>
		<h2 class="text-center text-3xl lg:text-5xl">Meet the Directors</h2>
	
<div class="grid grid-cols-2 lg:grid-cols-3 col-gap-8 row-gap-20 mt-12">
	
		<Director 
		imageName="nikita"
		title="Founder & SEO"
		name="Nikita Marks"
		/>
		<Director 
		imageName="christian"
		title="Co-founder & COO"
		name="Cristian Duncan"
		/>

	

		<Director 
		imageName="cruz"
		title="Co-founder % CTO"
		name="Cruz Hamer"
		/>
		<Director 
		imageName="drake"
		title="Business Development Lead"
		name="Drake Heaton"
		/>
	

		<Director 
		imageName="griffin"
		title="Lead Marketing"
		name="Griffin Wise"
		quote='"Unique perspectives shape unique products, which is what you need to survive these days."'
		/>
		
		<Director 
		imageName="aden"
		title="Head of Talent"
		name="Aden Allen"
		quote='“Empowered teams create truly amazing products. Set the north star and let them follow it.”'
		/>
	
</div>
		<img src={bg2} alt="" class="w-48 xl:w-56 :h-56 h-48 absolute top-0 left-0 -mt-24 -ml-24 md:mt-0 md:-ml-32">
		<img src={bg3} alt="" class="w-32 h-20 absolute bottom-0 right-0">
	</StandardPadding>
</section>
<section class="h-64 bg-s4 overflow-y-hidden relative">
	<StandardPadding>
		<img src={bg4} alt="" class="absolute top-o left-0 w-48 h-56 -ml-24 -mt-32">
	</StandardPadding>
</section>
