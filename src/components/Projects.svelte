<script>
  import Heading from '../shared/Heading.svelte';
  import ProjectDetails from './ProjectDetails.svelte';
  import projects from '../../json/projects.json';
  let headingText="Projects";
</script>

<div id="projects">
  <Heading {headingText} />
  <p class="text">You can find all my projects on my <a href="https://github.com/ananyalohani/">GitHub account</a>. The most significant ones are mentioned below.</p>
  {#each projects as project}
    <ProjectDetails {project} />
  {/each}
</div>

<style>
  .text {
    margin-top: 50px;
  }

  /* Mobile Styling */
  @media only screen and (max-width: 550px) {
    #projects {
      margin-top: 50px;
    }
  }
</style>