# Markup

- abr: <abbr title="HyperText Markup Language">HTML</abbr>
- mark: (highlighting text e.g in search) Search results for <mark>'chicago'</mark>.
- del (for content that got deleted): I am an avid cyclist, <del cite="http://shayhowe.com" datetime="2012-07-01">skateboarder</del> and designer.
- s: (for content that’s not longer used e.g prise change) <s>$24.99</s> $19.99
- Time
    - <time>2011-08-24</time>
    - <time datetime="2011-08-24" pubdate>August 24th, 2011</time>
    - <time datetime="15:00">3pm</time>
    - <time datetime="2011-08-24T15:00">August 24th, 2011 at 3pm</time>
- Adress
<address>
  <strong>Shay Howe</strong><br>
  <a href="http://learn.shayhowe.com">http://learn.shayhowe.com</a><br>
  <a href="mailto:hello@awesome.com">hello@awesome.com</a><br>
  600 W. Chicago Ave.<br>
  Suite 620<br>
  Chicago, IL 60654<br>
  USA  
</address>
Code
    - Inline: Use the <code>article</code> element.
    - Block: <pre><code>body {
          color: #666;
          font: 14px/20px Arial, sans-serif;
        }</code></pre>
- wbr: word break.  http://shay<wbr>howe.com
- Cite, q, quote
- Small: <small>&copy; 2012 Shay Howe</small>
- Download Attribute <a href="twitter-logo.png" download="Logo">Twitter Logo</a>
- 




## Group of links

- https://www.w3.org/TR/WCAG20-TECHS/H48.html

```
<a name="categories" id="categories"></a><h2>Product Categories</h2>
<ul class="navigation">
    <li><a href="kitchen.html">Kitchen</a></li>
    <li><a href="bedbath.html">Bed &amp; Bath</a></li>
    <li><a href="dining.html">Fine Dining</a></li>
    <li><a href="lighting.html">Lighting</a></li>
    <li><a href="storage.html">Storage</a><li>
</ul> 
```


## Lists

If presented as a list but not list markup

```
<div class="list" role="list">
  <div role="listitem">first item</div>
  <div role="listitem">second item</div>
  <div role="listitem">third item</div>
</div>
```


## aria-labeledby for each section of the page. 

See full example. 
https://www.w3.org/WAI/tutorials/page-structure/example/

```
<nav aria-labelledby="mainnavheader">
  <h2 id="mainnavheader">Navigation Menu</h2>
    ...
```

```
<nav aria-labelledby="tocheader">
  <h3 id="tocheader">Table of Contents</h3>
    ...
```

```
<aside aria-labelledby="relatedheader">
  <h3 id="relatedheader">Related Articles</h3>
    ...
```

and maybe just for the screen reader
```
<nav aria-labelledby="mainmenulabel">
  <h2 id="mainmenulabel" class="visuallyhidden">Main Menu</h2>
</nav>
```


## Bread crumbs

https://gist.github.com/jonathantneal/4037764

```
// css
[aria-label="breadcrumbs"] [aria-hidden="true"]:after {
  content: "/";
}
// html
<nav role="navigation" aria-label="breadcrumbs">
  <a href="/">Home</a>
  <span aria-hidden="true"></span>
  <a href="/library">Library</a>
  <span aria-hidden="true"></span>
  <a href="">Data</a>
</nav>
```
