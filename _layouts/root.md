---
---
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>{{page.title}}</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-gH2yIJqKdNHPEq0n4Mqa/HGKIhSkIHeL5AyhkYV8i59U5AR6csBvApHHNl/vI1Bx" crossorigin="anonymous">
    <link href="/css/styles.css" rel="stylesheet">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
  </head>
  <body>
  <nav class="p-3 navbar header fixed-top navbar-expand-lg bg-light">
  <div class="container-fluid">
    <a class="navbar-brand py-3" href="/index.html"><img src="/BTIGreenTecLogo.png" style="
    display: inline-block;
    margin-top: -6px;
"> BTiGreenTec<span class="fs-6 fw-light" style="display:none;">™</span></a>
    <button class="navbar-toggler bg-light" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent" style="margin-top:0.25rem;">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
      {% for post in site.categories.leftnav %}
        <li class="nav-item">
          <a class="nav-link text-uppercase fw-bold" href="{{post.url}}">{{post.title}}</a>
        </li>
      {% endfor %}
      </ul>
      <ul class="navbar-nav">
      {% for post in site.categories.rightnav %}
        <li class="nav-item">
          <a class="nav-link" href="{{post.url}}">{{post.title}}</a>
        </li>
      {% endfor %}
        </ul>    </div>
  </div>
</nav>
    {{content}}

<div class="container-fluid bg-dark text-white-50 p-5 footer">
    <div class="row g-0">
        <div class="col-sm-12 col-md-3 text-center text-sm-center text-md-start g-0">
            <p class="py-3 text-light">[BTi Green Tec]&#8482;</p>
        </div>
        <div class="row col-sm-6 col-md-6 text-center text-md-start g-0 pb-3">
            <p class="text-uppercase fw-bold py-3 text-light">Quick Links</p>
            <div class="col-md-6 g-0">
                <ul class="navbar-nav">
                    <li class="nav-item"><a class="nav-link py-1" href="/index.html">Home</a></li>
                {% for post in site.categories.leftnav %}
                    <li class="nav-item"><a class="nav-link py-1" href="{{post.url}}">{{post.title}}</a></li>
                {% endfor %}
                </ul>
            </div>
            <div class="col-md-6 g-0">
                <ul class="navbar-nav">
                {% for post in site.categories.rightnav %}
                    <li class="nav-item"><a class="nav-link py-1" href="{{post.url}}">{{post.title}}</a></li>
                {% endfor %}
                {% for post in site.categories.other %}
                    <li class="nav-item"><a class="nav-link py-1" href="{{post.url}}">{{post.title}}</a></li>
                {% endfor %}
                </ul>
            </div>
        </div>
        <div class="col-sm-6 col-md-3 text-center text-md-start g-0 pb-3">
            <p class="text-uppercase fw-bold py-3 text-light">Stay in Touch</p>
            <p>Follow us on:</p>
            <p>
                <a href="#" class="fa fa-facebook text-dark text-decoration-none"></a>
                <a href="#" class="fa fa-twitter"></a>
                <a href="#" class="fa fa-google"></a>
                <a href="#" class="fa fa-linkedin"></a>
                <a href="#" class="fa fa-youtube"></a>
                <a href="#" class="fa fa-instagram"></a>
            </p>
        </div>
        <div class="col text-center text-sm-center text-md-start g-0">
            <p class="py-3">Copyright &copy; 2023 BTi Green Tec. Registered in England and Wales, UK. All rights reserved.</p>
        </div>        
    </div>
</div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js" integrity="sha384-A3rJD856KowSb7dwlZdYEkO39Gagi7vIsF0jrRAoQmDKKtQBHUuLZ9AsSv4jD4Xa" crossorigin="anonymous"></script>
    
        <script>
var scrollDir = (function (oldOffset, lastOffset, oldDir) {
    return function (offset) {

        var dir = offset < oldOffset;
        if (dir !== oldDir) {
            lastOffset = offset;
        } else {
            offset = offset - height;
        }
        oldOffset = offset;
        oldDir = dir;
        return {
            dir: dir,
            last: lastOffset
        };
    };
}());

var header = document.querySelector('.header');
var height = header.clientHeight;

$(window).scroll(function () {
    var scrollY = $(window).scrollTop();
    var dir = scrollDir(scrollY);
    var diff = dir.last - scrollY;

    var max = Math.max(-height, Math.min(height, diff));
    
    max = (dir.dir ? max - height : max); 
    max = scrollY<height?0:max;
    

    $('.header').data('size', 'small');
    $('.header').stop().animate({
        top: max
    }, 60);


});
        </script>
  </body>
</html>
