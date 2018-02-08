---
author: Franziskus Domig
categories:
- Programming
- Web
date: 2011-05-03T21:14:39+00:00
featured_image: /uploads/2011/05/sf2-80x80.png
tags:
- Annotaions
- PHP
- Symfony
- Symfony2
title: Annotations with Symfony2
type: post
url: /2011/05/03/annotations-with-symfony2/
---

With Symfony2 much configuration can be added directly to actions with annotations. With Symfony1 there have been `cache.yml`, `route.yml`, `security.yml` and many more configuration files for a single controller. This has not changed with Symfony2. You still are able to configure your (bundle) controller with single files. However, there is a new way which offers more flexibility and adds the configuration right to the place where it is used: to the specific action as meta-info with some sort of annotations.

First, your `route.yml` has to be edited and your bundle has to be added.

<pre lang="yml"># app/config/route.yml
your_bundle:
    resource "@YourBundle/Controller/YourController.php"
    type: annotation</pre>

This is needed in every setup, but as you see, you can specify the route type as annotation. This means, Symfony2 will parse the doc block on any action of your controller file, and import this to `route.yml`. But don&#8217;t worry, Symfony2 does this just once and stores the information on the cached `route.yml` file.

Now you have to add the routing information on each action which should be imported as route, as shown below. You can also insert params to your route. Additionally to the route you can add various other settings direct to the action as also shown below.

<pre lang="php">class YourController
{
  /**
   * @extra:Route("/action/{id}", name"route_name", requirements = {"id" = "\d+"})
   * @extra:Template("YourBundle:Controller:action", vars={"your"})
   * @extra:Secure(roles="ROLE_MEMBER")
   * @extra:Cache(expires="+7 days")
   */
  public function yourAction($id)
  {
    $your = 'code ' . does('something with', $id);
  }
}</pre>

There is much more to come and everything is still under development. So expect changes and additions to these existing annotations.

**Update 24.05.11**
  
Yesterday, Fabien Potencier announced a change in the Annotation System of Symfony2. There is a [official blog post explaining the changes][1].

 [1]: http://symfony.com/blog/symfony2-annotations-gets-better
