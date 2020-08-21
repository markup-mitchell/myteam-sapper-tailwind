<script>
import BtnLinkContactUsDark from "./BtnLinkContactUsDark.svelte";


    let bg = "images/bg-pattern-home-6-about-5.svg";
</script>

<div class="flex flex-col md:flex-row items-center justify-between pt-20 pb-24 ">
    <img src={bg} alt="" class="absolute bottom-0 left-0 -mb-5">


        <h2 class="text-4xl  lg:text-5xl  text-s4 text-center inline leading-none ">
            Ready to get started?
        </h2>
        <div class="mt-6 md:mt-0 lg:mr-20">

            <BtnLinkContactUsDark />
        </div>
    </div>