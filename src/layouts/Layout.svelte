<script>
  import style from '../../assets/style.css';
  export let templateHtml, settings;
</script>

<style>
  :global(h1) {
    font-style: italic;
  }
  .container {
    max-width: 900px;
    margin: 0 auto;
    padding: 1rem;
  }

  :root {
    --balloon-color: #0639fa;
    --balloon-font-size: 14px;
  }
  .footer {
    padding: 0.5rem 0;
    background: #06397a;
    padding-top: 0.667rem;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans',
      'Helvetica Neue', sans-serif;
    color: #f4f7fb;
    text-align: center;
    font-size: 14px;
  }
  .footer a {
    color: #f4f7fb;
  }
  :global(ul li),
  :global(ol li) {
    margin-bottom: 0.3rem;
  }
</style>

<div class="container">
  {@html templateHtml}
</div>
<div class="footer" style="margin-top: 0">
  <span style="color:#f0b040; font-size: 120%"> Built </span>
  in
  <span style="color:#c050ff; font-size: 120%"> peace </span>
  with
  <span style="color:#b0f040; font-size: 133%"> ❤ </span>
  and under
  <span style="color:#ff4020; font-size: 133%"> © </span>
</div>
