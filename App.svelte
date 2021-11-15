<script>
  import Button from "./Button.svelte";
  import About from "./About.svelte";
  import Portfolio from "./Portfolio.svelte";
  let page = "";
</script>

<nav>
	<code>Provided by App.svelte nav:</code>
	<span on:click={e => page = ""}> Home </span>
	<span on:click={e => page = "About"}> About </span>
	<span on:click={e => page = "Portfolio"}> Portfolio </span>
</nav>

<main>
  {#if page === "About"}
    <About />
  {:else if page === "Portfolio"}
    <Portfolio />
  {:else}
    <h1>Hello CodeSandbox</h1>
    <h2>Start editing to see some magic happen!</h2>
    <Button />
  {/if}
</main>

<style>
  main {
    font-family: sans-serif;
    text-align: center;
  }
  nav {
    background-color: pink;
    position: fixed;
    top: 0px;
    left: 0px;
    height: 30px;
    width: 100%;
  }
  span {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
      Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
    color: rgb(0, 100, 200);
  }
  span:hover {
    text-decoration: underline;
    cursor: pointer;
  }
  main {
    padding-top: 30px;
    margin: 0;
  }
  :global(body) {
    padding: 0;
  }
</style>