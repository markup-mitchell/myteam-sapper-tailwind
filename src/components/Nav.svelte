<script>
	import { sidebarOpen } from '../stores.js';

	import { fly,fade } from 'svelte/transition';
import BtnLinkContactUsLight from "./BtnLinkContactUsLight.svelte";
	export let logo;
	let close = "images/icon-close.svg";
	let menu = "images/icon-hamburger.svg";
	let bg = "images/bg-pattern-about-1-mobile-nav-1.svg";

	$: if (process.browser) document.body.classList.toggle('overflow-y-hidden', $sidebarOpen);
	$: if (process.browser) document.body.classList.toggle('fixed', $sidebarOpen);
	$: if (process.browser) document.body.classList.toggle('overflow-y-scroll', !$sidebarOpen);
</script>

<nav class="flex justify-between items-center px-6 pt-12 md:pt-16 max-w-5xl mx-auto">
	<div class="flex items-center lg:mt-2">
		<div class="mr-10">
			<img src={logo} alt="myteam">
		</div>
		<ul class="text-white text-xl hidden md:flex ">
			<li ><a  href='/' class="hover:text-p2 transition-colors duration-200">home</a></li>
			<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
				the blog data when we hover over the link or tap it on a touchscreen -->
			<li class="ml-6"><a rel=prefetch href='about' class="hover:text-p2 transition-colors duration-200">about</a></li>
		</ul>
	</div>
			<div class="hidden md:block">

				<BtnLinkContactUsLight />
			</div>
	

	
	{#if $sidebarOpen}
		<div transition:fade class="absolute inset-0 bg-black opacity-50 z-20"></div>
		
	<div
		transition:fly="{{ x: 10, duration: 400 }}" class="absolute top-0 right-0 inset-y-0 bg-s2 z-20 pt-12 pl-12 pr-6 w-64 h-screen">
		<div class="flex flex-col items-end">
			<button aria-label="Close" class="h-10" on:click={()=>$sidebarOpen = !$sidebarOpen}>
				<img src={close} alt="">
			</button>
		<nav class=" flex flex-col items-start w-full mt-8">
			<ul class="text-white text-xl">
				<li ><a  href='/'>home</a></li>
				<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
				the blog data when we hover over the link or tap it on a touchscreen -->
				<li class="mt-6"><a rel=prefetch href='about'>about</a></li>
				<li class="mt-10">
					<BtnLinkContactUsLight/>
				</li>
			</ul>
			<img src={bg} alt="" class="absolute bottom-0 right-0 -mr-24">
		</nav>
	</div>
</div>
		{/if}
	<button aria-label="Open Menu" on:click={()=> $sidebarOpen=!$sidebarOpen} class="md:hidden">
		<img src={menu} alt="">
	</button>
	</nav>
	