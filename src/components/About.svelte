<script>
  import Heading from '../shared/Heading.svelte';
  let headingText = "About";
</script>

<div id="about">
  <Heading {headingText} invisibleOnPhone="true"/>
  <div class="section-content">
    <img class="my-photo" src="./images/my-photo.png" alt="Ananya Lohani"/>
    <p class="about-me">Hello, I am Ananya. Welcome to my website!
      <br/>
      <br/>
      I am a 2nd year undergrad student at <a href="https://iiitd.ac.in/" target="_blank">IIIT Delhi</a>, majoring in Computer Science and Engineering. My recent interests include web development and UI/UX design. I am currently a Web Design and Development intern at <a href="https://cse.iiitd.ac.in/" target="_blank">Department of CSE</a>, IIIT Delhi. I am also a part of the Web Development team of <a href='https://iiitdplaybook.web.app/'>IIITD Playbook</a>.
      <br/>
      <br/>
      I paint, sometimes. You can see all my artwork on my <a href="https://www.instagram.com/lohani_art/" target="_blank">art account</a>.</p>
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
    /* flex-wrap: wrap; */
    align-items: center;
    justify-content: center;
    vertical-align: middle;
    line-height: 1.75;
  }

  .about-me {
    padding-top: 30px;
  }

  .my-photo {
    height: 350px;
    width: 350px;
    padding: 40px;
    -webkit-filter: drop-shadow(0px 0px 20px rgba(0,0,0,0.25));
    filter: drop-shadow(0px 0px 20px rgba(0,0,0,0.25));
  }
  
  p {
    vertical-align: middle;
  }

  a {
    border-bottom: solid 2px #4ac2ca5d;
    text-decoration: none;
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