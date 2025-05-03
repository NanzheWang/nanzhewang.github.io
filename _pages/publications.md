---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true




publications:
  - title: "Deep-learning-based inverse modeling approaches: A subsurface flow example"
    authors:
     - "Nanzhe Wang"
     - "Haibin Chang"
     - "Dongxiao Zhang"
    venue: "Journal of Geophysical Research: Solid Earth"
    year: 2021
    volume: 126
    issue: 2
    pages: "e2020JB020549"
    url: "https://doi.org/10.1029/2020JB020549"
    

  - title: "Efficient uncertainty quantification for dynamic subsurface flow with surrogate by theory-guided neural network"
    authors:
     - "Nanzhe Wang"
     - "Haibin Chang"
     - "Dongxiao Zhang"
    venue: "Computer Methods in Applied Mechanics and Engineering"
    year: 2021
    volume: 373
    pages: "113492"
    url: "https://doi.org/10.1016/j.cma.2020.113492"



  - title: "Deep learning of subsurface flow via theory-guided neural network"
    authors:
     - "Nanzhe Wang"
     - "Dongxiao Zhang"
     - "Haibin Chang"
     - "Heng Li"
    venue: "Journal of Hydrology"
    year: 2020
    volume: 584
    pages: 124700
    url: "https://doi.org/10.1016/j.jhydrol.2020.124700"

  - title: "Theory-guided auto-encoder for surrogate construction and inverse modeling"
    authors:
     - "Nanzhe Wang"
     - "Haibin Chang"
     - "Dongxiao Zhang"
    venue: "Computer Methods in Applied Mechanics and Engineering"
    year: 2021
    volume: 385
    pages: "114037"
    url: "https://doi.org/10.1016/j.cma.2021.114037"


  - title: "Efficient well placement optimization based on theory-guided convolutional neural network"
    authors:
     - "Nanzhe Wang"
     - "Haibin Chang"
     - "Dongxiao Zhang"
     - "Liang Xue"
     - "Yuntian Chen"
    venue: "Journal of Petroleum Science and Engineering"
    year: 2022
    volume: 208
    pages: "109545"
    url: "https://doi.org/10.1016/j.petrol.2021.109545"

  - title: "Surrogate and inverse modeling for two-phase flow in porous media via theory-guided convolutional neural network"
    authors:
     - "Nanzhe Wang"
     - "Haibin Chang"
     - "Dongxiao Zhang"
    venue: "Journal of Computational Physics"
    year: 2022
    volume: 466
    pages: "111419"
    url: "https://doi.org/10.1016/j.jcp.2022.111419"


---


{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}


### Journal Publications
{% assign my_name = "Nanzhe Wang" %}
{% assign sorted_pubs = page.publications | sort: 'year' | reverse %}
{% for pub in sorted_pubs %}
- {% for author in pub.authors %}
    {% if author == my_name %}
      <strong>{{ author }}</strong>{% unless forloop.last %}; {% endunless %}
    {% else %}
      {{ author }}{% unless forloop.last %}; {% endunless %}
    {% endif %}
  {% endfor %} ({{ pub.year }}).  
  <em>{{ pub.title }}</em>. *{{ pub.venue }}*{% if pub.volume %}, <strong>{{ pub.volume }}</strong>{% endif %}{% if pub.issue %}({{ pub.issue }}){% endif %}{% if pub.pages %}: {{ pub.pages }}{% endif %}.  
  {% if pub.url %}[Download Paper]({{ pub.url }}){% endif %}
  {% if pub.pdf %}| [PDF]({{ pub.pdf }}){% endif %}
{% endfor %}



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
