---
title: Calcul Mental
date: 2021-06-29 12:00:00 +0100
categories: [App, Website]
tags: [web, math, php]
render_with_liquid: false
image:
  path: /brain.webp
  lqip: data:image/webp;base64,UklGRmQBAABXRUJQVlA4IFgBAABQCwCdASoyACYAPjEUh0KiIQwGAwAQAYJQBOmarDe+HooHjVMpO0cDjksAIhjgNS+ZC9xy4Nq1dgkmfhv2ZD3LRZoPFQslO4nPOk02qh3welz8uDF6e90oFX08mNFexnWpzqwA/vLnv3cTDrQpBXCTYtEQpkPa7/9tD/y7//+RS3+tt/8MsjhGpCdieBxaaGxo5VhaZV/dSTwt2WlBrJFhVAgJ8lnIUL9faOmD3cLVRZktW/xhkvnwbXRY+3uQdknlpm2gfMW4/Yfx1s5q+idkyS6qKC8xauiI0LR5/IoU3OC8z/Hz0L/cLQSvraezaSPBVvxHMHLUZnHPCtLDr4sukQ1Ekz4fwAo8kn3eSr/V9X/2WrKF8JlXxj/iljHWqdE1L4su7x9U4KFqTk77ufdj/IglHxJERU2bzmASg1Tq1E0i142s8U5EpYxuffCZ46Ae0meSiEAAAA==
  alt: A brain.
---

# Table of Contents

1. [Introduction](#introduction)
2. [Project Overview](#project-overview)
3. [Learning PHP](#learning-php)
   - [Why PHP?](#why-php)
   - [Resources for Learning PHP](#resources-for-learning-php)
4. [Development Process](#development-process)
   - [Initial Setup](#initial-setup)
   - [Creating the Application](#creating-the-application)
     - [Frontend](#frontend)
     - [Backend](#backend)
5. [Conclusion](#conclusion)
6. [References](#references)

## Introduction

In an effort to expand my IT skills and improve my mental arithmetic abilities, I embarked on a project to develop a mental arithmetic training tool using PHP. The result is [Calcul Mental](https://github.com/Constantin-Hentgen/Calcul-Mental), a web application designed to help users enhance their mental computation skills. Here, I share my development journey, the challenges I faced, and the resources that aided me along the way.

## Project Overview

Calcul Mental is a web-based application that generates random arithmetic problems for users to solve, helping them to practice and improve their mental math skills. The project was also an opportunity for me to learn PHP and apply it in a practical context.

## Learning PHP

### Why PHP?

PHP is a popular server-side scripting language widely used for web development. It is known for its ease of use and integration with various databases. Learning PHP allowed me to create dynamic web applications and broaden my IT knowledge.

### Resources for Learning PHP

- **PHP Official Documentation:** The [PHP.net](https://www.php.net/) website is the primary source of information about PHP. It provides comprehensive documentation, examples, and user comments.
- **W3Schools:** The [W3Schools PHP Tutorial](https://www.w3schools.com/php/) is a great starting point for beginners, offering interactive examples and exercises.
- **PHP: The Right Way:** [PHP: The Right Way](https://phptherightway.com/) is an easy-to-read, quick reference for PHP best practices, accepted coding standards, and links to authoritative tutorials around the Web.

## Development Process

### Initial Setup

Setting up the development environment was the first step. I installed PHP and set up a local server using XAMPP, a free and open-source cross-platform web server solution stack package.

### Creating the Application

#### Frontend

The frontend of Calcul Mental was built using HTML and CSS, ensuring a simple and user-friendly interface. JavaScript was used to handle client-side interactions and validations.

#### Backend

The backend was developed in PHP, which handled the generation of arithmetic problems, user session management, and score tracking. Here’s a basic example of how a simple arithmetic problem is generated in PHP:

```php
<?php
$operand1 = rand(1, 10);
$operand2 = rand(1, 10);
$operator = array_rand(['+', '-', '*', '/']);
$question = "$operand1 $operator $operand2";
$answer = eval("return $question;");
?>
```

# Conclusion

Developing Calcul Mental was a rewarding experience that not only enhanced my mental arithmetic skills but also significantly improved my understanding of PHP and web development. I encourage anyone interested in web development or mental arithmetic to check out the project on GitHub even though it needs some work to be operational back.

---

# References

- [PHP Official Documentation](https://www.php.net/)
- [PHP: The Right Way](https://phptherightway.com/)
- [Calcul Mental on GitHub](https://github.com/Constantin-Hentgen/Calcul-Mental)
