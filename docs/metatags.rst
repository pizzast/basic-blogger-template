Implement Meta Tags For Blogger
========================

Meta tags help us and search engine to understand your blog, implementing meta tags is very important.

By implement meta tags to your template you already help the search engine and visitor to understand your blog.

Basic Blogger Meta Tags
~~~~~~~~~~~~~~~~~~~~~~~

At the previous guide the meta tags is

.. code:: xml

  <meta charset="UTF-8"/>
  <title><data:blog.title/></title>

This a good place to start but we need a **further optimization** including seo *title tags*, *seo meta tags*, *blogger optimized meta tags*, and *open graph meta tags*.

Canonical Url
~~~~~~~~~~~~~

.. code:: xml

  <link expr:href='data:blog.canonicalUrl' rel='canonical'/>

Internet Explorer
~~~~~~~~~~~~~~~~

.. code:: xml

  <!--[if lt IE 9]>
  <script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"> </script>
  <![endif]-->
  <meta content='width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1' name='viewport'/>
  <meta content='text/html;charset=UTF-8' http-equiv='Content-Type'/>
  <meta content='IE=edge,chrome=1' http-equiv='X-UA-Compatible'/> 
  <b:include data='blog' name='all-head-content'/>

Blogger Optimized Meta Tags
~~~~~~~~~~~~~~~~~~~~~~~~~~~

This meta tags is optimized for Blogger, this is very important for your blog because have a **function**.

here it's:

.. code:: xml

  <link expr:href='data:blog.homepageUrl + &quot;favicon.ico&quot;' rel='icon' type='image/x-icon'/>
  <link expr:href='data:blog.url' rel='canonical'/>
  <link expr:href='data:blog.homepageUrl + &quot;feeds/posts/default&quot;' expr:title='data:blog.title + &quot; - Atom&quot;' rel='alternate' type='application/atom+xml'/>
  <link expr:href='data:blog.homepageUrl + &quot;feeds/posts/default?alt=rss&quot;' expr:title='data:blog.title + &quot; - RSS&quot;' rel='alternate' type='application/rss+xml'/>
  <link expr:href='&quot;http://www.blogger.com/feeds/&quot; + data:blog.blogId + &quot;/posts/default&quot;' expr:title='data:blog.title + &quot; - Atom&quot;' rel='alternate' type='application/atom+xml'/>
  <link href='http://www.blogger.com/openid-server.g' rel='openid.server'/>
  <link expr:href='data:blog.homepageUrl' rel='openid.delegate'/>
  <b:if cond='data:blog.isMobile'>
  <meta content='noindex,nofollow' name='robots'/>
  </b:if>
  <b:if cond='data:blog.pageType == &quot;item&quot;'>
  <b:if cond='data:blog.postImageThumbnailUrl'>
  <link expr:href='data:blog.postImageThumbnailUrl' rel='image_src'/>
  </b:if>
  </b:if>

SEO Title Tags
~~~~~~~~~~~~~~

SEO title tags help search engine to understand the title for your homepage, blog posting, archives, etc. 

here it's:

.. code:: xml

  <b:if cond='data:blog.url == data:blog.homepageUrl'><title><data:blog.title/></title></b:if>
  <b:if cond='data:blog.pageType == &quot;item&quot;'><title><data:blog.pageName/> - <data:blog.title/></title></b:if>
  <b:if cond='data:blog.pageType == &quot;archive&quot;'><title>Archive for <data:blog.pageName/></title></b:if>
  <b:if cond='data:blog.pageType == &quot;static_page&quot;'><title><data:blog.pageName/></title></b:if>
  <b:if cond='data:blog.pageType == &quot;index&quot;'><b:if cond='data:blog.searchLabel'><title><data:blog.title/> - <data:blog.pageName/></title></b:if></b:if>
  <b:if cond='data:blog.pageType == &quot;error_page&quot;'><title>Page Not Found</title></b:if>
  <b:if cond='data:blog.pageType == &quot;index&quot;'><b:if cond='data:blog.url != data:blog.homepageUrl'><title><data:blog.pageTitle/> - All Post</title></b:if></b:if>

SEO Meta Tags
~~~~~~~~~~~~~

This meta tags is **optional** but i recommend you to use this.

here it's:

