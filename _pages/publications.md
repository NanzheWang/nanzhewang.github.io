---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true




Publications
  - title: "Deep-learning-based inverse modeling approaches: A subsurface flow example"
    authors: "Nanzhe Wang, Haibin Chang, Dongxiao Zhang"
    venue: "Journal of Geophysical Research: Solid Earth"
    year: 2021
    url: "https://doi.org/10.1029/2020JB020549"
    

  - title: "Efficient uncertainty quantification for dynamic subsurface flow with surrogate by theory-guided neural network"
    authors: "Nanzhe Wang, Haibin Chang, Dongxiao Zhang"
    venue: "Computer Methods in Applied Mechanics and Engineering"
    year: 2021
    url: "https://doi.org/10.1016/j.cma.2020.113492"




---


{% assign sorted_pubs = page.publications | sort: 'year' | reverse %}
{% for pub in sorted_pubs %}
- <strong>{{ pub.authors }}</strong> ({{ pub.year }}).  
  <em>{{ pub.title }}</em>. *{{ pub.venue }}*.  
  {% if pub.url %}[Download Paper]({{ pub.url }}){% endif %}
  {% if pub.pdf %}| [PDF]({{ pub.pdf }}){% endif %}
{% endfor %}


{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}






<!--
{% include base_path %}
-->
<!-- New style rendering if publication categories are defined -->
<!--
{% if site.publication_category %}
  {% for category in site.publication_category  %}
    {% assign title_shown = false %}
    {% for post in site.publications reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}

-->
<!--
### Journal Publications
 
[1] **Wang, N.**, Zhang, D., Chang, H., & Li, H. (2020). Deep learning of subsurface flow via theory-guided neural network. Journal of Hydrology, 584, 124700.
    [[Download Paper]](https://doi.org/10.1016/j.jhydrol.2020.124700)



### Conference Proceedings 
-->
