---
layout: root
---
<div class="container-fluid p-5 m-0" style="background: url({{page.hero-page-image}}) center; background-size: cover;">
    <div class="container-fluid p-5 py-md-5" style="background-image: linear-gradient(to right, rgba(0, 0, 0, 0), rgba(255, 0, 0, 0));">
        <div class="container p-5 py-md-5">
            <div class="row py-3 py-md-3">
                <div class="col-md-7">
                </div>
            </div>
        </div>
    </div>
</div>
<div class="container-fluid bg-light py-3 py-md-5">
    <div class="container bg-light rounded p-3" style="position:relative;top:-11rem;">
        <nav aria-label="breadcrumb">
            <ol class="breadcrumb">
              <li class="breadcrumb-item"><a href="/index.html">Home</a></li>
              <li class="breadcrumb-item active" aria-current="page">{{page.title}}</li>
            </ol>
          </nav>
          <div class="row">
          <div class="col-md-4 col-lg-4">
            <img src="{{page.content-image}}" width="100%" style="margin-bottom:2rem;"/>
          </div>
          <div class="col-md-8 col-lg-8">
          <h1>{{page.title}}</h1>
            {{content}}
          </div>
            </div>
            </div>
</div>