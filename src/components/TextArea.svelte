<script>
  export let name;
  export let id;
</script>

<div>

  <label for={id} class="sr-only">
    {name}
  </label>
  <textarea 
    id={id}
    type="text"
    rows="3"
    placeholder={name}
    class="pb-4 pl-4 border-b w-full text-white text-base placeholder-white bg-transparent placeholder-opacity-75"  
  ></textarea>
  
</div>