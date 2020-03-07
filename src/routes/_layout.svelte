<script>
  import '../../node_modules/bulma/css/bulma.css';
  import Nav from '../components/Nav.svelte';
  import { hideSidebar } from '../stores.js';
  export let segment;
  let hide_sidebar;
  const unsubscribe = hideSidebar.subscribe(value => hide_sidebar = value);
</script>

<style>
  main {
      position: relative;
      max-width: 56em;
      background-color: white;
      padding: 2em;
      margin: 0 auto;
      box-sizing: border-box;
  }
</style>

<main>
  <div class="columns">
    <div class="column" class:is-two-thirds="{!hide_sidebar}">
      <slot></slot>
    </div>
    <Nav {segment} hideSidebar={hide_sidebar}/>
  </div>
</main>
