<script>
    export let imageName;
    export let name;
    export let title;
    let image = "images/icon-cross.svg";
    let avatar = `images/avatar-${imageName}.jpg`;
</script>


<div class="w-full flex flex-col items-center bg-s5 pt-8 pb-12  relative">
    <img src={avatar} alt={name} class="rounded-full w-24 h-24 border-2 border-s1">
    <p class="mt-4 text-s1 text-xl">{name}</p>
    <p class="italic text-white font-medium text-base mb-2">{title}</p>
    <div class="w-16 h-16 rounded-full bg-p2 flex justify-center items-center absolute bottom-0 -mb-8">
        <img src={image} alt="">
    </div>
</div>