.. code:: xml

  <meta content='width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1' name='viewport'/>
  <meta content='IE=edge,chrome=1' http-equiv='X-UA-Compatible'/>
  <meta content='blogger' name='generator'/>
  <meta content='indonesian' name='language'/>
  <meta content='id' name='geo.country'/>
  <meta content='indonesia' name='geo.placename'/>
  <meta content='Author' name='author'/>
  <meta content='index,follow' name='robots'/>
  <meta content='2 days' name='revisit-after'/>
  <meta content='2 days' name='revisit'/>
  <meta content='never' name='expires'/>
  <meta content='always' name='revisit'/>
  <meta content='global' name='distribution'/>
  <meta content='general' name='rating'/>
  <meta content='true' name='MSSmartTagsPreventParsing'/>
  <meta content='text/html; charset=UTF-8' http-equiv='Content-Type'/>
  <meta content='index, follow' name='googlebot'/>
  <meta content='follow, all' name='Googlebot-Image'/>
  <meta content='follow, all' name='msnbot'/>
  <meta content='follow, all' name='Slurp'/>
  <meta content='follow, all' name='ZyBorg'/>
  <meta content='follow, all' name='Scooter'/>
  <meta content='all' name='spiders'/>
  <meta content='all' name='WEBCRAWLERS'/>
  <meta content='aeiwi, alexa, alltheWeb, altavista, aol netfind, anzwers, canada, directhit, euroseek, excite, overture, go, google, hotbot. infomak, kanoodle, lycos, mastersite, national directory, northern light, searchit, simplesearch, Websmostlinked, webtop, what-u-seek, aol, yahoo, webcrawler, infoseek, excite, magellan, looksmart, bing, cnet, googlebot' name='search engines'/>
  
Here's the full of code:

