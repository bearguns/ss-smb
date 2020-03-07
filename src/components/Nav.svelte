<script>
  export let segment;
  export let hideSidebar;
</script>

<style>
	nav {
		border-left: 1px solid black;
		font-weight: 300;
		padding: 0 1em;
	}

	ul {
		margin: 0;
		padding: 0;
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

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: black;
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}
</style>

<div class="column is-one-third" class:hidden="{hideSidebar}">
  <nav>
    <h1 class="title">I'M SEAN BRAGE</h1>
    <ul>
      <li><a aria-current='{segment === undefined ? "page" : undefined}' href='.'>resume</a></li>
      <li><a aria-current='{segment === "about" ? "page" : undefined}' href='about'>about</a></li>

      <!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
	   the blog data when we hover over the link or tap it on a touchscreen -->
      <li><a rel=prefetch aria-current='{segment === "print" ? "page" : undefined}' href='print'>print</a></li>
    </ul>
  </nav>
</div>
