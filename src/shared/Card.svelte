<script>
  import AOS from 'aos';
  AOS.init({
    duration: 700,
    once: true,
    offset: 100,
  });
</script>

<div class="card" data-aos="fade-up" data-aos-offset="100" data-aos-once="true">
  <slot />
</div>

<style>
  .card {
    padding: 20px;
    margin: 30px auto;
    background-color: #1e4348;
    border: solid 1px #245053;
    box-shadow: 0px, 2px, 4px, rgba(0, 0, 0, 1);
    border-radius: 15px;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }

  @media only screen and (max-width: 550px) {
    .card {
      flex-wrap: wrap;
    }
  }
</style>
