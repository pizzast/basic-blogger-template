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

This a good place to start but we need a **further optimization** including seo title tags, seo meta tags, blogger optimized meta tags and open graph meta tags.

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


