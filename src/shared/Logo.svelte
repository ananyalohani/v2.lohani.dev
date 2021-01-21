<script>
  import tippy from "sveltejs-tippy";

  const props = {
    content: "<span class='tooltip'><p><b>一意</b><p class='pronunciation'>/ichii/</p>Unique, as in 'Ananya'</p></span>",
    allowHTML: true,
    animation: "fade",
    arrow: false,
    placement: "bottom",
  };
</script>

<div class="logo">
  <img src="images/favicons/android-chrome-512x512.png" alt="Ichii Logo" use:tippy={props} />
</div>

<style>
  :global(.tooltip) {
    font-family: 'Overpass-Mono', monospace;
    padding: 4px 8px;
    width: 200px;
    color: #031a1b;
    font-weight: lighter;
    position: absolute;
    left: 0;
    top: 100%;
    font-size: 14px;
    /* white-space: normal; */
    z-index: 2;
    border-radius: 5px ;
    text-align: left;
    background:#c3eff1d3;
    line-height: 1.5;
  }

  :global(.tooltip > p) {
    margin-bottom: 0;
    margin-top: 0;
  }

  :global(.tooltip > b) {
    font-weight: 350;
  }

  :global(.pronunciation) {
    color: #031a1b9a;
    font-size: 13px;
  }

  .logo {
    margin-bottom: 30px;
  }

  img {
    width: 120px;
    -webkit-filter: drop-shadow(0px 0px 20px rgba(0,0,0,0.25));
    filter: drop-shadow(0px 0px 20px rgba(0,0,0,0.25));
  }

  /* Mobile Styling */
  @media only screen and (max-width: 550px) {
    img {
      width: 90px;
    }
  }
</style>