<script>
  import Heading from '../shared/Heading.svelte';
  let headingText = 'About';
</script>

<div id="about">
  <Heading {headingText} invisibleOnPhone="true" />
  <div class="section-content">
    <img class="my-photo" src="./images/my-photo.png" alt="Ananya Lohani" />
    <p class="about-me">
      Hello, I am Ananya. Welcome to my website!
      <br />
      <br />
      I am a 3rd year undergrad at
      <a href="https://iiitd.ac.in/" target="_blank">IIIT Delhi</a>, majoring in
      Computer Science and Engineering. I am currently a Frontend Engineer at
      <a href="https://tweek-labs.com" target="_blank">Tweek Labs</a>.
      <br />
      <br />
      I get bored of things easily and I'm constantly looking for new things to learn.
      <br />
      I paint, sometimes. You can see all my artwork on my
      <a href="https://www.instagram.com/lohani_art/" target="_blank"
        >art account</a
      >.
    </p>
  </div>
</div>

<style>
  #about {
    margin-top: 40px;
    font-family: 'Overpass Mono', monospace;
    font-weight: 300;
    margin-bottom: -20px;
  }

  .section-content {
    width: 100%;
    display: flex;
    flex-direction: row;
    margin-top: 30px;
    /* flex-wrap: wrap; */
    align-items: center;
    justify-content: center;
    vertical-align: middle;
    line-height: 1.75;
  }

  .my-photo {
    height: 350px;
    width: 350px;
    padding: 40px;
    -webkit-filter: drop-shadow(0px 0px 20px rgba(0, 0, 0, 0.25));
    filter: drop-shadow(0px 0px 20px rgba(0, 0, 0, 0.25));
  }

  p {
    vertical-align: middle;
  }

  @media only screen and (max-width: 700px) {
    .section-content {
      flex-direction: column;
    }
  }

  /* Mobile Styling */
  @media only screen and (max-width: 550px) {
    .section-content {
      flex-direction: column;
      align-items: center;
    }

    .my-photo {
      height: 200px;
      width: 200px;
      padding-top: 20px;
      padding-bottom: 10px;
      /* padding-left: 70px; */
    }

    #about {
      margin-top: 50px;
    }
  }
</style>
