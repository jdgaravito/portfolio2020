<script>
  import Navlist from './UI/Navlist.svelte';
  export let bgColor;
  export let color;
  export let segment;
</script>

<style>
.inner{
  padding: 1.25rem 0 1.25rem 0;
}

</style>

<div class="wrapper" style="background: var(--{bgColor})">
  <div class="inner">
    <Navlist {color} {segment} />
  </div>
</div>
