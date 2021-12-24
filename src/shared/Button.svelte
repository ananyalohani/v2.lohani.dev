<script>
  export let type;
</script>

<button {type}>
  <slot />
</button>

<style>
  button {
    background: #0e676b;
    outline: none;
    color: white;
    font-family: 'Overpass', sans-serif;
    font-weight: lighter;
    border: solid 1px #245053;
    cursor: pointer;
    padding: 8px 15px;
    border-radius: 3px;
    box-shadow: 1px 2px 5px #0000006b;
  }

  button:hover {
    background: #0e666bc0;
  }

  button:active {
    background: #093e42;
  }
</style>
