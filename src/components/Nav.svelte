<script>
  export let segment;
</script>

<nav>
  <ul>
    <li>
      <a aria-current={segment === "about" ? "page" : undefined} href="about"
        >About</a
      >
    </li>
    <li>
      <a aria-current={segment === undefined ? "page" : undefined} href="."
        >News</a
      >
    </li>
    <!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
    <li>
      <a
        rel="prefetch"
        aria-current={segment === "blog" ? "page" : undefined}
        href="solarSystem">Solar system</a
      >
    </li>
    <li>
      <a
        rel="prefetch"
        aria-current={segment === "blog" ? "page" : undefined}
        href="milkyWay">Milky Way</a
      >
    </li>
  </ul>
</nav>

<style>
  nav {
    border-bottom: 1px solid rgba(255, 62, 0, 0.1);
    font-weight: 300;
  }

  ul {
    margin: 0;
    padding-right: 2rem;
  }

  /* clearfix */
  ul::after {
    content: "";
    display: block;
    clear: both;
  }

  li {
    display: block;
    float: right;
    color: white;
  }

  [aria-current] {
    position: relative;
    display: inline-block;
  }

  /* [aria-current]::after {
    position: absolute;
    content: "";
    width: calc(100% - 1em);
    height: 2px;
    background-color: rgb(255, 62, 0);
    display: block;
    bottom: -1px;
  } */

  a {
    text-decoration: none;
    padding-top: 3.5rem;
    padding-left: 1.5rem;

    display: block;
  }
</style>
