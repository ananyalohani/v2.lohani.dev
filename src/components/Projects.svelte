<script>
  import Heading from '../shared/Heading.svelte';
  import projectData from '../../json/projects.json';
  let headingText="Projects";
  console.log(projectData);
</script>

<div id="projects">
  <Heading {headingText} />
</div>

<style>
  #projects {}
</style>