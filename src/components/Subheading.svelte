<script>
    export let icon;
    export let heading;
    export let copy; 
    let iconImage = `images/icon-${icon}.svg`;
</script>


    <div class="flex flex-col items-center md:flex-row">
        
        <img src={iconImage} alt="">
            <div class="hidden flex-col md:flex ml-6">
            <h3 class="text-p2 text-xl mt-4">{heading}</h3>
            <p class="mt-2 md:mt-4 leading-6 tracking-wider text-center md:text-left text-white">{copy}</p>
        </div>
    </div>
