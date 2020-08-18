<script>
import BtnLinkContactUs from "./BtnLinkContactUs.svelte";
	let logo = "images/logo.svg";
	let close = "images/icon-close.svg";
	let menu = "images/icon-hamburger.svg";
	export let segment;
	let sidebarOpen = true;
	$: if (process.browser) document.body.classList.toggle('overflow-y-hidden', sidebarOpen)
</script>

<nav class="flex justify-between px-6 pt-12">
	<div class="mr-10">
		<a class:selected='{segment === undefined}' href='.'><img src={logo} alt=""></a>
	</div>

	
	{#if sidebarOpen}
		<div class="absolute inset-0 bg-black opacity-50 z-10"></div>
		
	<div class="absolute top-0 right-0 inset-y-0 bg-red-400 z-10 pt-12 px-6">
<div class="flex flex-col items-end">
	<button class="h-10" on:click={()=>sidebarOpen = !sidebarOpen}>
		<img src={close} alt="">
	</button>
	<ul class="text-white text-xl flex flex-col items-start w-full mt-8">
		<li ><a  href='/'>home</a></li>
		
			<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
				the blog data when we hover over the link or tap it on a touchscreen -->
				<li class="mt-6"><a rel=prefetch href='about'>about</a></li>
			</ul>
			<div class="mt-10">

				<BtnLinkContactUs/>
			</div>
		</div>
		</div>
		{/if}
	<button on:click={()=>sidebarOpen=!sidebarOpen}>
		<img src={menu} alt="">
	</button>
	</nav>
	