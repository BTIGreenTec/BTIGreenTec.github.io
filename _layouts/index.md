---
layout: root
---
<div class="container-fluid bg-light g-0">
<div class="container-fluid g-0">
<div id="carouselExampleSlidesOnly" class="carousel slide" data-bs-ride="carousel" data-bs-interval="5000" >
  <div class="carousel-inner">
      {% assign isfirst = true %}
      {% for post in site.categories.leftnav %}
        <div class="carousel-item {% if isfirst == true %}active{% endif %}">
      <img src="{{post.hero-image}}" class="d-block w-100" alt="...">
      <div class="carousel-caption">
        <h5>{{post.hero-heading}}</h5>
        <p>{{post.hero-brief}}</p>
        <a class="btn btn-outline-light" href="{{post.url}}" role="button">{{post.hero-button}}</a>
      </div>
    </div>
      {% assign isfirst = false %}
      {% endfor %}
    
  </div>
</div>
</div>

<div class="container-fluid pt-5">
  <div class="container py-5">
    {{content}}
  </div>
</div>

      {% for post in site.categories.leftnav %}
      {% assign remainder = forloop.index | modulo: 2 %}
  <div class="container py-5 text-light subsection g-5">
    <div class="row" style="background-color:{{post.subsection-color}}">
      {% if remainder == 1 %}
      <div class="col-md-6 p-5 my-5">
        <div class="p-5">
          <h2>{{post.subsection-heading}}</h2>
          <p>{{post.subsection-brief}}</p>
          <a class="btn btn-outline-light" href="{{post.url}}" role="button">{{post.subsection-button}}</a>
        </div>
      </div>
      <div class="col-md-6 bg-primary text-light g-0 d-none d-sm-none d-md-block">
        <img src="{{post.subsection-image}}" class="d-block w-100" alt="...">
      </div>
      {% else %}
      <div class="col-md-6 bg-primary text-light g-0 d-none d-sm-none d-md-block">
        <img src="{{post.subsection-image}}" class="d-block w-100" alt="...">
      </div>
      <div class="col-md-6 p-5 my-5">
        <div class="p-5">
          <h2>{{post.subsection-heading}}</h2>
          <p>{{post.subsection-brief}}</p>
          <a class="btn btn-outline-light" href="{{post.url}}" role="button">{{post.subsection-button}}</a>
        </div>
      </div>
      
      {% endif %}
    </div>
  </div>
    
      {% if forloop.index == 1 %}
      <div class="container-fluid p-3 py-5 p-sm-5 text-light subsection-press">
  <div class="row">
    <h3 class="col-9 col-md-10 fs-3 fw-lighter">Press Releases</h3>
    <a class="mb-4 col-3 col-md-2 btn btn-outline-light" role="button">View All</a>
    {% for post in site.categories.press limit:4 %}
    <div class="py-3 col-lg-3 col-md-6 col-sm-6">
      <p class="fs-6 fw-lighter">{{ post.date | date: '%B %d, %Y' }}</p>
      <p><a href="{{post.url}}" class="text-decoration-none text-light">{{post.brief}}</a></p>
    </div>
    {% endfor %}
  </div>
</div>

      {% endif %}

            {% if forloop.index == 2 %}
      <div class="container-fluid p-3 py-5 p-sm-5 text-light subsection-blog">
  <div class="row">
    <h3 class="col-9 col-md-10 fs-3 fw-lighter">Blog Posts</h3>
    <a class="mb-4 col-3 col-md-2 btn btn-outline-light" role="button">View All</a>
    {% for post in site.categories.press limit:4 %}
    <div class="py-3 col-lg-3 col-md-6 col-sm-6">
      <p class="fs-6 fw-lighter">{{ post.date | date: '%B %d, %Y' }}</p>
      <p><a href="{{post.url}}" class="text-decoration-none text-light">{{post.title}}</a></p>
    </div>
    {% endfor %}
  </div>
</div>

      {% endif %}

      {% endfor %}



</div>