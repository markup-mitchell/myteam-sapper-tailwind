<script>
	import StandardPadding from "../components/StandardPadding.svelte";
	import Director from "../components/Director.svelte";
	import GetStarted from '../components/GetStarted.svelte';
	import ClientLogo from "../components/ClientLogo.svelte";
	import TransitionWrapper from "../components/TransitionWrapper.svelte";
	let bg1 = "images/bg-pattern-about-1-mobile-nav-1.svg";
	let bg2 = "images/bg-pattern-about-2-contact-1.svg";
	let bg3 = "images/bg-pattern-home-4-about-3.svg";
	let bg4 = "images/bg-pattern-home-3.svg";
	let twitterIcon = "images/icon-twitter.svg";
	let linkedinIcon = "images/icon-linkedin.svg";
	let cross = "images/icon-cross.svg";

	let theVerge = "images/logo-the-verge.png";
	let jakartaPost = "images/logo-jakarta-post.png";
	let theGuardian = "images/logo-the-guardian.png"
	let techRadar = "images/logo-tech-radar.png"
	let gadgetsNow = "images/logo-gadgets-now.png"

	import { onMount } from "svelte";
	import { sidebarOpen } from "../stores";
	onMount( () => $sidebarOpen = false );

</script>

<svelte:head>
	<title>Frontend Mentor | myteam website challenge - Contact</title>
</svelte:head>

<TransitionWrapper>


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

<section class="bg-s3 relative overflow-y-hidden pt-20 pb-24 lg:pb-40 text-white">
	<StandardPadding>
		<h2 class="text-center text-3xl lg:text-5xl">Meet the Directors</h2>
	
<div class="flex flex-col md:grid grid-cols-2 lg:grid-cols-3 col-gap-4 lg:col-gap-8 space-y-16 md:row-gap-20 md:space-y-0 mt-12">
	
		<Director 
		imageName="nikita"
		title="Founder & SEO"
		name="Nikita Marks"
		quote='“People demand freedom of speech as a compensation for the freedom of thought which they seldom use.“'
		/>

		<Director 
		imageName="christian"
		title="Co-founder & COO"
		name="Cristian Duncan"
		quote='“What if everything in the world were a misunderstanding, what if laughter were really tears?“'
		/>

		<Director 
		imageName="cruz"
		title="Co-founder & CTO"
		name="Cruz Hamer"
		quote='“Time is that by which at every moment all things become as nothing in our hands, and lose all true value.“'
		/>
		<Director 
		imageName="drake"
		title="Business Development Lead"
		name="Drake Heaton"
		quote='“When death is one&#39;s hope, despair is the disconsolateness of not being able to die.“'
		/>
	

		<Director 
		imageName="griffin"
		title="Lead Marketing"
		name="Griffin Wise"
		quote='“Unique perspectives shape unique products, which is what you need to survive these days.“'
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

<section class="bg-s4 overflow-y-hidden relative">
	<StandardPadding>
		
		<img src={bg4} alt="" class="absolute top-0 left-0 w-48 h-56 -ml-24 -mt-32 lg:mt-0 md:ml-0">
			<div class="py-20 md:py-24 lg:py-32 flex flex-col items-center	">
			
			<h1 class="text-center text-white text-3xl lg:text-5xl">Some of our clients</h1>
	<div class="flex flex-col md:flex-row items-center justify-between space-y-16 md:space-y-0 mt-16 md:mt-12 lg:mt-16 w-full">

		<ClientLogo 
			client="The Verge"
			imageName="the-verge"
		/>
		<ClientLogo 
			client="The Jakarta Post"
			imageName="jakarta-post"
		/>
		<ClientLogo 
			client="The Guardian"
			imageName="the-guardian"
		/>
		<ClientLogo 
			client="Techradar"
			imageName="tech-radar"
			width="w-32"
		/>
		<ClientLogo 
			client="Gadgets Now"
			imageName="gadgets-now"
			width="w-24"
		/>

	
		
	</div>
	
	
	
		</div>
	</StandardPadding>
</section>
<section class="bg-p2 relative">
	<StandardPadding>
		
		<GetStarted/>
	</StandardPadding>
</section>
</TransitionWrapper>

