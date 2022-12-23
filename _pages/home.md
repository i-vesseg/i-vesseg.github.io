---
title: "Home"
layout: default
sitemap: false
permalink: /
---

<div id="homeid" class="col-sm-7 col-xs-12">

## I-VESSEG:
#### Interactive and Collaborative Learning for Vessel Segmentation

<center>
 <!-- <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/group.jpg" width="100%"> -->
</center> 
<p></p>
I-VESSEG is an [ANR JCJC](https://anr.fr/en/call-for-proposals-details/call/programme-jeunes-chercheuses-et-jeunes-chercheurs-jcjc/) funded project that aims to develop a novel interactive and collaborative learning-based framework to close the gap that hampers the use of 3D vessel segmentation tools in clinical routine. 

The project will tackle three problems: 
1. The difficulty to collect large representative training samples.
2. The burden associated to manual labelling.
3. The poor generalization and reproducibility of current vessel extraction approaches. 

##### Clinical Use Cases
The final goal of I-VESSEG is to assure clinical translation. Its clinical value will be demonstrated in two clinical use cases: 
* **Multiple sclerosis (MS):** I-VESSEG will be used to estimate the central vein sign, an imaging biomarker in MS which refers to a vein visualized inside a white matter lesion on susceptibility-weighted images.
* **Stroke:** The I-VESSEG framework will assist the analysis of the cerebrovascular tree anatomy to detect intracranial stenosis, a major risk factor for stroke.

</div>
<div id="newsid" class="col-sm-5 col-xs-12" >
<div>
{% for member in site.data.pi %}
<div class="jumbotron">
   <center>
<!-- <a href="{{site.url}}{{site.baseurl}}/team"><img src="{{site.url}}{{site.baseurl}}/images/teampic/{{ member.photo }}" width="50%" style="block:inline; margin-left:auto; margin-right:auto; margin-bottom:5px;"/></a> -->
   <h5>PI: {{ member.name }}</h5>
   <h6>{{ member.info1 }}</h6>
   <h7>{{ member.info2 }}</h7><br>
   <h7>{{ member.info3 }}</h7>
<div style="margin-bottom:5px">
   {% if member.twitter %}<a href="{{ member.twitter }}" target="_blank"><i class="fa fa-twitter-square fa-2x"></i></a> {% endif %}
   {% if member.cmu %}<a href="{{ member.cmu }}" target="_blank"><i class="ai ai-archive-square ai-2x"></i></a> {% endif %}
   {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-2x"></i></a> {% endif %}
   {% if member.cv %} <a href="{{ site.url }}{{ site.baseurl }}/{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-2x"></i></a> {% endif %}
   {% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-2x"></i></a> {% endif %}
   {% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-2x"></i></a> {% endif %}
   {% if member.website %} <a href="{{ member.website }}" target="_blank"><i class="fa fa-external-link-square fa-2x"></i></a> {% endif %}
  </div>
  </center>
</div>
{% endfor %}
</div>

<div class="jumbotron">
<h2>News</h2>
  {% for article in site.data.news limit:7%}
  <b>{{ article.date }}</b>
    {{ article.headline }}
  {% endfor %}
  
  <h5><a href="{{ site.url }}{{ site.baseurl }}/allnews.html">... see all News</a></h5>
</div>
</div>
