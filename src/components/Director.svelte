<script>
    export let imageName;
    export let name;
    export let title;
    export let quote;
    let image = "images/icon-cross.svg";
    let avatar = `images/avatar-${imageName}.jpg`;
    let state = "profile";
    // let state = "quote";

    let twitterIcon = "images/icon-twitter.svg";
	let linkedinIcon = "images/icon-linkedin.svg";
	let cross = "images/icon-cross.svg";
</script>


<div class="w-full flex flex-col items-center bg-s4 pt-8 px-6 pb-12  relative"> 

    {#if state === 'profile'}
    <img src={avatar} alt={name} class="rounded-full w-24 h-24 border-2 border-s1">
    <p class="mt-4 text-s1 text-lg">{name}</p>
    <p class="italic text-white font-medium text-base mb-2">{title}</p>

    {:else if state === 'quote'}

    <p class="mt-4 text-s1 text-lg">{name}</p>
			<p class="italic text-white tracking-wider leading-6 mt-2 text-center text-sm">{quote}</p>
			<div class="flex mt-6">
				<img src={twitterIcon} alt="">
				<img src={linkedinIcon} alt="" class="ml-4">
            </div>
            {:else}
            ERROR!
            {/if}
    <div class="w-16 h-16 rounded-full bg-p2 flex justify-center items-center absolute bottom-0 -mb-8">
        <img src={image} alt="">
    </div>
</div>