---
author: Franziskus Domig
categories:
- PHP
date: 2008-09-02T20:21:57+00:00
tags:
- English
- REST
- Symfony
title: Symfony 1.2 introduces REST
type: post
url: /2008/09/02/symfony-12-introduces-rest/
---

As [Fabien just posted on the Symfony Blog][1] the next major release of Symfony &#8211; Symfony 1.2 &#8211; will introduce a quite cool feature to the framework. It will be possible to add a hidden form element to add [REST][2] inforrmation to the form and get the REST state with `sfRequest::getMethod()`. This is quite useful and adds native support for `PUT` and `DELETE` from the browser.

 [1]: http://www.symfony-project.org/blog/2008/09/02/new-in-symfony-1-2-small-things-matter "Symfony Blog"
 [2]: http://en.wikipedia.org/wiki/Representational_State_Transfer
