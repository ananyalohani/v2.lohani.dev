<script>
  export let headingText;
  export let invisibleOnPhone = false;
</script>

<div class="section-heading" class:invisible={invisibleOnPhone}>
  <div class="wrapper">
    <h1>{headingText}</h1>
    <div class="background-deco"></div>
  </div>
</div>

<style>
  .section-heading {
    padding: 0;
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    vertical-align: center;
  }

  .wrapper {
    text-align: center;
    font-family: 'Overpass', sans-serif;
    color: white;
    width: min-content;
  }

  h1 {
    position: relative;
    font-weight: 500;
    letter-spacing: 3px;
    text-shadow: 0px 4px 10px rgba(0, 0, 0, 0.5);
    font-size: 35px;
  }

  .background-deco {
    height: 10px;
    background-color: rgb(11, 105, 109);
    margin-top: -45px;
  }

  /* Mobile Styling */
  @media only screen and (max-width: 550px) {
    h1 {
      font-size: 30px;
    }

    .background-deco {
      height: 10px;
      margin-top: -39px;
    }

    .invisible {
      display: none;
    }
  }
</style>