<script>
  export let article;
  export let rubrik;
  export let helpers;
</script>

<style>
a, article { padding: 0; }
article {
  margin-bottom: 1rem;
  font-weight: bolder;
  border-width: 0.20rem;
  border-style: solid;
  border-image: linear-gradient(
      90deg,
      rgba(90, 140, 180, 1) 0%,
      rgba(120, 60, 120, 1) 15%,
      rgba(180, 60, 120, 1) 85%,
      rgba(220, 90, 180, 1) 100%
  ) 1;
  background-color: #e0e0f0;
}
h1 {
  display: block;
  margin: 0;
  padding: 0.5rem 1rem;
  color: white;
  background-image: linear-gradient(
      90deg,
      rgba(90, 140, 180, 1) 0%,
      rgba(120, 60, 120, 1) 15%,
      rgba(180, 60, 120, 1) 85%,
      rgba(220, 90, 180, 1) 100%
  );
}
section {
  padding: 1rem;
}
</style>

<a href={helpers.permalinks[rubrik]({ slug: article.slug })}>
  <article>
    <h1>{article.frontmatter.title}</h1>
    <section>
      <p>{article.frontmatter.excerpt}</p>
      {#if article.frontmatter.license}<p>{article.frontmatter.license}</p>{/if}
    </section>
  </article>
</a>
