---
author: Franziskus Domig
categories:
- PHP
- Programming
date: 2010-07-19T11:23:45+00:00
tags:
- Anti-Pattern
- Code
- Facebook
- lex-pass
- PHP
- Symfony
- University
title: Automatic Anti-Pattern Corrections for PHP
type: post
url: /2010/07/19/automatic-anti-pattern-corrections-for-php/
---

During my computer science studies at the Vorarlberg University of Applied Sciences I wrote my bachelor thesis about &#8220;Automatic Anti-Pattern Corrections for PHP&#8221;. As a fan of the open source philosophy, I want to share my work with others. I invite everyone to contribute to the great lex-pass project and this approach to better PHP software. Please share your thought and ideas on this with me and others by leaving a comment or sending me a message.<!--more-->

The thesis is written in german but at least there is an english abstract.

> **Abstract**
> 
> Since the first release of the programming language PHP, PHP has been rapidly developed. As a result to these huge improvements, many of the features from PHP 4 have been rewritten or replaced in PHP 5. For instance exception handling, abstract classes and interfaces have been introduced. Additionally, objects are not getting copied (call-by-value) every time they are assigned to another variable or used as function parameters, but assigned as reference (call-by-reference). As a result, many old and bad constructs remain in already existing applications. This leads to several issues.
> 
> That is why many companies struggle especially with security and performance problems. Manual refactoring of existing source code is time-consuming and a reason why a lot of companies abandon such improvements.
  
> The open-source initiative of Facebook led to the tool [lex-pass][1] which is already capable of some very basic refactoring transformations. It is using the abstract syntax tree (AST) to transform PHP into corrected code according to predefined rules.
> 
> This bachelor thesis detects several anti-patterns and implements some basic transformations. As a result, these anti-patterns are automatically corrected with lex-pass. Then the implemented transformations are explained in detail and some further possible corrections are discussed. For demonstration purposes, some well known open-source projects are being tested and corrected with the written transformations.
> 
> As a conclusion the advantages and disadvantages of automatic corrections are explained and the usefulness and limitations of such automatic transformations are illustrated.

[Download &#8220;Automatic Anti-Pattern Corrections for PHP&#8221; bachelor thesis][2]

I would like to thank the people from Mayflower GmbH for their great support and Daniel Corson from Facebook for his contribution to my work.

 [1]: http://github.com/facebook/lex-pass
 [2]: /uploads/2010/07/Bachelorarbeit_Franziskus_Domig.pdf
