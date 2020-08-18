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

		<Nav {logo}/>

	
	<main class="bg-p1 w-full">
		<slot></slot>
		<aside class="bg-p2 relative">
			<StandardPadding>
				
				<GetStarted/>
			</StandardPadding>
		</aside>
	</main>
	<footer class="bg-s5 z-10 relative">
		<div class="py-16 ">

			<StandardPadding>
				<div class="flex flex-col items-center">
					<img src={logo} alt="" class="h-6">
					<div class="flex text-white mt-6">
						<a href="home">home</a>
						<a href="about" class="ml-6">about</a>
					</div>
					<address class="text-white no-italic text-center text-sm opacity-50 mt-6 leading-6 tracking-wider">
						987  Hillcrest Lane <br/>
						Irvine, CA<br/>
						California 92714<br/>
						Call Us : <a href="tel:+949-833-7432">
							949-833-7432
						</a> 
					</address>
					<div class="flex mt-10">
						<img src={facebook} alt="">
						<img src={twitter} alt="" class="ml-4"> 
						<img src={pinterest} alt="" class="ml-4">
					</div>
					<p class="text-white opacity-50 text-sm mt-4">Copyright 2020. All Rights Reserved</p>

				</div>
			</StandardPadding>
		</div>
	</footer>
</div>
	