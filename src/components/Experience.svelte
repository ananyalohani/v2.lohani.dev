<script>
  import Heading from '../shared/Heading.svelte';
  import ExperienceDetails from './ExperienceDetails.svelte';
  import workex from '../../json/experience.json';
  let headingText="Experience";
</script>

<div id="experience">
  <Heading {headingText} />
  <p class="text">If you like my work and are interested in working with me, you can contact me via this <a href="#contact">Contact Form</a>.</p>
  {#each workex as exp}
    <ExperienceDetails {exp} />
  {/each}
</div>

<style>
  #experience {
    margin-top: 40px;
  }

  .text {
    margin-top: 50px;
  }
</style>