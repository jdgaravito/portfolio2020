<script>
  export let segment;
  
  import MainHeader from "../components/MainHeader.svelte";
  import HomeBanner from "../components/HomeBanner/HomeBanner.svelte";
  
  let color;
  let bgColor;
  let bgImage;  
  //background and style switcher based on the segment variable. Change depending the url.

  $: switch (segment) {
    case undefined:
      bgImage = "/images/design-1920.jpg";
      color = "black";
      break;
    case "dev":
      bgImage = "/images/desarrollo-1920.jpg";
      color = "black";
      bgColor ="devGr";
      break;
    case "ux-ui":
      bgImage = "/images/design-1920.jpg";
      color = "white";
      bgColor ="uxGr";
      break;

    case "product":
      bgImage = "/images/product-1920.jpg";
      bgColor ="prodGr";
      color = "white";
      break;

    case "video":
      bgImage = "/images/video-1920.jpg";
      bgColor ="videoGr";
      color = "white";
      break;

    case "contact":
      
      break;
  }
</script>

<style>
  main {
    width: 100%;
    background-color: white;
    margin: 0 auto;
    box-sizing: border-box;
  }
</style>

<HomeBanner {bgImage} />
<MainHeader {segment} {bgColor} {color} />

<main>
  <slot />
</main>
