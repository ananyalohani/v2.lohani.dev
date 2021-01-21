<script>
  import Heading from '../shared/Heading.svelte';
  import Socials from '../shared/Socials.svelte';
  import ContactForm from '../shared/ContactForm.svelte';
  let headingText="Contact";

  function topFunction() {
    document.body.scrollTop = 0; // For Safari
    document.documentElement.scrollTop = 0; // For Chrome, Firefox, IE and Opera
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
  <Socials />
  <ContactForm />
  <p on:click={topFunction} id="scrollToTop">Back to top ↑</p>
</div>

<style>
  #contact {
    padding-top: 40px;
  }

  .text {
    margin-top: 50px;
  }

  #scrollToTop {
    /* text-decoration: underline; */
    cursor: pointer;
    width: fit-content;
    position: relative;
    margin-left: 87%;
    /* margin-bottom: 20px; */
    padding-bottom: 0;
    margin-bottom: 0;
    font-size: smaller;
    border-bottom: solid 2px #4ac2ca5d;
  }

  #scrollToTop:hover {
    font-weight: 500;
    /* height: 22px; */
    background: rgba(11, 105, 109, 0.3);
    transition: all 0.3s ease-in-out;
  }

  @media only screen and (max-width: 450px) {
    #contact {
      max-width: 450px;
    }

    #scrollToTop {
      margin-left: 70%;
    }
  }
</style>