<script>
import BtnLinkContactUs from "./BtnLinkContactUs.svelte";

	let logo = "images/logo.svg"
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
	}

	.selected {
		position: relative;
		display: inline-block;
	}

	.selected::after {
		position: absolute;
		content: '';
		width: calc(100%);
		height: 4px;
		background-color: #F67E7E;
		display: block;
		bottom: -8px;
	}

</style>

<nav class="flex justify-between mt-12">
	<ul class="text-white text-xl">
		<li class="mr-10">
			<a class:selected='{segment === undefined}' href='.'><img src={logo} alt=""></a>
		</li>
		<li class="ml-10"><a class:selected='{segment === "about"}' href='about'>about</a></li>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<li class="ml-10"><a rel=prefetch class:selected='{segment === "blog"}' href='blog'>blog</a></li>
	</ul>
	<BtnLinkContactUs/>

</nav>
