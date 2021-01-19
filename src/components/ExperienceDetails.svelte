<script>
  import Card from '../shared/Card.svelte';
  export let exp;
</script>

<div class="exp-details">
  <Card>
    <img src={exp.logo} alt={exp.company + " logo"} />
    <div class="body">
      <h3><a href={exp.link}>{exp.company}</a></h3>
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
    max-width: 120px;
    max-height: 120px;
    padding: 20px 40px;
    -webkit-filter: drop-shadow(0px 0px 20px rgba(0,0,0,0.25));
    filter: drop-shadow(0px 0px 20px rgba(0,0,0,0.25));
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
  }

  .duration {
    font-size:smaller;
  }
</style>