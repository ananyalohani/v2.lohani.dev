<script>
  import Heading from '../shared/Heading.svelte';
  let headingText="Contact";

  const resetForm = () => {
    // prevent
    document.getElementById('#fullname').value = '';
    document.getElementById('#email').value = '';
    document.getElementById('#text-input').value = '';
  }
</script>

<div id="contact">
  <Heading {headingText} />
  <p class="text">
    You can get in touch with me by filling the contact form below.
    Alternately, you can email me at <a href="mailto:mail@ananyalohani.me">mail@ananyalohani.me.</a>
  </p>
  <p>
    You can (and should) follow me on:
  </p>
  <div class="social-icons">
    <a href="https://instagram.com/ananyalohani/">
      <div class="container">
        <img class="logo instagram" src="./images/socials/instagram.svg" alt="instagram logo"/>
        <p class="logo-label">Instagram</p>
      </div>
    </a>
    <a href="https://github.com/ananyalohani/">
      <div class="container">
        <img class="logo github" src="./images/socials/github.svg" alt="github logo"/>
        <p class="logo-label">Github</p>
      </div>
    </a>
    <a href="https://linkedin.com/in/ananyalohani/">
      <div class="container">
        <img class="logo linkedin" src="./images/socials/linkedin.svg" alt="linkedin logo"/>
        <p class="logo-label">Linkedin</p>
      </div>
    </a>
    <a href="https://twitter.com/ananyalohani_/">
      <div class="container">
        <img class="logo twitter" src="./images/socials/twitter.svg" alt="twitter logo"/>
        <p class="logo-label">Twitter</p>
      </div>
    </a>
  </div>
  <form class="contact-form" action="https://formspree.io/f/xwkwyvar" method="POST">
    <label for="fullname">Name *</label>
    <br/>
    <input class="text-input" id="fullname" type="text" name="fullname" placeholder="Your name" required/>
    <br/>
    <label for="email">Email *</label>
    <br/>
    <input class="text-input" id="email" type="text" name="email" placeholder="Your email address" required/>
    <br/>
    <label for="message">Message *</label>
    <br/>
    <textarea class="text-input" id="text-input" rows="7" name="message" placeholder="Your message" required></textarea>
    <br/>
    <button type="submit">Send</button>
  </form>
</div>

<style>
  .social-icons {
    margin-top: -15px;
    margin-bottom: 20px;
  }

  .logo {
    width: 30px;
    fill: #3db5bbd7;
  }

  .social-icons {
    display: flex;
    flex-direction: row;
  }

  #contact {
    padding-top: 40px;
  }

  .text {
    margin-top: 50px;
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
    padding-left: 5px;
  }

  a:hover {
    color: #c7eff8;
    font-weight: 400;
    /* height: 22px; */
    background: transparent;
    text-shadow: 0 0 7px #64cbe278;
    transition: all 0.3s ease-in-out;
  }

  label {
    font-family: 'Overpass', sans-serif;
    font-weight: 300;
    color: white;
    margin-bottom: -10px;
    margin-top: 10px;
  }

  input {
    margin-top: -10px;
  }

  textarea {
    margin-top: -5px;
  }

  .text-input {
    width: 650px;
    font-size: 14px;
    background-color: #1e4348a9;
    border: solid 1px #245053;
    color: inherit;
  }
  
  .text-input:focus {
    background-color: #27565da9;
    outline: none !important;
  }

  button {
    background: #0E676B;
    outline: none;
    color: white;
    font-family: 'Overpass', sans-serif;
    font-weight: lighter;
    border: solid 1px #245053;
    cursor: pointer;
    padding: 8px 12px;
    border-radius: 3px;
    box-shadow: 1px 2px 5px #0000006b;
  }

  button:hover {
    background: #0e666bc0;
  }

  button:active {
    background: #093e42;
  }

  ::-webkit-input-placeholder { /* WebKit, Blink, Edge */
    color: inherit;
    opacity: 0.75;
  }
  :-moz-placeholder { /* Mozilla Firefox 4 to 18 */
    color: inherit;
    opacity: 0.5;
  }
  ::-moz-placeholder { /* Mozilla Firefox 19+ */
    color: inherit;
    opacity: 0.5;
  }
  :-ms-input-placeholder { /* Internet Explorer 10-11 */
    color: inherit;
    opacity: 0.5;
  }
  ::-ms-input-placeholder { /* Microsoft Edge */
    color: inherit;
    opacity: 0.5;
  }

  ::placeholder { /* Most modern browsers support this now. */
    color: inherit;
    opacity: 0.5;
  }

</style>