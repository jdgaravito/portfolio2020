<script>
  export let segment;
  export let color ;
</script>

<style>
  .navlist {
    display: flex;
    list-style-type: none;
    flex-wrap: wrap;
    justify-content: space-evenly;
  }
  /* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}
	li {
		display: block;
		float: left;
	}


  a {
    color: var(--color);
    font-weight: 700;
    font-family: "Raleway";
    text-decoration: none;
    padding: 0 0.625rem 0 0.625rem;
  }

  .selected {
    position: relative;
    display: inline-block;
  }

  .selected::after {
    position: absolute;
    content: "";
    width: calc(100% - 1em);
    height: 2px;
    background-color: white;
    opacity: 30%;
    display: block;
    bottom: -1px;
  }
</style>

<ul class="navlist" >
  <li>
    <a rel="prefetch" class:selected={segment === undefined} href="." style="--color:{color}">Me</a>
  </li>
  <li>
    <a rel="prefetch" class:selected={segment === 'dev'} href="dev" style="--color:{color}">/dev</a>
  </li>
  <li>
    <a rel="prefetch" class:selected={segment === 'ux-ui'} href="ux-ui" style="--color:{color}">
      UX/UI
    </a>
  </li>
  <li>
    <a rel="prefetch" class:selected={segment === 'product'} href="product" style="--color:{color}">
      Product
    </a>
  </li>
  <li>
    <a rel="prefetch" class:selected={segment === 'video'} href="video" style="--color:{color}">
      Video
    </a>
  </li>
  <li>
    <a class:selected={segment === 'contact'} href="contact" style="--color:{color}">Contact</a>
  </li>
</ul>
