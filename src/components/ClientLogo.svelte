<script>
  export let client;
  export let imageName;
  export let width = "w-40";

  let src = `images/logo-${imageName}.png`;
</script>



  <img src={src} alt={client} class="{width} md:h-4 lg:h-6 md:w-auto">
