<script>
  export let name;
  export let id;
</script>

<div>

  <label for={id} class="sr-only">
    {name}
  </label>
  <input 
    id={id}
    type="text"
    placeholder={name}
    class="pb-4 pl-4 border-b w-full text-white text-base placeholder-white bg-transparent placeholder-opacity-75"  
  >
</div>