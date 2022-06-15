---
layout: default
---

<div class="bib">
{% bibliography --file mcmi.bib --file ds.bib %}
</div>

<script type="text/javascript">
  document.addEventListener("DOMContentLoaded", function(event) {
    var urlParts   = document.URL.split('#');
    if (urlParts.length > 1) {
        var anchor = decodeURIComponent(urlParts[1]);
        var bibitems = document.querySelectorAll('ol.bibliography li');
        bibitems.forEach(el => el.style.display = 'none');
        bibitems.forEach(el => {
            if(el.innerText.includes(anchor)) {
                el.style.display = 'inline';
            }
        });
    }
  });
</script>