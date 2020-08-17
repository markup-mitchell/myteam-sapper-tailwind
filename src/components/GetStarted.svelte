<script>
import StandardPadding from "./StandardPadding.svelte";
let bg = "images/bg-pattern-home-6-about-5.svg";
</script>

<aside class="flex flex-col items-center py-24 bg-p2 relative">
    <img src={bg} alt="" class="absolute bottom-0 left-0 -mb-5">
    <h1 class="text-4xl text-s4 text-center leading-none ">
        Ready to get started?
    </h1>
    <a  class="border-2 rounded-full px-8 py-2 mt-6 border-s4 text-md text-s4" href="/contact-us">contact us</a>
</aside>