<script lang="ts">
  let InputElement
    function DisplayImage(): void { 
      let reader = new FileReader()
let file = InputElement.files[0]
     reader.onloadend = function(e)  {
        let image = document.createElement("img");
        // the result image data
        image.src = e.target.result;
        document.body.appendChild(image);
     }
     // you have to declare the file loading
     reader.readAsDataURL(file);
  }
</script>

<form on:submit|preventDefault={DisplayImage} method="post">
<input type="file" id="files" name="files" bind:this={InputElement} />
<button type="submit" >Submit</button>
</form>