.. code:: xml
     
  <?xml version="1.0" encoding="UTF-8" ?>
  <!DOCTYPE html>
  <html b:version='2' class='v2' expr:dir='data:blog.languageDirection' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr' xmlns:og='http://ogp.me/ns#'>
  <head>
  <meta charset='UTF-8'/>
  
  <!-- Blogger Optimized Meta Tags -->
  <link expr:href='data:blog.homepageUrl + &quot;favicon.ico&quot;' rel='icon' type='image/x-icon'/>
  <link expr:href='data:blog.url' rel='canonical'/>
  <link expr:href='data:blog.homepageUrl + &quot;feeds/posts/default&quot;' expr:title='data:blog.title + &quot; - Atom&quot;' rel='alternate' type='application/atom+xml'/>
  <link expr:href='data:blog.homepageUrl + &quot;feeds/posts/default?alt=rss&quot;' expr:title='data:blog.title + &quot; - RSS&quot;' rel='alternate' type='application/rss+xml'/>
  <link expr:href='&quot;http://www.blogger.com/feeds/&quot; + data:blog.blogId + &quot;/posts/default&quot;' expr:title='data:blog.title + &quot; - Atom&quot;' rel='alternate' type='application/atom+xml'/>
  <link href='http://www.blogger.com/openid-server.g' rel='openid.server'/>
  <link expr:href='data:blog.homepageUrl' rel='openid.delegate'/>
  <b:if cond='data:blog.isMobile'>
  <meta content='noindex,nofollow' name='robots'/>
  </b:if>
  <b:if cond='data:blog.pageType == &quot;item&quot;'>
  <b:if cond='data:blog.postImageThumbnailUrl'>
  <link expr:href='data:blog.postImageThumbnailUrl' rel='image_src'/>
  </b:if>
  </b:if>

  <!-- SEO Title Tag -->
  <b:if cond='data:blog.url == data:blog.homepageUrl'><title><data:blog.title/></title></b:if>
  <b:if cond='data:blog.pageType == &quot;item&quot;'><title><data:blog.pageName/> - <data:blog.title/></title></b:if>
  <b:if cond='data:blog.pageType == &quot;archive&quot;'><title>Archive for <data:blog.pageName/></title></b:if>
  <b:if cond='data:blog.pageType == &quot;static_page&quot;'><title><data:blog.pageName/></title></b:if>
  <b:if cond='data:blog.pageType == &quot;index&quot;'><b:if cond='data:blog.searchLabel'><title><data:blog.title/> - <data:blog.pageName/></title></b:if></b:if>
  <b:if cond='data:blog.pageType == &quot;error_page&quot;'><title>Page Not Found</title></b:if>
  <b:if cond='data:blog.pageType == &quot;index&quot;'><b:if cond='data:blog.url != data:blog.homepageUrl'><title><data:blog.pageTitle/> - All Post</title></b:if></b:if>

  <!-- SEO Meta Tag -->
  <meta content='width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1' name='viewport'/>
  <meta content='IE=edge,chrome=1' http-equiv='X-UA-Compatible'/>
  <meta content='blogger' name='generator'/>
  <meta content='indonesian' name='language'/>
  <meta content='id' name='geo.country'/>
  <meta content='indonesia' name='geo.placename'/>
  <meta content='Author' name='author'/>
  <meta content='index,follow' name='robots'/>
  <meta content='2 days' name='revisit-after'/>
  <meta content='2 days' name='revisit'/>
  <meta content='never' name='expires'/>
  <meta content='always' name='revisit'/>
  <meta content='global' name='distribution'/>
  <meta content='general' name='rating'/>
  <meta content='true' name='MSSmartTagsPreventParsing'/>
  <meta content='text/html; charset=UTF-8' http-equiv='Content-Type'/>
  <meta content='index, follow' name='googlebot'/>
  <meta content='follow, all' name='Googlebot-Image'/>
  <meta content='follow, all' name='msnbot'/>
  <meta content='follow, all' name='Slurp'/>
  <meta content='follow, all' name='ZyBorg'/>
  <meta content='follow, all' name='Scooter'/>
  <meta content='all' name='spiders'/>
  <meta content='all' name='WEBCRAWLERS'/>
  <meta content='aeiwi, alexa, alltheWeb, altavista, aol netfind, anzwers, canada, directhit, euroseek, excite, overture, go, google, hotbot. infomak, kanoodle, lycos, mastersite, national directory, northern light, searchit, simplesearch, Websmostlinked, webtop, what-u-seek, aol, yahoo, webcrawler, infoseek, excite, magellan, looksmart, bing, cnet, googlebot' name='search engines'/>

  <b:skin><![CDATA[

  /* Variable definitions
  =======================

  ]]></b:skin>

  <style type='text/css'>
  /*
  -----------------------------------------------
  Blogger Template Style
  Name         : Basic Blogger Template
  Designer     : Agus Purwantoro
  Release      : April 2018
  Version      : 1.0
  License      : MIT
  Email        : me@aguspurwantoro.com
  -----------------------------------------------
  Thanks to:
  - Eric Meyer (CSS Reset)
  */

  /* Eric Meyer&#39;s Reset CSS v2.0 (http://meyerweb.com/eric/tools/css/reset/)
  --------------------------------------------------------------------------------------- */
  html,body,div,span,applet,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,pre,a,abbr,acronym,address,big,cite,code,del,dfn,em,img,ins,kbd,q,s,samp,small,strike,strong,sub,sup,tt,var,b,u,i,center,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td,article,aside,canvas,details,embed,figure,figcaption,footer,header,hgroup,menu,nav,output,ruby,section,summary,time,mark,audio,video{margin:0;padding:0;border:0;font-size:100%;font:inherit;vertical-align:baseline}article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section{display:block}body{line-height:1}ol,ul{list-style:none}blockquote,q{quotes:none}blockquote:before,blockquote:after,q:before,q:after{content:&#39;&#39;;content:none}table{border-collapse:collapse;border-spacing:0}
  </style>

  </head>
  <body class='index' itemscope='itemscope' itemtype='http://schema.org/WebPage'>
  <div id='wrapper'>
  <header id='header-wrapper' itemscope='itemscope' itemtype='http://schema.org/WPHeader'>
  <b:section class='header' id='header' maxwidgets='1'>
  <b:widget id='Header1' locked='true' title='Basic Blogger Template (Header)' type='Header'></b:widget>
  </b:section>
  </header>
  <nav id='navigation' itemscope='itemscope' itemtype='http://schema.org/SiteNavigationElement' role='navigation'>
  <ul>
  <li><a href=''>Home</a></li>
  <li><a href=''>About</a></li>
  </ul>
  </nav>
  <div class='clearfix'/>
  <section id='outer-wrapper'>
  <article id='article-wrapper' itemscope='itemscope' itemtype='http://schema.org/Blog' role='main'>
  <b:section class='main' id='main'>
  <b:widget id='Blog1' locked='true' title='Blog Posting' type='Blog'></b:widget>
  </b:section>
  </article>
  </section>
  <div class='clearfix'/>
  <aside id='sidebar-wrapper' itemscope='itemscope' itemtype='http://schema.org/WPSideBar'>
  <b:section class='sidebar' id='sidebar' showaddelement='yes'></b:section>
  </aside>
  <div class='clearfix'/>
  <footer id='footer-wrapper' itemscope='itemscope' itemtype='http://schema.org/WPFooter'>
  <b:section class='footer' id='footer' showaddelement='yes'></b:section>
  </footer>
  </div>
  </body>
  </html>

Save it.
