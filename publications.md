---
layout: default
nav_active: publications
---

<input id="filter" type="text" size=20 placeholder="filter..." />
<div class="bib">
{% bibliography -f bco.bib -f mcmi.bib -f ds.bib -f diair.bib -f mml.bib -f tml.bib -f kei.bib -f ait.bib -f accr.bib --remove_duplicates %}
</div>

<script type="text/javascript">
  function filter(text) {
    text = text.toLowerCase();
    var bibitems = document.querySelectorAll('ol.bibliography li');
    bibitems.forEach(el => el.style.display = 'none');
    bibitems.forEach(el => {
      var c = el.children;
      var tmp = c[c.length -1].value.toLowerCase();
      if(tmp.includes(text)) {
        el.style.display = 'inline';
      }
    });
  };
  document.addEventListener("DOMContentLoaded", function(event) {
    document.querySelector('#filter').addEventListener('input', (e) => {
      filter(document.querySelector('#filter').value);
    });
    var urlParts   = document.URL.split('#');
    if (urlParts.length > 1) {
        var anchor = decodeURIComponent(urlParts[1]);
        document.querySelector('#filter').value = anchor;
        filter(anchor);
    }
  });
</script>