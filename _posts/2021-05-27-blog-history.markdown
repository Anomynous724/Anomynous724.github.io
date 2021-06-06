---
title: Blog History
subtitle: Blog Renewal, Create, Edit, and etc.
layout: post_detail
date-created: 2020-05-27
date-edited: 2020-06-06
thumbnail: 2021-05-27-blog-history-thumbnail.jpg
alt: image-alt
project-date: May 2021
client: Start Bootstrap
category: [Post, Blog]
description: Blog History
---

### Blog History

#### Blog Renewal
* Date: 2021-06-06
* Basic Theme: Agency Jekyll Blog Theme
* Source: [agency-jekyll-theme](https://github.com/raviriley/agency-jekyll-theme)

#### Set Up Local Environment
* Date: 2021-05-28
* Stack: Docker, Git
* Reference: [Docker Local Envrionment](https://jehuipark.github.io/blog/blog-env-setting-with-docker)
* docker-compose.yml code: 
```go
version: "3.3"

services:
  jekyll:
    image: jekyll/jekyll:latest
    command: jekyll serve --force_polling --drafts --livereload --trace
    ports:
      - "4000:4000"
    volumes:
      - ".:/srv/jekyll"
```

#### Add Typed Animation in Header Introduction
* Date: 2021-05-28
* Stack: Liquid, Javascript(typed.min.js)
* Code:
```Javascript
<script type="text/javascript">
                    var typed = new Typed('.typed', {
                        // Waits 1000ms after typing "First"
                        strings: [
                            'Developer.',
                            'Always Student.'
                        ],
                        smartBackspace: true,
                        typeSpeed: 30,
                        backSpeed: 30,
                        backDelay: 1000,
                        loop: true,
                        loopCount: Infinity
                    });
                </script>
```
* Result:
![Typed Animation]({{ site.url }}/img/post/blog/blog-history/header-typed-animation.gif "Logo Title Text 1")

#### Add Social
* Date: 2021-05-29
* Stack: Liquid, Jekyll
* Details: StackOverFlow, Github, Linkedin

#### Fix Nav Menu Shrink Error
* Date: 2021-05-29
* Stack: Liquid, Jekyll, Javascript, jQuery
* Problem: Nav Bar doesn't shrink when scroll down.
* Cause: In default.html, js.html is moved to the top second position for typed animation.
* Solution: In header.html, typed animation script tags is surrounded by document.
* Code:
```Javascript
document.addEventListener("DOMContentLoaded", function(event) { });
```

#### Fix Mail Error
* Date: 2021-05-29
* Stack: Liquid, Jekyll, Javascript, HTML, ajax
* Problem: Mail Service doesn't work.
* Cause: Github pages Service only supports static websites, not dynamic website(node.js, php, and etc).
* Solution: Use formspree.io service.
* Details:
1. The ‘agency Jekyll theme’ mail service is made by php which is server-side programming language. However, Github pages only supports static html components, so a blog that is serviced by Github pages cannot actually run server side components including node.js, php…. I’ll use formspree.io service
Formspree.io service only takes json file with special header.
2. Using Ajax with Formspree.io
```Javascript
$.ajax({
  url: "https://formspree.io/f/YOUR_FORM_ID",
  method: "POST",
  dataType: "json",
  data: {
    email: "a.visitor@email.com",
    message: "Hello!"
  }
});
```

* Reference:
1. [https://dev.to/charalambosioannou/create-a-static-webpage-with-a-contact-form-on-github-pages-3532](https://dev.to/charalambosioannou/create-a-static-webpage-with-a-contact-form-on-github-pages-3532)
2. [https://dev-yakuza.posstree.com/ko/jekyll/send-email/](https://dev-yakuza.posstree.com/ko/jekyll/send-email/)
3. [https://stackoverflow.com/questions/24348223/send-email-from-static-page-hosted-on-github-pages](https://stackoverflow.com/questions/24348223/send-email-from-static-page-hosted-on-github-pages)
4. [https://jehwanyoo.net/2020/09/28/%EC%A0%95%EC%A0%81-%EC%82%AC%EC%9D%B4%ED%8A%B8(Github%20Pages)%EC%97%90%EC%84%9C-%EC%B5%9C%EC%8B%A0%EA%B8%80-%EB%B6%88%EB%9F%AC%EC%98%A4%EA%B8%B0-%EA%B8%B0%EB%8A%A5-%EA%B5%AC%ED%98%84%ED%95%98%EA%B8%B0/](https://jehwanyoo.net/2020/09/28/%EC%A0%95%EC%A0%81-%EC%82%AC%EC%9D%B4%ED%8A%B8(Github%20Pages)%EC%97%90%EC%84%9C-%EC%B5%9C%EC%8B%A0%EA%B8%80-%EB%B6%88%EB%9F%AC%EC%98%A4%EA%B8%B0-%EA%B8%B0%EB%8A%A5-%EA%B5%AC%ED%98%84%ED%95%98%EA%B8%B0/)
5. [https://help.formspree.io/hc/en-us/articles/360013470814-Submit-forms-with-JavaScript-AJAX-](https://help.formspree.io/hc/en-us/articles/360013470814-Submit-forms-with-JavaScript-AJAX-)

---

Reference Website

[https://www.salary.com/articles/sell-yourself-14-steps-to-creating-a-powerful-personal-brand/](https://www.salary.com/articles/sell-yourself-14-steps-to-creating-a-powerful-personal-brand/)