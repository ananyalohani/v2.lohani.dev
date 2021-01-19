<script>
  import Card from '../shared/Card.svelte';
  export let project;
</script>

<div class="project-details">
  <Card>
    <img src={project.logo} alt={project.title + " logo"} />
    <div class="body">
      <h3><a href={project.link}>{project.title}</a></h3>
      <p class="duration">{project.duration}</p>
      <p>{project.description}</p>
      <h4>Technologies Used:</h4>
      <p>
        {#each project.technologies as tech, i}
          {tech}{i == project.technologies.length - 1 ? "" : ", "}
        {/each}
      </p>
    </div>
  </Card>
</div>

<style>
  p {
    font-size: 15px;
    color:#bae4eb;
    font-weight: 100;
  }

  img {
    max-width: 140px;
    max-height: 140px;
    padding: 20px 20px 40px 20px;
    -webkit-filter: drop-shadow(0px 0px 10px rgba(0,0,0,0.25));
    filter: drop-shadow(0px 0px 10px rgba(0,0,0,0.25));
  }

  h3, h4 {
    font-family: 'Overpass', sans-serif;
    font-weight: 500;
    padding: 0;
    margin: 0;
    margin-bottom: -12px;
  }

  a {
    text-decoration: none;
    position: relative;
  }

  a::after {
    content:"";
    width: 100%;
    height: 0;
    display: block;
    position: absolute;
    bottom: 1px;
    left: 0;
    background: rgba(102, 165, 173, 0.5);
    transition: all 0.3s ease-in-out;
  }

  a:hover::after {
    height: 5px;
  }

  a:hover {
    color: inherit;
    background: transparent;
  }

  .duration {
    font-size:smaller;
  }

  .body {
    padding-left: 20px;
  }
</style>