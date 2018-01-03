---
title: I Love the JavaScript shorthand of If-else statement 😃
author: Raymon Schouwenaar
type: post
date: 2017-06-28T19:02:25+00:00
url: /love-javascript-shorthand-else-statement/
featured_image: /wp-content/uploads/2017/06/love-javascript-shorthand-else-statement-photo.jpg
medium_post:
  - 'O:11:"Medium_Post":11:{s:16:"author_image_url";s:75:"https://cdn-images-1.medium.com/fit/c/200/200/1*W5ssxLrDoscNIwTcu_fDEA.jpeg";s:10:"author_url";s:33:"https://medium.com/@rsschouwenaar";s:11:"byline_name";N;s:12:"byline_email";N;s:10:"cross_link";s:3:"yes";s:2:"id";s:12:"e55ea8e8c77f";s:21:"follower_notification";s:3:"yes";s:7:"license";s:19:"all-rights-reserved";s:14:"publication_id";s:2:"-1";s:6:"status";s:6:"public";s:3:"url";s:99:"https://medium.com/@rsschouwenaar/i-love-the-javascript-shorthand-of-if-else-statement-e55ea8e8c77f";}'
dsq_thread_id:
  - 5949255122
categories:
  - Javascript
tags:
  - ES6

---
So there it is! It is a long time ago that I put online a new blog post! Did a lot of other stuff then Web Development. But this time I want to share a small nice trick in JavaScript!

Yes, I love the JavaScript shorthand of the if-else statement. (_For the record, the let variable is_ an ES6_ type variable._) Check the super simple example below.

{{< code type="javascript" >}}
  let aVar = 'A';
  let conditionalVariable = aVar === 'A' ? true : false;
{{< /code >}}

This example is super simple. I use this most of the times when the value of a variable needs to be based on the other variable.

In the early days of me writing an if-else statement in JavaScript was more like this:

{{< code type="javascript" >}}
  var aVar = 'A';
  if(aVar === 'A') {
    var conditionalVariable = true;
  } else {
    var conditionalVariable = false;
  }
{{< /code >}}

But since DRY (Don&#8217;t Repeat Yourself) is a good thing to keep in mind, this is not the best code! In some cases, the normal If-else statement is more readable.

But for very simple tasks like my top example, it is less code.

**Bonus**

As a bonus, I want to show that this does also work very good in Angular template expressions.

{{< code type="javascript" >}}
&lt;strong&gt;{{COMPONENT.incomeType === 'SELF_EMPLOYED' ? 'Self employed' : 'Employed'}}&lt;/strong&gt;
{{< /code >}}

This will avoid writing multiple HTML tags with ng-if&#8217;s:

{{< code type="javascript" >}}
&lt;strong ng-if="COMPONENT.incomeType === 'SELF_EMPLOYED"&gt;
    Self employed
&lt;/strong&gt;
&lt;strong ng-if="COMPONENT.incomeType !== 'SELF_EMPLOYED'"&gt;
    Employed
&lt;/strong&gt;
{{< /code >}}

So hopefully this is gonna help you with writing better DRY JavaScript code!