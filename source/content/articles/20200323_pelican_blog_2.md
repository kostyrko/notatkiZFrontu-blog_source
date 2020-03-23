Title: Pelican Blog 2
Author: mkostyrko
Date: 2020-03-23 9:05
Category: blog
Tags: python, markdown, pelican
Slug: pelican-blog-2

Basic markdown examples are shown below
after [matthewdevaney.com](https://matthewdevaney.com/posts/2019/03/07/build-a-blog-with-pelican-and-python-pt-2-creating-content/)

This text is **bold**
This text is also __bold__

This text is *italic*
This text is also _italic_

This text is **_italic and bold_**

# An h1 heading

## An h2 heading

### An h3 heading...

###### An h6 heading

A list with numbers:
1. One
2. Two
3. Three

A list with bullets:
* Bullet
* Bullet
* Bullet

Here's a blockquote:

&gt; Simple is better than complex

Here's a table:

| Column1 | Column 2 | Column 3
|---|---|---|
| Value 1 | Value 2 | Value 3 |
| Value 4 | Value 5 | Value 6 |
| Value 7 | Value 8 | Value 9 |

Code blocks are preceeded by an indent, three : symbols and the name of the language.  
All of the following code will be highlighted while the text is indented.

    :::python3
    def do_twice(func):
    def wrapper_do_twice(*args, **kwargs):
        return func(*args, **kwargs).lower()
    return wrapper_do_twice

    @do_twice
    def say_whee(some_text):
        print(some_text)

    x = 'Whee!'
    say_whee(x)