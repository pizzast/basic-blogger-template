Implement Blogger Markup Structure
========================

It's easy to make a structure of your template, you just need a make website structure using HTML.

.. code:: html

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

.. code:: xml

  <?xml version="1.0" encoding="UTF-8" ?>
  <!DOCTYPE html>
  <html b:version="2" class="v2" expr:dir="data:blog.languageDirection" xmlns="http://www.w3.org/1999/xhtml" xmlns:b="http://www.google.com/2005/gml/b" xmlns:data="http://www.google.com/2005/gml/data" xmlns:expr="http://www.google.com/2005/gml/expr" xmlns:og="http://ogp.me/ns#">
  <head>
  <meta charset="UTF-8"/>
  <title><data:blog.title/></title>
  </head>
  <body>
  <div id="wrapper">
  <header id="header-wrapper">
  <b:section class="header" id="header" maxwidgets="1">
  <b:widget id="Header1" locked="true" title="Basic Blogger Template (Header)" type="Header"></b:widget>
  </b:section>
  </header>
  <nav id="navigation">
  <ul>
  <li><a href="">Home</a></li>
  <li><a href="">About</a></li>
  </ul>
  </nav>
  <div class="clearfix"/>
  <section id="outer-wrapper">
  <article id="article-wrapper">
  <b:section class="main" id="main">
  <b:widget id="Blog1" locked="true" title="Blog Posting" type="Blog"></b:widget>
  </b:section>
  </article>
  </section>
  <div class="clearfix"/>
  <aside id="sidebar-wrapper">
  <b:section class="sidebar" id="sidebar" showaddelement="yes"></b:section>
  </aside>
  <div class="clearfix"/>
  <footer id="footer-wrapper">
  <b:section class="footer" id="footer" showaddelement="yes"></b:section>
  </footer>
  </div>
  </body>
  </html>

This is a basic markup structure, we need to add this markup to Blogger and save the template. After this blogger will generate a xml markup provided by

.. code:: xml

  <header id="header-wrapper">
  <b:section class="header" id="header" maxwidgets="1">
  <b:widget id="Header1" locked="true" title="Basic Blogger Template (Header)" type="Header"></b:widget>
  </b:section>
  </header>
  <article id="article-wrapper">
  <b:section class="main" id="main">
  <b:widget id="Blog1" locked="true" title="Blog Posting" type="Blog"></b:widget>
  </b:section>
  </article>
  <aside id="sidebar-wrapper">
  <b:section class="sidebar" id="sidebar" showaddelement="yes"></b:section>
  </aside>
  <footer id="footer-wrapper">
  <b:section class="footer" id="footer" showaddelement="yes"></b:section>
  </footer>

You cann't save these template because Blogger must have design/styling to succesfully save the template, for this solution we just use css reset by eric meyer

Here for full template

.. code:: xml
     
  <?xml version="1.0" encoding="UTF-8" ?>
  <!DOCTYPE html>
  <html b:version="2" class="v2" expr:dir="data:blog.languageDirection" xmlns="http://www.w3.org/1999/xhtml" xmlns:b="http://www.google.com/2005/gml/b" xmlns:data="http://www.google.com/2005/gml/data" xmlns:expr="http://www.google.com/2005/gml/expr" xmlns:og="http://ogp.me/ns#">
  <head>
  <meta charset="UTF-8"/>
  <title><data:blog.title/></title>
  
  <b:skin><![CDATA[
  /* Variable definitions
  =======================
  ]]></b:skin>
  
  <style type='text/css'>
  /*
  -----------------------------------------------
  Blogger Template Style
  Name		: Basic Blogger Template
  Designer	: Agus Purwantoro
  Release		: April 2018
  Version		: 1.0
  License		: MIT
  Email		: me@aguspurwantoro.com
  -----------------------------------------------
  Thanks to:
  - Eric Meyer (CSS Reset)
  */
  
  /* Eric Meyer&#39;s Reset CSS v2.0 (http://meyerweb.com/eric/tools/css/reset/)
  --------------------------------------------------------------------------------------- */
 html,body,div,span,applet,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,pre,a,abbr,acronym,address,big,cite,code,del,dfn,em,img,ins,kbd,q,s,samp,small,strike,strong,sub,sup,tt,var,b,u,i,center,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td,article,aside,canvas,details,embed,figure,figcaption,footer,header,hgroup,menu,nav,output,ruby,section,summary,time,mark,audio,video{margin:0;padding:0;border:0;font-size:100%;font:inherit;vertical-align:baseline}article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section{display:block}body{line-height:1}ol,ul{list-style:none}blockquote,q{quotes:none}blockquote:before,blockquote:after,q:before,q:after{content:&#39;&#39;;content:none}table{border-collapse:collapse;border-spacing:0}
  </style>
  </head>
  <body>
  <div id="wrapper">
  <header id="header-wrapper">
  <b:section class="header" id="header" maxwidgets="1">
  <b:widget id="Header1" locked="true" title="Basic Blogger Template (Header)" type="Header"></b:widget>
  </b:section>
  </header>
  <nav id="navigation">
  <ul>
  <li><a href="">Home</a></li>
  <li><a href="">About</a></li>
  </ul>
  </nav>
  <div class="clearfix"/>
  <section id="outer-wrapper">
  <article id="article-wrapper">
  <b:section class="main" id="main">
  <b:widget id="Blog1" locked="true" title="Blog Posting" type="Blog"></b:widget>
  </b:section>
  </article>
  </section>
  <div class="clearfix"/>
  <aside id="sidebar-wrapper">
  <b:section class="sidebar" id="sidebar" showaddelement="yes"></b:section>
  </aside>
  <div class="clearfix"/>
  <footer id="footer-wrapper">
  <b:section class="footer" id="footer" showaddelement="yes"></b:section>
  </footer>
  </div>
  </body>
  </html>

At this simple detailed guide, i wish you already understand how Blogger generate a xml markup.
