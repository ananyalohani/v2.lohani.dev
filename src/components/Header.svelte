<header>
  <div class="logo">
    <img src="images/favicons/android-chrome-512x512.png" alt="Ichii Logo" />
  </div>
  <div class="navbar">
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>
</header>

<style>

  header {
    color: #FFFFFF;
    font-family: 'Overpass Mono', monospace;
    text-align: center;
  }

  a {
    text-decoration: none;
    color: inherit;
  }

  .logo {
    margin-bottom: 30px;
  }

  img {
    width: 120px;
    -webkit-filter: drop-shadow(0px 0px 20px rgba(0,0,0,0.25));
    filter: drop-shadow(0px 0px 20px rgba(0,0,0,0.25));
  }
  
  img:hover::after {
    content:"test";
    width: 100%;
    display: block;
    position: absolute;
    bottom: 0;
    left: 0;
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
  @media only screen and (max-width: 450px) {
    .navbar {
      font-size: 15px;
      margin-bottom: -30px;
    }

    img {
      width: 90px;
    }
  }
</style>