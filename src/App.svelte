<script>
  import Card from "./Card.svelte";

  let price = 50;
  let description = "";
  let image;

  const imageHandler = (event) => {
    const file = event.target.files[0];
    if (file) {
      const reader = new FileReader();

      reader.onload = function (event) {
        image = event.target.result;
      };

      reader.readAsDataURL(file);
    }
  };
</script>

<main>
  <input type="text" bind:value={price} />
  <input type="text" bind:value={description} />
  <input type="file" on:input={imageHandler} />
  <br />
  <Card {price} {description} {image} />
</main>

<style>
</style>
