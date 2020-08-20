<script>
  export let client;
  export let imageName;

  let src = `images/logo-${imageName}.png`;
</script>



<img src={src} alt={client} class="w-32 flex-shrink">