# Learning HTML

Over the years there have been several forms of HTML. Because of this every HTML file must begin with a DOCTYPE declaraction to denote which version of HTML is being used. The DOCTYPE declaration for HTML5, the most recent version of HTML, is very simple. 

<!DOCTYPE html>    ---- is all that is needed.

### Comments

If you want to add a comment
to your code that will not be
visible in the user's browser, you
can add the text between these
characters:

<!-- comment goes here -->

### The ID Attribute

Every HTML element can carry
the id attribute. It is used to
uniquely identify that element
from other elements on the
page. 

### The Class Attribute

Every HTML element can
also carry a class attribute.
Sometimes, rather than uniquely
identifying one element within
a document, you will want a
way to identify several elements
as being different from the
other elements on the page.

### Block Elements

Some elements will always
appear to start on a new line in
the browser window. These are
known as block level elements.
Examples of block elements are
h1, p, ul, and li.

### Inline Elements

Some elements will always
appear to continue on the
same line as their neighbouring
elements. These are known as
inline elements.
Examples of inline elements are
a, b, em, and img.

### Grouping Text and Elements in a Block

The div element allows you to
group a set of elements together
in one block-level box.
For example, you might create
a div element to contain all
of the elements for the header
of your site (the logo and the
navigation), or you might create
a div element to contain
comments from visitors.

### Grouping Text and Elements Inline

The span element acts like
an inline equivalent of the div
element. It is used to either:
contain a section of text
where there is no other suitable
element to differentiate it from
its surrounding text, OR
contain a number of inline
elements
The most common reason why
people use <span> elements
is so that they can control the
appearance of the content of
these elements using CSS.

###  Iframes

An iframe is like a little window
that has been cut into your
page — and in that window you
can see another page. The term
iframe is an abbreviation of inline
frame.
One common use of iframes
(that you may have seen on
various websites) is to embed
a Google Map into a page. The
content of the iframe can be any
html page (either located on the
same server or anywhere else on
the web).
An iframe is created using the
iframe element.

<iframe>
width="450"
height="350"
src="http://maps.google.co.uk/maps?q=moma+new+york
&amp;output=embed">
</iframe>

### Meta

The <meta> element lives
inside the <head> element and
contains information about that
web page.

<!DOCTYPE html>
<html>
<head>
 <title>Information About Your Pages</title>
 <meta name="description"
 content="An Essay on Installation Art" />
 <meta name="keywords"
 content="installation, art, opinion" />
 <meta name="robots"
 content="nofollow" />
 <meta http-equiv="author"
 content="Jon Duckett" />
 <meta http-equiv="pragma"
 content="no-cache" />
 <meta http-equiv="expires"
 content="Fri, 04 Apr 2014 23:59:59 GMT" />
</head>
<body>
</body>
</html>

### Escape Characters and Symbols

There are some characters that are used in
and reserved by HTML code. (For example, the
left and right angled brackets.)
Therefore, if you want these
characters to appear on your
page you need to use what are
termed "escape" characters
(also known as escape codes or
entity references). For example,
to write a left angled bracket,
you can use either &lt; or
&#60;. For an ampersand, you
can use either &amp; or &#38;.
There are also special codes
that can be used to show
symbols such as copyright and
trademark, currency symbols,
mathematical characters, and
some punctuation marks. For
example, if you want to include a
copyright symbol on a web page
you can use either &copy; or
&#169;.