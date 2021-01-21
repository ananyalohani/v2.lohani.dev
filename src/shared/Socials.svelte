<div class="social-icons">
  <div class="container">
    <img class="logo instagram" src="./images/socials/instagram.svg" alt="instagram logo"/>
    <a href="https://instagram.com/ananyalohani/" target="_blank">
      <p class="logo-label">Instagram</p>
    </a>
  </div>
  <div class="container">
    <img class="logo github" src="./images/socials/github.svg" alt="github logo"/>
    <a href="https://github.com/ananyalohani/" target="_blank">
      <p class="logo-label">Github</p>
    </a>
  </div>
  <div class="container">
    <img class="logo linkedin" src="./images/socials/linkedin.svg" alt="linkedin logo"/>
    <a href="https://linkedin.com/in/ananyalohani/" target="_blank">
      <p class="logo-label">Linkedin</p>
    </a>
  </div>
  <div class="container">
    <img class="logo twitter" src="./images/socials/twitter.svg" alt="twitter logo"/>
    <a href="https://twitter.com/ananyalohani_/" target="_blank">
      <p class="logo-label">Twitter</p>
    </a>
  </div>
</div>

<style>
  .social-icons {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    margin-top: -15px;
    margin-bottom: 20px;
  }

  .logo {
    width: 30px;
    fill: #3db5bbd7;
  }

  p {
    /* margin-left: 5px; */
    /* padding-right: 5px; */
  }

  .logo-label {
    padding-left: 5px;
  }

  .container {
    display: flex;
    flex-direction: row;
    padding-left: 0;
    padding-right: 40px;
  }

  a {
    text-decoration: none;
    position: relative;
  }

  a::after {
    content:"";
    width: 94%;
    height: 0;
    display: inline;
    position: absolute;
    bottom: -15px;
    left: 6px;
    background: rgba(102, 165, 173, 0.5);
    /* transition: all 0.3s ; */
  }

  a:hover::after {
    height: 6px;
  }

  a:hover {
    color: inherit;
    background: transparent;
  }
</style>