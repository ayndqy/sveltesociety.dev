<script>
  export let title = ''
</script>
  
<style>
  .card {
    box-shadow: -5px 5px 5px rgba(0, 0, 0, 0.3);
    border: var(--m1) solid var(--color);
    width: fit-content;
  }

  .card > .title {
    background-color: var(--color);
    padding: var(--m10);
    color: #ffffff;    
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 48px;
    max-width: 100%;
  }

  .title > h2 {
    text-overflow: ellipsis;
    white-space: nowrap;
    overflow: hidden;
    font-size: 1.5em;
  }

  .title > .circles {
    display: block;
    width: var(--m18);
    height: var(--m18);
    border-radius: 50%;
    background-color: var(--color-red);
    border: 1px solid #fff;
    box-shadow: 25px 0 0 0 var(--color-yellow), 50px 0 0 0 var(--color-green);
    margin-right: 50px;
    margin-left: 20px;
  }

  .card > section {
    display: block;
    padding: var(--m10);
    height: calc(100% - 48px);
    overflow-x: auto;
    font-size: 0.8rem;
  }

  @media (max-width: 484px) {
    .title > h2 {
      font-size: 0.8em;
    }
  }
</style>

<div class="card">
  <header class="title">
    <h2>{title}</h2>
    <span class="circles" />
  </header>
  <section>
    <slot>Content</slot>
  </section>
</div>