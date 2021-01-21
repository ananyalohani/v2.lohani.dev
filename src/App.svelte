<script>
  import Header from './components/Header.svelte';
  import Footer from './components/Footer.svelte';
  import About from './components/About.svelte';
  import Projects from './components/Projects.svelte';
  import Experience from './components/Experience.svelte';
  import Contact from './components/Contact.svelte';
</script>

<main>
  <Header />
  <About />
  <Projects />
  <Experience />
  <Contact />
  <Footer />
</main>

<style>
  main {
    font-family: 'Overpass Mono', monospace;
    color: #D2EAED;
    font-weight: 100;
    max-width: 880px;
    margin: 40px auto;
  }

  /* Mobile Styling */
  @media only screen and (max-width: 550px) {
    main {
      font-family: 'Overpass Mono', monospace;
      color: #D2EAED;
      font-weight: 100;
      width: 100% !important;
      max-width: 450px;
      margin: 0;
    }
  }
</style>