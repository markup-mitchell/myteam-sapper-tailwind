<script>
    export let icon;
    export let heading;
    export let copy; 
    let iconImage = `images/icon-${icon}.svg`;
</script>


    <div class="flex flex-col items-center">
        <img src={iconImage} alt="">
        <h3 class="text-p2 text-xl mt-4">{heading}</h3>
        <p class="mt-2 leading-6 tracking-wider text-center text-white">{copy}</p>
    </div>
