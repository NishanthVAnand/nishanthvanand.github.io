---
layout: page
title: Publications
permalink: /publications/
background: /images/research.jpg
---
<head>
  <style>
    .papers {margin: 5pt; text-align: justify;}

    .arrow {
      border: solid #595959;
      border-width: 0 3pt 3pt 0;
      display: inline-block;
      padding: 4pt;
    }

    .right {
      transform: rotate(-45deg);
      -webkit-transform: rotate(-45deg);
    }

    .left {
      transform: rotate(135deg);
      -webkit-transform: rotate(135deg);
    }

    .up {
      transform: rotate(-135deg);
      -webkit-transform: rotate(-135deg);
    }

    .down {
      transform: rotate(45deg);
      -webkit-transform: rotate(45deg);
    }

    .format_abs {color: #404040; 
      font-style: oblique; 
      font-size: 13pt;}

    .author_format {color:  #404040;}
  </style>

  <script>
    function absFunc(div_id, anc_id) {
      var x = document.getElementById(div_id);
      var y = document.getElementById(anc_id);
      // if (y.className == "arrow down") { y.className = "arrow up";}
      // else {y.className == "arrow down";}
      if (x.style.display === "none") {
      x.style.display = "block";
      y.className = "arrow up";
      } else {
      x.style.display = "none";
      y.className = "arrow down";
      }
    } 
  </script>
</head>

Find my full research on <a style="color:blue;" href="https://scholar.google.com/citations?user=pRNasKQAAAAJ&hl=en">Google scholar</a>.

<ol>
  {% assign var = 1 %}
  {% for post in site.papers reversed %}
    <li class="papers">
       <b>{{post.title}}</b>. <i class="author_format">{{post.authors}}</i>. {{post.conference}}.
       {% if post.pdf %}[<a style="color:blue;" href="{{post.pdf}}">PDF</a>]{% endif %}
       {% if post.video %}[<a style="color:blue;" href="{{post.video}}">YouTube</a>]{% endif %}&nbsp;
       <a id="{{var | append: 'anchor'}}" class = "arrow down" onclick="absFunc('{{var}}', '{{var | append: 'anchor'}}')" style="color:blue;"> </a> 
       <div class = "format_abs" id="{{var}}" style="display: none;"> {{post.abstract}} </div> 
    </li>
    {% assign var = var | plus: 1  %}
  {% endfor %}
</ol>