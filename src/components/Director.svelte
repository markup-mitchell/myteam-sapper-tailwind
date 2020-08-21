<script>
    import {fade} from "svelte/transition";
    export let imageName;
    export let name;
    export let title;
    export let quote = "quote not supplied"
    let image = "images/icon-cross.svg";
    let avatar = `images/avatar-${imageName}.jpg`;
    let state = "profile";
    // let state = "quote";
    let toggle = () => {
        state = state === "profile" ? "quote" : "profile";
    }

    let twitterIcon = "images/icon-twitter.svg";
	let linkedinIcon = "images/icon-linkedin.svg";
	let cross = "images/icon-cross.svg";
</script>


<article class="w-full flex flex-col items-center bg-s4 pt-8 px-6 pb-12 relative"> 

    <img src={avatar} alt={name} class="rounded-full w-24 h-24 border-2 border-s1">
    <h3 class="mt-4 text-s1 text-lg">{name}</h3>
    <p class="italic text-white font-medium text-base mb-2">{title}</p>
    {#if state === 'quote'}
    <div transition:fade class="absolute inset-0 pt-8 px-6 pb-12 flex flex-col items-center bg-s5">
        <blockquote>
            <footer>
                <p class="text-s1 text-center text-lg">
                    {name}
                </p>
            </footer>
            <p class="italic text-white tracking-wider leading-6  text-center text-sm mt-2">
                {quote}
            </p>
        </blockquote>
        <div class="flex mt-6">
            <img src={twitterIcon} alt="">
            <img src={linkedinIcon} alt="" class="ml-4">
        </div>
    </div>
    {/if}
    <button aria-label="Show/Hide" on:click={toggle}
        class="w-16 h-16 rounded-full bg-p2 flex justify-center items-center absolute bottom-0 -mb-8 transform transition- duration-300 transition-all focus:outline-none focus:shadow-focus"
        class:hover:bg-s1="{state === 'profile'}"
        class:hover:bg-p2="{state === 'quote'}"
        class:bg-s1="{state === 'quote'}" >
        <img src={image}
            alt=""
            class="transform transition- duration-300 transition-all"
            class:rotate-45="{state === 'quote'}" >
    </button>
</article>