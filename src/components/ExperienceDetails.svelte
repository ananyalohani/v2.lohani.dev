<script>
  import Card from '../shared/Card.svelte';
  export let exp;
</script>

<div class="exp-details">
  <Card>
    <img src={exp.logo} alt={exp.company + " logo"} />
    <div class="body">
      <h3><a href={exp.link} target="_blank">{exp.company}</a></h3>
      <p class="job-title">{exp.jobTitle}</p>
      <p class="duration">{exp.duration}</p>
      <p>{exp.responsibilities}</p>
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

  h3 {
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