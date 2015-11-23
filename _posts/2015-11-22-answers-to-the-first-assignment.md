---

layout: post
title: Answers to the first assignment
date:   2015-11-22
categories: jekyll update
comments: true
---



**Below are the answers to the questions, which was a part of Assignment 1.**

**1. What do you think of pre-compiling your CSS?**

* Compare to regular CSS

* Which techniques did you use?

* Pros and cons?



I think this technique is a great way for compiling css files.
 Mostly because of the different tools that are available to use while pre-compiling, such as variables and Mixins which brings a much cleaner workspace compared to regular repeated css code.
But at the same time I feel like I should have learnt this way of building static websites a long time ago, rather than the classic way of compiling CSS and HTML pages, because of the fact that the syntax is a little bit different and takes a while to understand.

Regular CSS files takes a lot more time and are not as efficient due to all the repeated code that has to be written which brings more bugs & problems while elements affecting each-other.
While using this pre-compiled technique, I used both variables to avoid repeated code, and also mixins to state an "property" once, and use it when needed. I also used .md "Markdown" syntax to write the contents of the pages, and also some Liquid templating language to bring the content to the html pages.

**Conclusion:** The pros are the fact that pre-compiled CSS is much easier to get things done much faster and also cleaner while not have the need to repeat code which can bring bugs.
  Compared to regular CSS, I can not see any cons about this technique, but then I have not been using this technique so long ether. The only con for me personally is that the syntax is not the same which can take a while to understand completely.

**2. What do you think of static site generators?**

* What type of projects are they suitable for?

I think it is really great to be able to work with static pages that are easy to maintain and configure with this technique.
 The loading time is much faster and the html-structure is divided into separate parts that are included to the "big tree" which also makes it easier to find bugs when occured.

Static site generators are more suitable for static sites like, blogs, information sites and other similar websites that does not have dynamic data that changes every day like prices etc..


**3. What is robots.txt and how have you configure it for your site?**

By including the file "robots.txt", we telling the search engines how to behave. We can here state what folders they can/can not access.
 There is a few configurations that can be made here to control for example which search engines that are allowed to get access.

**This is my configurations:**
{% highlight ruby %}
User-agent: *
Disallow
{% endhighlight %}


**4. What is humans.txt and how have you configure it for your site?**

By including the file "humans.txt", we give other users access to credit information about the website and depending on the developer, also other information that can be interesting to know.

**This is my configurations:**
{% highlight ruby %}
/* TEAM */
Name: Sahand Rajabion
Site: http://sahandrajabion.github.io
Twitter: sahandrajabion
Github: sahandrajabion
Location: Kalmar, Sweden

/* THANKS */
URL: http://lnu.se/, http://sahandrajabion.com/, http://jekyllrb.com/docs/


/* SITE */
Standards: HTML5, CSS3.
Components: Jekyll, SASS, Disqus, Open Graph.
Software: JetBrains WebStorm.
{% endhighlight %}



**5. How did you implements comments to blog posts?**

I followed the recommended instructions for Discus, and implemented the script after I registered an account. I enabled comments by using, "comments: true" and put the generic code in the post.html layout for all created posts that uses that specific layout.


**What is Open Graph and how do you make use of it?**

Open Graph is a tool that is created in the html-head and are used to determine how the shared link of the website should be presented.
By controlling the image, description and title in the shared link, you can make other users more interested in your site rather than a simple shared URL link in a social media.




{% if page.comments %}

<div id="disqus_thread"></div>
<script>
    /**
     *  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
     *  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables
     */
    /*
    var disqus_config = function () {
        this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
        this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
    };
    */
    (function() {  // DON'T EDIT BELOW THIS LINE
        var d = document, s = d.createElement('script');

        s.src = '//sahandrajabion.disqus.com/embed.js';

        s.setAttribute('data-timestamp', +new Date());
        (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript" rel="nofollow">comments powered by Disqus.</a></noscript>

{% endif %}