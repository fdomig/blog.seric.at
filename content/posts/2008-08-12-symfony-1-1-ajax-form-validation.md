---
author: Franziskus Domig
categories:
- PHP
date: 2008-08-12T16:30:58+00:00
tags:
- Ajax
- English
- Symfony
title: Symfony 1.1 Ajax Form Validation
type: post
url: /2008/08/12/symfony-1-1-ajax-form-validation/
---

Since [Symfony 1.1 was released][1], I am working with it. I adept a existing Symfony 1.0 application to 1.1. This process is quite tricky and needs a lot of research to get the result that I want.

As I faced a problem with a form which I submit via an Ajax request, I found a pretty nice solution in doing this with Symfony 1.1.
  
<!--more-->

<pre lang="php">public function executeSubmitaction($request) {
    $form   = new FoobarForm();

    // set the form to bound status with the submitted values
    $form-&gt;bind($request-&gt;getParameter('formvalues'));

    // validate all values
    if (!$form-&gt;isValid()) {
        $errors = array();
        foreach ($form-&gt;getErrorSchema() as $field =&gt; $error) {
            $errors[$field] = $error-&gt;getMessage();
        }
        $this-&gt;errors = $errors;
        return sfView::ERROR;
    }

    // do stuff if the form is valid

    return sfView::SUCCESS;
}</pre>

On the view-side I then have a javascript function which handles all the errors and I am using the serialized errors-array in the error-template to display the errors to the propriate divs.

 [1]: http://www.symfony-project.org/blog/2008/06/30/the-wait-is-over-symfony-1-1-released
