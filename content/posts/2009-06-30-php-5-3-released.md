---
author: Franziskus Domig
categories:
- PHP
- Programming
date: 2009-06-30T10:25:08+00:00
tags:
- PHP
title: PHP 5.3 Released
type: post
url: /2009/06/30/php-5-3-released/
---

Well not yet, but hopefully in a couple of hours and minutes. (Check [php.net][1]) Although there are some new cool features in it such as lambda functions, closures and PHAR support, there is this silly namespace thing. Namespaces are good in generally (remember, you had to prefix each class with your damn project-name to be on the save side) but separating the namespace parts with the \*escape\* character &#8220;\&#8221; (YES THE BACKSLASH!) &#8211; the worst ever to choose character &#8211; is a awful and total painful thing.

I was hoping until the latest second before the release that someone will fix this BUG and replace the namespace-separator with a better character (maybe &#8220;_&#8221;, &#8220;-&#8220;, &#8220;..&#8221; or &#8220;|&#8221; since &#8220;.&#8221; (concat), &#8220;::&#8221; (static) are already used for other issues).

Do not get me wrong, I appreciate the great work the PHP5.3 Team has done but this namespace thing takes some of the coolness away from that release. Sad but true story.

\*UPDATE\* [PHP 5.3.0 has been release now][2].

 [1]: http://php.net
 [2]: http://www.php.net/archive/2009.php#id2009-06-30-1
