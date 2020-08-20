<script>
	import Nav from '../components/Nav.svelte';
	import StandardPadding from '../components/StandardPadding.svelte';
	import GetStarted from '../components/GetStarted.svelte';
	let logo = "images/logo.svg";
	let facebook = "images/icon-facebook.svg";
	let twitter = "images/icon-twitter.svg";
	let pinterest = "images/icon-pinterest.svg";
</script>


<div class="relative">

		<Nav {logo} />

	
	<main class="bg-p1 w-full">
		<slot></slot>
		<aside class="bg-p2 relative">
			<StandardPadding>
				
				<GetStarted/>
			</StandardPadding>
		</aside>
	</main>
	<footer class="bg-s5 z-10 relative">
		<div class="py-16 md:py-12 text-white text-sm ">

			<StandardPadding>
				<div class="flex flex-col lg:flex-row items-center lg:items-stretch">
					
					<div class="md:flex md:flex-row md:w-full lg:max-w-md justify-between ">

						<div class="flex flex-col md:justify-between items-center md:items-start">
							<img src={logo} alt="" class="h-6 lg:h-10">
							<div class="mt-6 lg:mb-4 lg:text-lg">
								<a href="/" class="hover:text-p2 transition-colors duration-200">home</a>
								<a href="about"  class="hover:text-p2 transition-colors duration-200 ml-6">about</a>
							</div>
						</div>
						
						
						<address class="text-center opacity-50 mt-6 md:mt-0 leading-6 tracking-wider lg:text-left">
							987  Hillcrest Lane <br/>
							Irvine, CA<br/>
							California 92714<br/>
							Call Us : <a href="tel:+949-833-7432">
								949-833-7432
							</a> 
						</address>
					</div>
						
					<div class="mt-10 md:flex md:flex-row lg:flex-col lg:items-end md:w-full justify-between lg:mt-0">
						<div class="flex justify-center md:mt-0">
							<img src={facebook} alt="">
							<img src={twitter} alt="" class="ml-4"> 
							<img src={pinterest} alt="" class="ml-4">
						</div>
						<p class="opacity-50 mt-4 md:mt-0">Copyright 2020. All Rights Reserved</p>
					</div>
						

				</div>
			</StandardPadding>
		</div>
	</footer>
</div>
	