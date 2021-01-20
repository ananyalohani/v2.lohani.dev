<script>
  import AOS from 'aos';
  AOS.init({
    duration: 1200,
  });
</script>

<div class="card" data-aos="zoom-in-up">
  <slot></slot>
</div>

<style>
  .card {
    padding: 20px;
    margin: 30px auto;
    background-color: #1E4348;
    border: solid 1px #245053;
    box-shadow: 0px, 2px, 4px, rgba(0, 0, 0, 1);
    border-radius: 15px;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }
</style>