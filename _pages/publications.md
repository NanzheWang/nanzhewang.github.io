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

  - title: "Efficient uncertainty quantification and data assimilation via theory-guided convolutional neural network"
    authors:
     - "Nanzhe Wang"
     - "Haibin Chang"
     - "Dongxiao Zhang"
    venue: "SPE Journal"
    year: 2021
    pages: "1-29"
    url: "https://doi.org/10.2118/203904-PA"


  - title: "Deep learning based closed-loop well control optimization of geothermal reservoir with uncertain permeability"
    authors:
     - "Nanzhe Wang"
     - "Haibin Chang"
     - "Xiang-Zhao Kong"
     - "Dongxiao Zhang"
    venue: "Renewable Energy"
    year: 2023
    volume: 211
    pages: "379-394"
    url: "https://doi.org/10.1016/j.renene.2023.04.088"


  - title: "Inverse modeling for subsurface flow based on deep learning surrogates and active learning strategies"
    authors:
     - "Nanzhe Wang"
     - "Haibin Chang"
     - "Dongxiao Zhang"
    venue: "Water Resources Research"
    year: 2023
    volume: 59
    issue: 7
    pages: "e2022WR033644"
    url: "https://doi.org/10.1029/2022WR033644"


  - title: "Physics‐Informed Convolutional Decoder (PICD): A novel approach for direct inversion of heterogeneous subsurface flow"
    authors:
     - "Nanzhe Wang"
     - "Xiang‐Zhao Kong"
     - "Dongxiao Zhang"
    venue: "Geophysical Research Letters"
    year: 2024
    volume: 51
    issue: 13
    pages: "e2024GL108163"
    url: "https://doi.org/10.1029/2024GL108163"


  - title: "Deep-learning-based upscaling method for geologic models via theory-guided convolutional neural network"
    authors:
     - "Nanzhe Wang"
     - "Qinzhuo Liao"
     - "Haibin Chang"
     - "Dongxiao Zhang"
    venue: "Computational Geosciences"
    year: 2023
    volume: 27
    issue: 6
    pages: "913-938"
    url: "https://doi.org/10.1007/s10596-023-10233-2"

  - title: "Deep learning framework for history matching CO2 storage with 4D seismic and monitoring well data"
    authors:
     - "Nanzhe Wang"
     - "Louis J. Durlofsky"
    venue: "Geoenergy Science and Engineering"
    year: 2025
    pages: 213736
    url: "https://doi.org/10.1016/j.geoen.2025.213736"


  - title: "A comprehensive review of physics-informed deep learning and its applications in geoenergy development"
    authors:
     - "Nanzhe Wang"
     - "Yuntian Chen"
     - "Dongxiao Zhang"
    venue: "The Innovation Energy"
    year: 2025
    volume: 2
    issue: 2
    pages: "100087-1-100087-15"
    url: "https://doi.org/10.59717/j.xinn-energy.2025.100087"

---


{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}


### Journal Publications
{% assign my_name = "Nanzhe Wang" %}
{% assign sorted_pubs = page.publications | sort: 'year' | reverse %}
{% for pub in sorted_pubs %}
  {% assign author_line = "" %}
  {% for author in pub.authors %}
    {% if author == my_name %}
      {% assign formatted_author = "<strong>" | append: author | append: "</strong>" %}
    {% else %}
      {% assign formatted_author = author %}
    {% endif %}
    {% if forloop.last %}
      {% assign author_line = author_line | append: formatted_author %}
    {% else %}
      {% assign author_line = author_line | append: formatted_author | append: "; " %}
    {% endif %}
  {% endfor %}
- {{ author_line }} ({{ pub.year }}). <em>{{ pub.title }}</em>. *{{ pub.venue }}*{% if pub.volume %}, <strong>{{ pub.volume }}</strong>{% endif %}{% if pub.issue %}({{ pub.issue }}){% endif %}{% if pub.pages %}: {{ pub.pages }}{% endif %}.  
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
