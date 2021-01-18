<script>
  import Heading from './Heading.svelte';
  let headingText = "About";
</script>

<div id="about">
  <Heading {headingText} />
  <div class="section-content">
    <img class="my-photo" src="./images/my-photo.png" alt="Ananya Lohani"/>
    <p class="about-me">Hello, I am Ananya. Welcome to my website!
      <br/>
      <br/>
      I am a Sophomore at <a href="https://iiitd.ac.in/" target="_blank">IIIT Delhi</a>, majoring in Computer Science and Engineering. My recent interests include web development and UI/UX design. I am currently a Web Design intern at <a href="https://vincistationery.com" target="_blank">Vinci Stationery</a>.
      <br/>
      <br/>
      I paint, sometimes. You can see all my artwork on my <a href="https://www.instagram.com/lohani_art/" target="_blank">art account</a>.</p>
  </div>
</div>

<style>
  #about {
    color: #bae4eb;
    margin-top: 40px;
    font-family: 'Overpass Mono', monospace;
    font-weight: 300;
  }

  a:hover {
    color:#8db1b8;
  }

  .section-content {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    vertical-align: middle;
  }

  .about-me {
    padding-top: 50px;
  }

  .my-photo {
    height: 450px;
    width: 450px;
  }
  
  p {
    vertical-align: middle;
  }

</style>