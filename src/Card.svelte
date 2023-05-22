<script>
  export let price;
  export let description;
  export let image;
</script>

<main>
  <div>
    <h2>product price is {price}</h2>
    {description}
    <img src={image} alt="" />
  </div>
</main>
