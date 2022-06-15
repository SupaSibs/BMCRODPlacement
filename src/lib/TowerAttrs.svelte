<script lang="ts">
  let InputElement
    function DisplayImage(): void { 
      let FileReader = new FileReader()
console.log(InputElement.files[0])
   
  }
</script>

<form on:submit|preventDefault={DisplayImage} method="post">
<input type="file" id="files" name="files" bind:this={InputElement} />
<button type="submit" >Submit</button>
</form>