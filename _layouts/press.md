---
layout: root
---
<div class="container-fluid bg-dark splash g-0">
<img src="{{page.splash}}" />
<div class="container-fluid">
<div class="container heading">
    <h1>{{page.title}}</h1>
</div>
</div>
</div>
<div class="container-fluid bg-light py-3 py-md-5">
    <div class="container bg-light rounded p-3">
    <div class="clearfix">&nbsp;</div>
        <nav aria-label="breadcrumb m-0">
            <ol class="breadcrumb">
              <li class="breadcrumb-item"><a href="/index.html">Home</a></li>
              <li class="breadcrumb-item"><a href="/press-releases.html">Press Releases</a></li>
              <li class="breadcrumb-item active" aria-current="page">{{page.title}}</li>
            </ol>
          </nav>
          <h2>{{page.hero-brief}}</h2>
            {{content}}
            <div class="row my-3">
    </div></div>
</div>