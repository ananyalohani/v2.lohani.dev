<script>
  import Button from './Button.svelte';
  import {onMount} from 'svelte';
  let fields = {name: "", email: "", message:""};

  onMount(() => {
    const formElement = document.querySelector('#contact-form');
    formElement.addEventListener('submit', (event) => {
      event.preventDefault();
      const data = new URLSearchParams(new FormData(formElement));
      fetch("https://formspree.io/f/xwkwyvar", {
        method: 'post',
        body: data
      });
      alert("Thanks for submitting! :)");
      fields.name = "";
      fields.email = "";
      fields.message = "";
    });
  });
</script>

<form id="contact-form" action="https://formspree.io/f/xwkwyvar" method="POST">
  <label for="fullname">Name *</label>
  <br/>
  <input bind:value={fields.name} class="text-input" id="fullname" type="text" name="fullname" placeholder="Your name" required/>
  <br/>
  <label for="email">Email *</label>
  <br/>
  <input bind:value={fields.email} class="text-input" id="email" type="text" name="email" placeholder="Your email address" required/>
  <br/>
  <label for="message">Message *</label>
  <br/>
  <textarea bind:value={fields.message} class="text-input" id="text-input" rows="7" name="message" placeholder="Your message" required></textarea>
  <br/>
  <Button type="submit">
    Send
  </Button>
</form>

<style>
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

  @media only screen and (max-width: 550px) {
    .text-input {
      width: 97%;
    }

    textarea {
      resize: vertical;
    }
  }
</style>