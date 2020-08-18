<script>
	import { fly,fade } from 'svelte/transition';
import BtnLinkContactUs from "./BtnLinkContactUs.svelte";
	let logo = "images/logo.svg";
	let close = "images/icon-close.svg";
	let menu = "images/icon-hamburger.svg";
	let bg = "images/bg-pattern-about-1-mobile-nav-1.svg";
	export let segment;
	let sidebarOpen = false;
	$: if (process.browser) document.body.classList.toggle('overflow-y-hidden', sidebarOpen);
	$: if (process.browser) document.body.classList.toggle('fixed', sidebarOpen);
	$: if (process.browser) document.body.classList.toggle('overflow-y-scroll', !sidebarOpen);
</script>

<nav class="flex justify-between px-6 pt-12">
	<div class="flex items-center">
		<div class="mr-10">
			<a class:selected='{segment === undefined}' href='.'><img src={logo} alt=""></a>
		</div>
		<ul class="flex text-white text-xl hidden md:flex">
			<li ><a  href='/'>home</a></li>
			<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
				the blog data when we hover over the link or tap it on a touchscreen -->
			<li class="ml-6"><a rel=prefetch href='about'>about</a></li>
		</ul>
	</div>
			<div class="hidden md:block">

				<BtnLinkContactUs/>
			</div>
	

	
	{#if sidebarOpen}
		<div transition:fade class="absolute inset-0 bg-black opacity-50 z-10"></div>
		
	<div
		transition:fly="{{ x: 10, duration: 400 }}" class="absolute top-0 right-0 inset-y-0 bg-s2 z-10 pt-12 pl-12 pr-6 w-64 h-screen">
		<div class="flex flex-col items-end">
			<button class="h-10" on:click={()=>sidebarOpen = !sidebarOpen}>
				<img src={close} alt="">
			</button>
		<div class=" flex flex-col items-start w-full mt-8">
			<ul class="text-white text-xl">
				<li ><a  href='/'>home</a></li>
				<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
				the blog data when we hover over the link or tap it on a touchscreen -->
				<li class="mt-6"><a rel=prefetch href='about'>about</a></li>
			</ul>
			<div class="mt-10">
				<BtnLinkContactUs/>
			</div>
			<img src={bg} alt="" class="absolute bottom-0 right-0 -mr-24">
		</div>
	</div>
</div>
		{/if}
	<button on:click={()=>sidebarOpen=!sidebarOpen} class="md:hidden">
		<img src={menu} alt="">
	</button>
	</nav>
	