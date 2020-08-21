<script>
    export let icon;
    export let heading;
    export let copy; 
    let iconImage = `images/icon-${icon}.svg`;
</script>


    <div class="flex flex-col items-center lg:items-start md:flex-row">
        
        <img src={iconImage} alt="">
            <div class="flex-col md:flex md:ml-6">
            <h3 class="text-p2 text-xl mt-4 lg:mt-0 text-center md:text-left">{heading}</h3>
            <p class="mt-2 md:mt-4 leading-6 tracking-0 text-sm lg:text-base text-center md:text-left text-white">{copy}</p>
        </div>
    </div>
