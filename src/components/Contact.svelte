<script>
  import Heading from '../shared/Heading.svelte';
  import Socials from '../shared/Socials.svelte';
  import ContactForm from '../shared/ContactForm.svelte';
  let headingText="Contact";
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
  <Socials />
  <ContactForm />
</div>

<style>
  #contact {
    padding-top: 40px;
  }

  .text {
    margin-top: 50px;
  }
</style>