<script>
  import ArticleTeaser from '../../components/ArticleTeaser.svelte';

  export let data, helpers;

  export let foo;

  // add permalinks to the hook list so we can link to the posts.
  const hooks = data.hookInterface.map((hook) => ({ ...hook, link: helpers.permalinks.hooks({ slug: hook.hook }) }));
</script>

<style>
  .banner {
    /*padding: 1rem 2rem;*/
    color: #00a000;
    width: 100%;
    /*background: #d0ffd0;*/
    /*border-radius: 0.5rem;*/
    margin-bottom: 1rem;
  }
  .entries {
    display: grid;
    grid-template-columns: 1fr;
    margin: 3rem 0;
  }

  @media (min-width: 768px) {
    .entries {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      margin: 3rem 0;
    }
    :global(.entries article) {
      margin-right: 1rem;
    }
  }

  .about {
    margin-bottom: 2rem;
  }

  @media (min-width: 768px) {
    .hydrate {
      display: grid;
      grid-template-columns: 80% 20%;
    }
  }

  .hooks {
    display: grid;
    grid-template-columns: 100%;
  }

  @media (min-width: 768px) {
    .hooks {
      grid-template-columns: 50% 50%;
    }
  }
</style>

<svelte:head>
  <title>Home | hostadelic</title>
</svelte:head>

{#if data.testingHooks}
  <div class="banner">
    <p>Testing hooks worked</p>
    {#if data.cpus}
      <p>If you use Elder.js to build your site, it will span all {data.cpus.length} cpus listed below:</p>
      <ol>
        {#each data.cpus as cpu}
          <li>{cpu.model}</li>
        {/each}
      </ol>
    {/if}
  </div>
{/if}

<div class="banner">

  <h1>
    <img src="/logotype-groovy-1-darkalpha.png"
         alt="Hostadelic"
         style="width: auto; max-width: 100%" />
  </h1>

  <p> Opinionated DevOps shop. </p>

  <p> We're sharing our work here for reuse (time's pricey) and improvement.
Feel free to participate. We have no communication channel yet but a contact
page in the meantime. </p>

  <p> Don't stay tuned, go work. </p>

</div>

<div class="about">
  <h2> Repositories </h2>
  <p> We publish some code under a permissive license: </p>
  <div class="entries">
    {#each data.markdown.repo as article}
      <ArticleTeaser {article} rubrik="repo" {helpers} />
    {/each}
  </div>
  <ul>
</div>

<div class="blog">
  <h2> Articles </h2>
  <div class="entries">
    {#each data.markdown.blog as article}
      <ArticleTeaser {article} rubrik="blog" {helpers} />
    {/each}
  </div>
</div>
