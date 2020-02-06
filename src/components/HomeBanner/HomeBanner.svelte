<script>
  export let bgImage;
</script>

<style>
  .wrapper {
    background: var(--image);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    height: 90vh;
  }
</style>

<div class="wrapper" style="--image: url({bgImage});">
<div class="inner">

</div>
</div>
