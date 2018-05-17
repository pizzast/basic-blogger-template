# Basic Blogger Template

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![Documentation Status](https://readthedocs.org/projects/basic-blogger-template/badge/?version=latest)](http://basic-blogger-template.readthedocs.io/en/latest/?badge=latest) 
[![Basic Blogger Template](https://img.shields.io/appveyor/ci/gruntjs/grunt.svg)](https://github.com/meagusp/basic-blogger-template/blob/master/cleantemplate.xml)

This template is built from scratch with schema markup,  i use schema because this help search engine understand the part of the website structure and help indexing in search engine. And i use open graph protocol for help social media i.e facebook to scraping and make preview for blog posting.

### Getting Started

Please review the markup structure before editing and make any changes using this template.

~~~
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:version='2' class='v2' expr:dir='data:blog.languageDirection' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr' xmlns:og='http://ogp.me/ns#'>
<head>
<meta charset='UTF-8'/>
<title><data:blog.title/></title>
</head>
<body>
<div id='wrapper'>
<header id='header-wrapper'>
<b:section class='header' id='header' maxwidgets='1'>
<b:widget id='Header1' locked='true' title='Basic Blogger Template (Header)' type='Header'></b:widget>
</b:section>
</header>
<nav id='navigation'>
<ul>
<li><a href=''>Home</a></li>
<li><a href=''>About</a></li>
</ul>
</nav>
<div class='clearfix'/>
<section id='outer-wrapper'>
<article id='article-wrapper'>
<b:section class='main' id='main'>
<b:widget id='Blog1' locked='true' title='Blog Posting' type='Blog'></b:widget>
</b:section>
</article>
</section>
<div class='clearfix'/>
<aside id='sidebar-wrapper'>
<b:section class='sidebar' id='sidebar' showaddelement='yes'></b:section>
</aside>
<div class='clearfix'/>
<footer id='footer-wrapper'>
<b:section class='footer' id='footer' showaddelement='yes'></b:section>
</footer>
</div>
</body>
</html>
~~~

### Debugging

* [Structured Data Testing Tool](https://search.google.com/structured-data/testing-tool?hl=id)
* [Open Graph Debugger](https://developers.facebook.com/tools/debug/)

### Technologies

* [Open Graph Protocol](http://ogp.me/)
* [Schema](http://schema.org/)


### Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

### Prerequisite

* HTML & CSS
* XML
* Javascript & Jquery (optional, if you need your Blog more interractive you need a Javascript, Jquery).

### Authors

* Agus Purwantoro *initial work* - [meagusp](https://github.com/meagusp)

### License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
