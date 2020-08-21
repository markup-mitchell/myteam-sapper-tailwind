<script>
    export let quote;
    export let avatar;
    export let name;
    export let jobTitle;

    let quotes = 'images/icon-quotes.svg';
    let avatarImage = `images/avatar-${avatar}.jpg`; 
</script>

<article  class="flex flex-col pt-10 mt-12" style={`background-image:url(${quotes});background-repeat:no-repeat;background-position: center top;`}>
    <blockquote class="text-base text-white text-center w-full">
        <p class="text-sm leading-relaxed">
            {quote}
        </p>
        <footer class="flex flex-col items-center">
            <p class="text-lg mt-4 lg:mt-6 text-s1">
                {name}
            </p>
            <p class="text-sm font-medium italic leading-none mt-1">
                {jobTitle}
            </p>
            <img src={avatarImage} alt={name} class="mt-4 lg:mt-8 rounded-full w-16 h-16 border-s6 border-2">
        </footer>
    </blockquote>
</article>

