<script>
  import Logo from '../shared/Logo.svelte';
  let headingText="Ananya Lohani";
</script>

<header>
  <Logo />
  <h2>{headingText}</h2>
  <div class="navbar">
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#contact">Contact</a></li>
      <li><a href="https://ananya.li/resume">Resume</a></li>
    </ul>
  </div>
</header>

<style>

  header {
    color: #FFFFFF;
    font-family: 'Overpass Mono', monospace;
    text-align: center;
  }

  h2 {
    font-weight: 500;
    font-family: 'Overpass Mono', monospace;
    color: #baebee8a;
    margin-top: -20px;
    margin-bottom: 30px;
    padding-bottom: 10px;
  }

  a {
    text-decoration: none;
    color: inherit;
    border-bottom: none;
    padding: 5px 0;
  }

  .navbar {
    background-color: #0E676B;
    padding: 9px;
    font-size: 17px;
    box-shadow: 0px 0px 20px 5px rgba(0, 0, 0, 0.25);
    border-radius: 20px;
  }

  ul {
    list-style: none;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    margin: 0;
    padding: 0;
  }

  a {
    position: relative;
  }

  a::after {
    content:"";
    width: 100%;
    height: 0;
    display: block;
    position: absolute;
    bottom: 3px;
    left: 0;
    background: rgba(126, 198, 207, 0.5);
    transition: all 0.3s ease-in-out;
  }

  a:hover::after {
    height: 5px;
  }

  a:hover {
    font-weight: 300;
  }

  /* Mobile Styling */
  @media only screen and (max-width: 550px) {
    .navbar {
      font-size: 15px;
      margin-bottom: -30px;
    }

    h2 {
      font-size: 20px;
    }
  }
</style>