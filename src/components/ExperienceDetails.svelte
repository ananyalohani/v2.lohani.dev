<script>
  import Card from '../shared/Card.svelte';
  export let exp;
  let currentColor = '#bae4eb';
</script>

<div class="exp-details">
  <Card>
    <img src={exp.logo} alt={exp.company + ' logo'} />
    <div class="body">
      <h3>
        <a href={exp.link} target="_blank">{exp.company}</a>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="15"
          height="15"
          viewBox="0 0 24 24"
          fill="none"
          stroke={currentColor}
          strokeWidth="1.5"
          strokeLinecap="round"
          strokeLinejoin="round"
          ><g fill="none" fill-rule="evenodd"
            ><path
              d="M18 14v5a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8c0-1.1.9-2 2-2h5M15 3h6v6M10 14L20.2 3.8"
            /></g
          ></svg
        >
      </h3>
      <p class="job-title">{exp.jobTitle}</p>
      <p class="duration">{exp.duration}</p>
      <p>{exp.responsibilities}</p>
    </div>
  </Card>
</div>

<style>
  p {
    font-size: 14px;
    line-height: 1.25;
    color: #bae4eb;
    font-weight: 100;
  }

  img {
    max-width: 140px;
    max-height: 140px;
    margin: 20px 20px 40px 20px;
    -webkit-filter: drop-shadow(0px 0px 10px rgba(0, 0, 0, 0.25));
    filter: drop-shadow(0px 0px 10px rgba(0, 0, 0, 0.25));
    border-radius: 20px;
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
    border-bottom: none;
  }

  a::after {
    content: '';
    width: 100%;
    height: 0;
    display: block;
    position: absolute;
    bottom: 0px;
    left: 0;
    background: rgba(102, 165, 173, 0.5);
    /* transition: all 0.1s ease-in-out; */
  }

  a:hover::after {
    height: 2px;
  }

  a:hover {
    color: inherit;
    background: transparent;
  }

  .duration {
    font-size: smaller;
  }

  .body {
    padding-left: 20px;
  }
</style>
