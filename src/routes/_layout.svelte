<script>
  export let segment;
  
  import MainHeader from "../components/MainHeader.svelte";
  import HomeBanner from "../components/HomeBanner/HomeBanner.svelte";
  
  let color;
  let bgColor;
  //background and style switcher based on the segment variable. Change depending the url.
</script>

<style>
  main {
    width: 100%;
    background-color: white;
    margin: 0 auto;
    box-sizing: border-box;
  }
</style>

<main>
<MainHeader {segment} {bgColor} {color} />
  <slot />
</main>
