Implement Blogger Markup Structure
========================

It's easy to make a structure of your template, you just need a make website structure using HTML.

I will make a example of this::

<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8"/>
<title>Website Structure</title>
</head>
<body>
<div id="wrapper">
<header id="header-wrapper">
</header>
<nav id="navigation">
<ul>
<li><a href="">Home</a></li>
<li><a href="">About</a></li>
</ul>
</nav>
<div class='clearfix'/>
<section id="outer-wrapper">
<article id="article-wrapper">
</article>
</section>
<div class='clearfix'/>
<aside id="sidebar-wrapper">
</aside>
<div class='clearfix'/>
<footer id="footer-wrapper">
</footer>
</div>
</body>
</html>

But, Blogger use XML to process, how do implement a HTML markup into XML markup? 

here it's::

<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:version='2' class='v2' expr:dir='data:blog.languageDirection' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr' xmlns:og='http://ogp.me/ns#'>
<head>
<meta charset="UTF-8"/>
<title><data:blog.title/></title>
</head>
<body>
<div id="wrapper">
<header id="header-wrapper">
<b:section class='header' id='header' maxwidgets='1'>
<b:widget id='Header1' locked='true' title='Basic Blogger Template (Header)' type='Header'></b:widget>
</b:section>
</header>
<nav id="navigation">
<ul>
<li><a href="">Home</a></li>
<li><a href="">About</a></li>
</ul>
</nav>
<div class='clearfix'/>
<section id="outer-wrapper">
<article id="article-wrapper">
<b:section class='main' id='main'>
<b:widget id='Blog1' locked='true' title='Blog Posting' type='Blog'></b:widget>
</b:section>
</article>
</section>
<div class='clearfix'/>
<aside id="sidebar-wrapper">
<b:section class='sidebar' id='sidebar' showaddelement='yes'></b:section>
</aside>
<div class='clearfix'/>
<footer id="footer-wrapper">
<b:section class='footer' id='footer' showaddelement='yes'></b:section>
</footer>
</div>
</body>
</html>

This is a basic markup structure, we need to add this markup to Blogger and save the template. After this blogger will generate a xml markup provided by::

<header id="header-wrapper">
<b:section class='header' id='header' maxwidgets='1'>
<b:widget id='Header1' locked='true' title='Basic Blogger Template (Header)' type='Header'></b:widget>
</b:section>
</header>
<article id="article-wrapper">
<b:section class='main' id='main'>
<b:widget id='Blog1' locked='true' title='Blog Posting' type='Blog'></b:widget>
</b:section>
</article>
</section>
<div class='clearfix'/>
<aside id="sidebar-wrapper">
<b:section class='sidebar' id='sidebar' showaddelement='yes'></b:section>
</aside>
<div class='clearfix'/>
<footer id="footer-wrapper">
<b:section class='footer' id='footer' showaddelement='yes'></b:section>
</footer>

At this simple detailed guide, i wish you already understand how Blogger generate a xml markup.
