Implement Meta Tags
========================

Meta tags help us and search engine to understand your blog, implement meta tags is very important.

By implement meta tags to your template you already help the search engine and visitor to understand your blog.

Basic Blogger Meta Tags
-----------------------

Blogger have a basic meta tags, here it's::

<meta content='width=device-width, initial-scale=1' name='viewport'/>
<title><data:view.title.escaped/></title>
<b:include data='blog' name='all-head-content'/>

This a good place to start but we need a **further optimization** including seo *title tags*, *seo meta tags*, *blogger optimized meta tags*, and *open graph meta tags*.

Blogger Optimized Meta Tags
~~~~~~~~~~~~~~~~~~~~~~~~~~~

This meta tags is optimized for Blogger, this is very important for your blog because have a **function**.

here it's::

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

here it's::

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

here it's::

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

Open Graph Protocol
~~~~~~~~~~~~~~~~~~~

Open graph protocol help social media to fetch your site, this will help fetching on **social media share article**.

here it's::

<meta expr:content='data:blog.pageName' property='og:title'/>
<b:if cond='data:blog.postImageThumbnailUrl'>
<meta expr:content='data:blog.postImageThumbnailUrl' property='og:image'/>
</b:if>
<meta expr:content='data:blog.title' property='og:title'/>
<meta expr:content='data:blog.canonicalUrl' property='og:url'/>
<b:if cond='data:blog.metaDescription'>
<meta expr:content='data:blog.metaDescription' property='og:description'/>
</b:if>

