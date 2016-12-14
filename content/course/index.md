---
date: 2016-12-07T14:36:21-08:00
title: Course
weight: 60
---

## Latex

To enable MathJax rendering of $\LaTeX$ on your entire website, include the following snippet in the footer of your page.
```
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    extensions: ["tex2jax.js"],
    jax: ["input/TeX", "output/HTML-CSS"],
    tex2jax: {
      inlineMath: [ ['$','$'] ],
      displayMath: [ ['$$','$$'] ],
      processEscapes: true
    },
    "HTML-CSS": { availableFonts: ["TeX"] }
  });
</script>
<script type="text/javascript"
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js">
</script>
```
The simplest way to do this, if you have not changed the footer included with your theme yet, is to copy `/themes/your-theme/layouts/partials/footer.html` to `/layouts/partials/footer.html` and add the snipet to this copy.

To use Latex in-line, surround it with dollar signs: `$\LaTeX$` becomes $\LaTeX$. For full equations use `$$ - $$`, so for example
```
$$ \zeta(s) = \sum_{n=1}^\infty \frac{1}{n^s} $$
```
becomes
$$ \zeta(s) = \sum_{n=1}^\infty \frac{1}{n^s} $$

If issues arise from underscores disappearing, it might be Markdown interpreting them as _emphasis_ added to words. In this case try replacing your `_` with `\_`.

## Mermaid

To enable mermaid.js, first we need to place `mermaid.min.js` at `/static/js/mermaid.min.js` or a similar location. Then, we need to create a shortcode, namely `/layouts/shortcodes/mermaid.html` with the following content:
```
<script src="/js/mermaid.min.js"></script>
<script>mermaid.initialize({startOnLoad:true});</script>
<div class="mermaid">
{{ .Inner }}
</div>
```

Then, to use mermaid simply enclose your mermaid code in `{{</* mermaid */>}}` and `{{</* /mermaid */>}}`. For example,
```
{{</* mermaid */>}}
sequenceDiagram
A->> B: Query
B->> C: Forward query
Note right of C: Thinking...
C->> B: Response
B->> A: Forward response
{{</* /mermaid */>}}
```
produces
{{< mermaid >}}
sequenceDiagram
A->> B: Query
B->> C: Forward query
Note right of C: Thinking...
C->> B: Response
B->> A: Forward response
{{< /mermaid >}}

## Gist

To embed a GitHub Gist, we once again add a shortcode `/layouts/shortcodes/gist.html` containing
```
<script type="text/javascript" src="http://gist.github.com/{{ .Get 0 }}.js"></script>
```
Then to embed simply type `{{</* gist HASH-OF-GIST */>}}`. For example, a Gis with hash `d34f252414de858be26d40908067a00c` can be embedded with `{{</* gist d34f252414de858be26d40908067a00c */>}}` to give:
 {{< gist d34f252414de858be26d40908067a00c >}}

