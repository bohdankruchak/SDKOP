Some text about HTML, SGML and HTML4.

Let's talk about the U.S.A., (É.U. or É.-U. d'A. in French).

*[HTML4]: Hyper Text Markup Language version 4
*[HTML]: Hyper Text Markup Language
*[SGML]: Standard Generalized Markup Language
*[U.S.A.]: United States of America
*[É.U.] : États-Unis d'Amérique
*[É.-U. d'A.] : États-Unis d'Amérique

And here we have a CD, some CDs, and some other CD's.

*[CD]: Compact Disk

Let's transfert documents through TCP/IP, using TCP packets.

*[IP]: Internet Protocol
*[TCP]: Transmission Control Protocol

 ---

Bienvenue sur [CMS](http://www.bidulecms.com "Bidule CMS").

*[CMS]: Content Management System

 ---

ATCCE

*[ATCCE]: Abbreviation "Testing" Correct 'Character' < Escapes >* one
* two

1. three
2. four

* one
* two
1. three
2. fourAT&T has an ampersand in their name.

AT&amp;T is another way to write it.

This & that.

4 < 5.

6 > 5.

Here's a [link] [1] with an ampersand in the URL.

Here's a link with an amersand in the link text: [AT&T] [2].

Here's an inline [link](/script?foo=1&bar=2).

Here's an inline [link](</script?foo=1&bar=2>).


[1]: http://example.com/?foo=1&bar=2
[2]: http://att.com/  "AT&T"Link: <http://example.com/>.

With an ampersand: <http://example.com/?foo=1&bar=2>

* In a list?
* <http://example.com/>
* It should.

> Blockquoted: <http://example.com/>

Auto-links should not occur here: <http://example.com/>

	or here: <http://example.com/>These should all get escaped:

Backslash: \\

Backtick: \

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-



These should not, because they occur within a code block:

	Backslash: \\

	Backtick: \

	Asterisk: \*

	Underscore: \_

	Left brace: \{

	Right brace: \}

	Left bracket: \[

	Right bracket: \]

	Left paren: \(

	Right paren: \)

	Greater-than: \>

	Hash: \#

	Period: \.

	Bang: \!

	Plus: \+

	Minus: \-


Nor should these, which occur in code spans:

Backslash: \\

Backtick:   \  

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-


These should get escaped, even though they're matching pairs for
other Markdown constructs:

\*asterisks\*

\_underscores\_

\backticks\

This is a code span with a literal backslash-backtick sequence:   \  

This is a tag with unescaped backticks <span attr='ticks'>bar</span>.

This is a tag with backslashes <span attr='\\backslashes\\'>bar</span>.
  .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>
 

As above: checking for bad interractions with the HTML block parser:

  html
<div>
 

Some *markdown* formatting.

  html
</div>
 

Some *markdown*

 
<div>
    <html>
 

 
function test();
 

<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">
 
<html>
    <title>
 
</div>

Two code blocks with no blank line between them:

 
<div>
 
 
<div>
 

Testing *confusion* with code spans at the HTML block parser:

 
<div></div>
 

Testing mixing with title code blocks

 
<p>

<p>
 

<p>
 
<p>

 
<Fenced>
 

Code block starting and ending with empty lines:
 


<Fenced>


 

Indented code block containing fenced code block sample:

	 
	<Fenced>
	 

Fenced code block with indented code block sample:

 
Some text

	Indented code block sample code
 

Fenced code block with long markers:

 
Fenced
 

Fenced code block with fenced code block markers of different length in it:

 
In code block
 
Still in code block
 
Still in code block
 

Fenced code block with Markdown header and horizontal rule:

 
#test
---
 

Fenced code block with link definitions, footnote definition and
abbreviation definitions:

 
[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language
 

* In a list item with smalish indent:

   
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
   

With HTML content.

 
<b>bold</b>
 

Bug with block level elements in this case:
 
  <div>
  </div>
 

Indented code block of a fenced code block:

     
	haha!
	 

With class:

 html
<b>bold</b>
 

  html
<b>bold</b>
 

 .html
<b>bold</b>
 

  .html
<b>bold</b>
 

With extra attribute block:

 {.html}
<b>bold</b>
 

  {.html #codeid}
<b>bold</b>
 

  .html{.bold}
<div>
 
  
  .html {#codeid}
</div>
 > Example:
> 
>     sub status {
>         print "working";
>     }
> 
> Or:
> 
>     sub status {
>         return "working";
>     }

*	List Item:

		code block

		with a blank line

	within a list item.

*       code block
        as first element of a list item

*	List Item:
	
		code block with whitespace on preceding line
    Codeblock on second line
    <?php
    echo "hello!";
    ?>

foo bar

    <?php
    echo "hello!";

lorem ipsum

    echo "hello!";
    ?>
    
lorem ipsum	code block on the first line
	
Regular text.

    code block indented by spaces

Regular text.

	the lines in this block  
	all contain trailing spaces  

Regular Text.

	code block on the last line<test a=" content of attribute ">

Fix for backticks within HTML tag: <span attr='ticks'>like this</span>

Here's how you put   backticks   in a code span.A simple definition list:

Term 1
:   Definition 1

Term 2
:   Definition 2

With multiple terms:

Term 1
Term 2
:   Definition 1

Term 3
Term 4
:   Definition 2

With multiple definitions:

Term 1
:   Definition 1
:   Definition 2

Term 2
:   Definition 3
:   Definition 4

With multiple lines per definition:

Term 1
:   Definition 1 line 1 ...
Definition 1 line 2
:   Definition 2 line 1 ...
Definition 2 line 2

Term 2
:   Definition 3 line 2 ...
    Definition 3 line 2
:   Definition 4 line 2 ...
    Definition 4 line 2

With paragraphs:

Term 1

:   Definition 1 (paragraph)

Term 2

:   Definition 2 (paragraph)

With multiple paragraphs:

Term 1

:   Definition 1 paragraph 1 line 1 ...
	Definition 1 paragraph 1 line 2

    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)

    Definition 1 paragraph 2 line 1 ...
Definition 1 paragraph 2 line 2 (lazy)

* * *

A mix:

Term 1
Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)
    
    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

:   Definition 2 paragraph 1 line 1 ...
Definition 2 paragraph 1 line 2 (lazy)

Term 3
:   Definition 3 (no paragraph)
:   Definition 4 (no paragraph)
:   Definition 5 line 1 ...
    Definition 5 line 2 (no paragraph)

:   Definition 6 paragraph 1 line 1 ...
Definition 6 paragraph 1 line 2
:   Definition 7 (no paragraph)
:   Definition 8 paragraph 1 line 1 (forced paragraph) ...
    Definition 8 paragraph 1 line 2
    
    Definition 8 paragraph 2 line 1
    
Term 4
:   Definition 9 paragraph 1 line 1 (forced paragraph) ...
    Definition 9 paragraph 1 line 2
    
    Definition 9 paragraph 2 line 1
:   Definition 10 (no paragraph)

* * *

Special cases:

Term

:       code block
        as first element of a definition<michel.fortin@michelf.ca>

International domain names: <help@tūdaliņ.lv>


## Some weird valid email addresses

<abc.123@example.com>

<1234567890@example.com>

<_______@example.com>

<abc+mailbox/department=shipping@example.com>

<!#$%&'*+-/=?^_.{|}@example.com> (all of these characters are allowed)

<"abc@def"@example.com> (anything goes inside quotation marks)

<"Fred Bloggs"@example.com>

<jsmith@[192.0.2.1]>

<"A"@example.com>Combined emphasis:

1.  ***test test***
2.  ___test test___
3.  *test **test***
4.  **test *test***
5.  ***test* test**
6.  ***test** test*
7.  ***test* test**
8.  **test *test***
9.  *test **test***
10. _test __test___
11. __test _test___
12. ___test_ test__
13. ___test__ test_
14. ___test_ test__
15. __test _test___
16. _test __test___
17. *test __test__*
18. **test _test_**
19. **_test_ test**
20. *__test__ test*
21. **_test_ test**
22. **test _test_**
23. *test __test__*
24. _test **test**_
25. __test *test*__
26. __*test* test__
27. _**test** test_
28. __*test* test__
29. __test *test*__
30. _test **test**_


Incorrect nesting:

1.  *test  **test*  test**
2.  _test  __test_  test__
3.  **test  *test** test*
4.  __test  _test__ test_
5.  *test   *test*  test*
6.  _test   _test_  test_
7.  **test **test** test**
8.  __test __test__ test__
9. _**some text_**
10. *__some text*__
11. **_some text**_
12. *__some text*__

No emphasis:

1.  test*  test  *test
2.  test** test **test
3.  test_  test  _test
4.  test__ test __test



Middle-word emphasis (asterisks):

1.  *a*b
2.   a*b*
3.   a*b*c
4. **a**b
5.   a**b**
6.   a**b**c


Middle-word emphasis (underscore):

1.  _a_b
2.   a_b_
3.   a_b_c
4. __a__b
5.   a__b__
6.   a__b__c

my_precious_file.txt


## Tricky Cases

E**. **Test** TestTestTest

E**. **Test** Test Test Test


## Overlong emphasis

Name: ____________  
Organization: ____  
Region/Country: __

_____Cut here_____

____Cut here____

# Regression

_**Note**_: This _is emphasis_.
With asterisks

 * List item
 *
 * List item

With numbers

1. List item
2.
3. List item

With hyphens

- List item
-
- List item

With asterisks

 * List item
 * List item
 *

With numbers

1. List item
2. List item
3.

With hyphens

- List item
- List item
-
This is the first paragraph.[^first]

[^first]:  This is the first note.

* List item one.[^second]
* List item two.[^third]

[^third]: This is the third note, defined out of order.
[^second]: This is the second note.
[^fourth]: This is the fourth note.

# Header[^fourth]

Some paragraph with a footnote[^1], and another[^2].

[^1]: Content for fifth footnote.
[^2]: Content for sixth footnote spaning on 
    three lines, with some span-level markup like
    _emphasis_, a [link][].

[link]: http://michelf.ca/

Another paragraph with a named footnote[^fn-name].

[^fn-name]:
    Footnote beginning on the line next to the marker.

This paragraph should not have a footnote marker since 
the footnote is undefined.[^3]

This paragraph has a second footnote marker to footnote number one.[^1]

This paragraph links to a footnote with plenty of 
block-level content.[^block]

[^block]:
	Paragraph.
	
	*   List item
	
	> Blockquote
	
	    Code block

This paragraph host the footnote reference within a 
footnote test[^reference].

[^reference]:
	This footnote has a footnote of its own.[^nested]

[^nested]:
	This footnote should appear even though it is referenced
	from another footnote. But [^reference] should be litteral
	since the footnote with that name has already been used.

 - - -

Testing unusual footnote name[^1$^!"'].

[^1$^!"']: Haha!

 - - -
 
Footnotes mixed with images[^image-mixed]
![1800 Travel][img6]
![1830 Travel][img7]

[img6]: images/MGR-1800-travel.jpeg "Travel Speeds in 1800"
[^image-mixed]: Footnote Content
[img7]: images/MGR-1830-travel.jpeg "Travel Speeds in 1830"
In Markdown 1.0.0 and earlier. Version
8. This line turns into a list item.
Because a hard-wrapped line in the
middle of a paragraph looked like a
list item.

Here's one with a bullet.
* criminey.
Header  {#id1}
======

Header  { #id2}
------

### Header  {#id3 }
#### Header ##  { #id4 }

 - - -

Header  {.cl}
======

Header  { .cl}
------

### Header  {.cl }
#### Header ##  { .cl }

 - - -

Header  {.cl.class}
======

Header  { .cl .class}
------

### Header  {.cl .class }
#### Header ##  { .cl.class }

 - - -

Header  {#id5.cl.class}
======

Header  { #id6 .cl .class}
------

### Header  {.cl.class#id7 }
#### Header ##  { .cl.class#id8 }
Header
======

Header
------

### Header

 - - -

Header
======
Paragraph

Header
------
Paragraph

### Header
Paragraph

 - - -

Paragraph
Header
======
Paragraph

Paragraph
Header
------
Paragraph

Paragraph
### Header
ParagraphDashes:

---

 ---
 
  ---

   ---

	---

- - -

 - - -
 
  - - -

   - - -

	- - -


Asterisks:

***

 ***
 
  ***

   ***

	***

* * *

 * * *
 
  * * *

   * * *

	* * *


Underscores:

___

 ___
 
  ___

   ___

    ___

_ _ _

 _ _ _
 
  _ _ _

   _ _ _

    _ _ _
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")

Inline within a paragraph: [alt text](/url/).

![alt text](/url/  "title preceded by two spaces")

![alt text](/url/  "title has spaces afterward"  )

![alt text](</url/>)

![alt text](</url/> "with a title").

![Empty]()

![this is a stupid URL](http://example.com/(parens).jpg)


![alt text][foo]

  [foo]: /url/

![alt text][bar]

  [bar]: /url/ "Title here"Simple block on one line:

<div>foo</div>

And nested without indentation:

<div>
<div>
<div>
foo
</div>
<div style=">"/>
</div>
<div>bar</div>
</div>

And with attributes:

<div>
	<div id="foo">
	</div>
</div>

This was broken in 1.0.2b7:

<div class="inlinepage">
<div class="toggleableend">
foo
</div>
</div>
Here's a simple block:

<div>
	foo
</div>

This should be a code block, though:

	<div>
		foo
	</div>

As should this:

	<div>foo</div>

Now, nested:

<div>
	<div>
		<div>
			foo
		</div>
	</div>
</div>

This should just be an HTML comment:

<!-- Comment -->

Multiline:

<!--
Blah
Blah
-->

Code block:

	<!-- Comment -->

Just plain comment, with trailing spaces on the line:

<!-- foo -->   

Code:

	<hr />
	
Hr's:

<hr>

<hr/>

<hr />

<hr>   

<hr/>  

<hr /> 

<hr class="foo" id="bar" />

<hr class="foo" id="bar"/>

<hr class="foo" id="bar" >

<abbr title=" **Attribute Content Is Not A Code Span** ">ACINACS</abbr>

<abbr title="first backtick!">SB</abbr> 
<abbr title="second backtick!">SB</abbr>Paragraph one.

<!-- This is a simple comment -->

<!--
	This is another comment.
-->

Paragraph two.

<!-- one comment block -- -- with two comments -->

The end.
# Markdown inside code blocks

<div markdown="1">
foo
</div>

<div markdown='1'>
foo
</div>

<div markdown=1>
foo
</div>

<table>
<tr><td markdown="1">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="span">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="block">test _emphasis_ (block)</td></tr>
</table>

## More complicated

<table>
<tr><td markdown="1">
* this is _not_ a list item</td></tr>
<tr><td markdown="span">
* this is _not_ a list item</td></tr>
<tr><td markdown="block">
* this _is_ a list item
</td></tr>
</table>

## With indent

<div>
    <div markdown="1">
    This text is no code block: if it was, the 
    closing <div> would be too and the HTML block 
    would be invalid.

    Markdown content in HTML blocks is assumed to be 
    indented the same as the block opening tag.

    **This should be the third paragraph after the header.**
    </div>
</div>

## Code block with rogue </div>s in Markdown code span and block

<div>
    <div markdown="1">

    This is a code block however:

        </div>

    Funny isn't it? Here is a code span: </div>.

    </div>
</div>

<div>
  <div markdown="1">
    * List item, not a code block

Some text

      This is a code block.
  </div>
</div>

## No code block in markdown span mode

<p markdown="1">
    This is not a code block since Markdown parse paragraph 
    content as span. Code spans like </p> are allowed though.
</p>

<p markdown="1">_Hello_ _world_</p>

## Preserving attributes and tags on more than one line:

<p class="test" markdown="1" 
id="12">
Some _span_ content.
</p>


## Header confusion bug

<table class="canvas">
<tr>
<td id="main" markdown="1">Hello World!
============

Hello World!</td>
</tr>
</table>
Here is a block tag ins:

<ins>
<p>Some text</p>
</ins>

<ins>And here it is inside a paragraph.</ins>

And here it is <ins>in the middle of</ins> a paragraph.

<del>
<p>Some text</p>
</del>

<del>And here is ins as a paragraph.</del>

And here it is <del>in the middle of</del> a paragraph.
		    GNU GENERAL PUBLIC LICENSE
		       Version 2, June 1991

 Copyright (C) 1989, 1991 Free Software Foundation, Inc.,
 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

			    Preamble

  The licenses for most software are designed to take away your
freedom to share and change it.  By contrast, the GNU General Public
License is intended to guarantee your freedom to share and change free
software--to make sure the software is free for all its users.  This
General Public License applies to most of the Free Software
Foundation's software and to any other program whose authors commit to
using it.  (Some other Free Software Foundation software is covered by
the GNU Lesser General Public License instead.)  You can apply it to
your programs, too.

  When we speak of free software, we are referring to freedom, not
price.  Our General Public Licenses are designed to make sure that you
have the freedom to distribute copies of free software (and charge for
this service if you wish), that you receive source code or can get it
if you want it, that you can change the software or use pieces of it
in new free programs; and that you know you can do these things.

  To protect your rights, we need to make restrictions that forbid
anyone to deny you these rights or to ask you to surrender the rights.
These restrictions translate to certain responsibilities for you if you
distribute copies of the software, or if you modify it.

  For example, if you distribute copies of such a program, whether
gratis or for a fee, you must give the recipients all the rights that
you have.  You must make sure that they, too, receive or can get the
source code.  And you must show them these terms so they know their
rights.

  We protect your rights with two steps: (1) copyright the software, and
(2) offer you this license which gives you legal permission to copy,
distribute and/or modify the software.

  Also, for each author's protection and ours, we want to make certain
that everyone understands that there is no warranty for this free
software.  If the software is modified by someone else and passed on, we
want its recipients to know that what they have is not the original, so
that any problems introduced by others will not reflect on the original
authors' reputations.

  Finally, any free program is threatened constantly by software
patents.  We wish to avoid the danger that redistributors of a free
program will individually obtain patent licenses, in effect making the
program proprietary.  To prevent this, we have made it clear that any
patent must be licensed for everyone's free use or not licensed at all.

  The precise terms and conditions for copying, distribution and
modification follow.

		    GNU GENERAL PUBLIC LICENSE
   TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

  0. This License applies to any program or other work which contains
a notice placed by the copyright holder saying it may be distributed
under the terms of this General Public License.  The "Program", below,
refers to any such program or work, and a "work based on the Program"
means either the Program or any derivative work under copyright law:
that is to say, a work containing the Program or a portion of it,
either verbatim or with modifications and/or translated into another
language.  (Hereinafter, translation is included without limitation in
the term "modification".)  Each licensee is addressed as "you".

Activities other than copying, distribution and modification are not
covered by this License; they are outside its scope.  The act of
running the Program is not restricted, and the output from the Program
is covered only if its contents constitute a work based on the
Program (independent of having been made by running the Program).
Whether that is true depends on what the Program does.

  1. You may copy and distribute verbatim copies of the Program's
source code as you receive it, in any medium, provided that you
conspicuously and appropriately publish on each copy an appropriate
copyright notice and disclaimer of warranty; keep intact all the
notices that refer to this License and to the absence of any warranty;
and give any other recipients of the Program a copy of this License
along with the Program.

You may charge a fee for the physical act of transferring a copy, and
you may at your option offer warranty protection in exchange for a fee.

  2. You may modify your copy or copies of the Program or any portion
of it, thus forming a work based on the Program, and copy and
distribute such modifications or work under the terms of Section 1
above, provided that you also meet all of these conditions:

    a) You must cause the modified files to carry prominent notices
    stating that you changed the files and the date of any change.

    b) You must cause any work that you distribute or publish, that in
    whole or in part contains or is derived from the Program or any
    part thereof, to be licensed as a whole at no charge to all third
    parties under the terms of this License.

    c) If the modified program normally reads commands interactively
    when run, you must cause it, when started running for such
    interactive use in the most ordinary way, to print or display an
    announcement including an appropriate copyright notice and a
    notice that there is no warranty (or else, saying that you provide
    a warranty) and that users may redistribute the program under
    these conditions, and telling the user how to view a copy of this
    License.  (Exception: if the Program itself is interactive but
    does not normally print such an announcement, your work based on
    the Program is not required to print an announcement.)

These requirements apply to the modified work as a whole.  If
identifiable sections of that work are not derived from the Program,
and can be reasonably considered independent and separate works in
themselves, then this License, and its terms, do not apply to those
sections when you distribute them as separate works.  But when you
distribute the same sections as part of a whole which is a work based
on the Program, the distribution of the whole must be on the terms of
this License, whose permissions for other licensees extend to the
entire whole, and thus to each and every part regardless of who wrote it.

Thus, it is not the intent of this section to claim rights or contest
your rights to work written entirely by you; rather, the intent is to
exercise the right to control the distribution of derivative or
collective works based on the Program.

In addition, mere aggregation of another work not based on the Program
with the Program (or with a work based on the Program) on a volume of
a storage or distribution medium does not bring the other work under
the scope of this License.

  3. You may copy and distribute the Program (or a work based on it,
under Section 2) in object code or executable form under the terms of
Sections 1 and 2 above provided that you also do one of the following:

    a) Accompany it with the complete corresponding machine-readable
    source code, which must be distributed under the terms of Sections
    1 and 2 above on a medium customarily used for software interchange; or,

    b) Accompany it with a written offer, valid for at least three
    years, to give any third party, for a charge no more than your
    cost of physically performing source distribution, a complete
    machine-readable copy of the corresponding source code, to be
    distributed under the terms of Sections 1 and 2 above on a medium
    customarily used for software interchange; or,

    c) Accompany it with the information you received as to the offer
    to distribute corresponding source code.  (This alternative is
    allowed only for noncommercial distribution and only if you
    received the program in object code or executable form with such
    an offer, in accord with Subsection b above.)

The source code for a work means the preferred form of the work for
making modifications to it.  For an executable work, complete source
code means all the source code for all modules it contains, plus any
associated interface definition files, plus the scripts used to
control compilation and installation of the executable.  However, as a
special exception, the source code distributed need not include
anything that is normally distributed (in either source or binary
form) with the major components (compiler, kernel, and so on) of the
operating system on which the executable runs, unless that component
itself accompanies the executable.

If distribution of executable or object code is made by offering
access to copy from a designated place, then offering equivalent
access to copy the source code from the same place counts as
distribution of the source code, even though third parties are not
compelled to copy the source along with the object code.

  4. You may not copy, modify, sublicense, or distribute the Program
except as expressly provided under this License.  Any attempt
otherwise to copy, modify, sublicense or distribute the Program is
void, and will automatically terminate your rights under this License.
However, parties who have received copies, or rights, from you under
this License will not have their licenses terminated so long as such
parties remain in full compliance.

  5. You are not required to accept this License, since you have not
signed it.  However, nothing else grants you permission to modify or
distribute the Program or its derivative works.  These actions are
prohibited by law if you do not accept this License.  Therefore, by
modifying or distributing the Program (or any work based on the
Program), you indicate your acceptance of this License to do so, and
all its terms and conditions for copying, distributing or modifying
the Program or works based on it.

  6. Each time you redistribute the Program (or any work based on the
Program), the recipient automatically receives a license from the
original licensor to copy, distribute or modify the Program subject to
these terms and conditions.  You may not impose any further
restrictions on the recipients' exercise of the rights granted herein.
You are not responsible for enforcing compliance by third parties to
this License.

  7. If, as a consequence of a court judgment or allegation of patent
infringement or for any other reason (not limited to patent issues),
conditions are imposed on you (whether by court order, agreement or
otherwise) that contradict the conditions of this License, they do not
excuse you from the conditions of this License.  If you cannot
distribute so as to satisfy simultaneously your obligations under this
License and any other pertinent obligations, then as a consequence you
may not distribute the Program at all.  For example, if a patent
license would not permit royalty-free redistribution of the Program by
all those who receive copies directly or indirectly through you, then
the only way you could satisfy both it and this License would be to
refrain entirely from distribution of the Program.

If any portion of this section is held invalid or unenforceable under
any particular circumstance, the balance of the section is intended to
apply and the section as a whole is intended to apply in other
circumstances.

It is not the purpose of this section to induce you to infringe any
patents or other property right claims or to contest validity of any
such claims; this section has the sole purpose of protecting the
integrity of the free software distribution system, which is
implemented by public license practices.  Many people have made
generous contributions to the wide range of software distributed
through that system in reliance on consistent application of that
system; it is up to the author/donor to decide if he or she is willing
to distribute software through any other system and a licensee cannot
impose that choice.

This section is intended to make thoroughly clear what is believed to
be a consequence of the rest of this License.

  8. If the distribution and/or use of the Program is restricted in
certain countries either by patents or by copyrighted interfaces, the
original copyright holder who places the Program under this License
may add an explicit geographical distribution limitation excluding
those countries, so that distribution is permitted only in or among
countries not thus excluded.  In such case, this License incorporates
the limitation as if written in the body of this License.

  9. The Free Software Foundation may publish revised and/or new versions
of the General Public License from time to time.  Such new versions will
be similar in spirit to the present version, but may differ in detail to
address new problems or concerns.

Each version is given a distinguishing version number.  If the Program
specifies a version number of this License which applies to it and "any
later version", you have the option of following the terms and conditions
either of that version or of any later version published by the Free
Software Foundation.  If the Program does not specify a version number of
this License, you may choose any version ever published by the Free Software
Foundation.

  10. If you wish to incorporate parts of the Program into other free
programs whose distribution conditions are different, write to the author
to ask for permission.  For software which is copyrighted by the Free
Software Foundation, write to the Free Software Foundation; we sometimes
make exceptions for this.  Our decision will be guided by the two goals
of preserving the free status of all derivatives of our free software and
of promoting the sharing and reuse of software generally.

			    NO WARRANTY

  11. BECAUSE THE PROGRAM IS LICENSED FREE OF CHARGE, THERE IS NO WARRANTY
FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW.  EXCEPT WHEN
OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES
PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED
OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.  THE ENTIRE RISK AS
TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU.  SHOULD THE
PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING,
REPAIR OR CORRECTION.

  12. IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING
WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MAY MODIFY AND/OR
REDISTRIBUTE THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES,
INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING
OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED
TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY
YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER
PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES.

		     END OF TERMS AND CONDITIONS

	    How to Apply These Terms to Your New Programs

  If you develop a new program, and you want it to be of the greatest
possible use to the public, the best way to achieve this is to make it
free software which everyone can redistribute and change under these terms.

  To do so, attach the following notices to the program.  It is safest
to attach them to the start of each source file to most effectively
convey the exclusion of warranty; and each file should have at least
the "copyright" line and a pointer to where the full notice is found.

    <one line to give the program's name and a brief idea of what it does.>
    Copyright (C) <year>  <name of author>

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

Also add information on how to contact you by electronic and paper mail.

If the program is interactive, make it output a short notice like this
when it starts in an interactive mode:

    Gnomovision version 69, Copyright (C) year name of author
    Gnomovision comes with ABSOLUTELY NO WARRANTY; for details type show w'.
    This is free software, and you are welcome to redistribute it
    under certain conditions; type show c' for details.

The hypothetical commands show w' and show c' should show the appropriate
parts of the General Public License.  Of course, the commands you use may
be called something other than show w' and show c'; they could even be
mouse-clicks or menu items--whatever suits your program.

You should also get your employer (if you work as a programmer) or your
school, if any, to sign a "copyright disclaimer" for the program, if
necessary.  Here is a sample; alter the names:

  Yoyodyne, Inc., hereby disclaims all copyright interest in the program
  Gnomovision' (which makes passes at compilers) written by James Hacker.

  <signature of Ty Coon>, 1 April 1989
  Ty Coon, President of Vice

This General Public License does not permit incorporating your program into
proprietary programs.  If your program is a subroutine library, you may
consider it more useful to permit linking proprietary applications with the
library.  If this is what you want to do, use the GNU Lesser General
Public License instead of this License.
This is an [inline link](/url "title"){.class #inline-link}.

This is a [reference link][refid].

This is an ![inline image](/img "title"){.class #inline-img}.

This is a ![reference image][refid].

[refid]: /path/to/something (Title) { .class #ref data-key=val }

Just a [URL](/url/).

[URL and title](/url/ "title").

[URL and title](/url/  "title preceded by two spaces").

[URL and title](/url/	"title preceded by a tab").

[URL and title](/url/ "title has spaces afterward"  ).

[URL wrapped in angle brackets](</url/>).

[URL w/ angle brackets + title](</url/> "Here's the title").

[Empty]().

[With parens in the URL](http://en.wikipedia.org/wiki/WIMP_(computing))

(With outer parens and [parens in url](/foo(bar)))


[With parens in the URL](/foo(bar) "and a title")

(With outer parens and [parens in url](/foo(bar) "and a title"))
Foo [bar] [1].

Foo [bar][1].

Foo [bar]
[1].

[1]: /url/  "Title"


With [embedded [brackets]] [b].


Indented [once][].

Indented [twice][].

Indented [thrice][].

Indented [four][] times.

 [once]: /url

  [twice]: /url

   [thrice]: /url

    [four]: /url


[b]: /url/

* * *

[this] [this] should work

So should [this][this].

And [this] [].

And [this][].

And [this].

But not [that] [].

Nor [that][].

Nor [that].

[Something in brackets like [this][] should work]

[Same with [this].]

In this case, [this](/somethingelse/) points to something else.

Backslashing should suppress \[this] and [this\].

[this]: foo


* * *

Here's one where the [link
breaks] across lines.

Here's another where the [link 
breaks] across lines, but with a line-ending space.


[link breaks]: /url/
This is the [simple case].

[simple case]: /simple



This one has a [line
break].

This one has a [line 
break] with a line-ending space.

[line break]: /foo


[this] [that] and the [other]

[this]: /this
[that]: /that
[other]: /other
Foo [bar][].

Foo [bar](/url/ "Title with "quotes" inside").


  [bar]: /url/ "Title with "quotes" inside"

Markdown: Basics
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a class="selected" title="Markdown Basics">Basics</a></li>
    <li><a href="/projects/markdown/syntax" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


Getting the Gist of Markdown's Formatting Syntax
------------------------------------------------

This page offers a brief overview of what it's like to use Markdown.
The [syntax page] [s] provides complete, detailed documentation for
every feature, but Markdown should be very easy to pick up simply by
looking at a few examples of it in action. The examples on this page
are written in a before/after style, showing example syntax and the
HTML output produced by Markdown.

It's also helpful to simply try Markdown out; the [Dingus] [d] is a
web application that allows you type your own Markdown-formatted text
and translate it to XHTML.

**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL] [src].

  [s]: /projects/markdown/syntax  "Markdown Syntax"
  [d]: /projects/markdown/dingus  "Markdown Dingus"
  [src]: /projects/markdown/basics.text


## Paragraphs, Headers, Blockquotes ##

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

Markdown offers two styles of headers: *Setext* and *atx*.
Setext-style headers for <h1> and <h2> are created by
"underlining" with equal signs (=) and hyphens (-), respectively.
To create an atx-style header, you put 1-6 hash marks (#) at the
beginning of the line -- the number of hashes equals the resulting
HTML header level.

Blockquotes are indicated using email-style '>' angle brackets.

Markdown:

    A First Level Header
    ====================
    
    A Second Level Header
    ---------------------

    Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.

    The quick brown fox jumped over the lazy
    dog's back.
    
    ### Header 3

    > This is a blockquote.
    > 
    > This is the second paragraph in the blockquote.
    >
    > ## This is an H2 in a blockquote


Output:

    <h1>A First Level Header</h1>
    
    <h2>A Second Level Header</h2>
    
    <p>Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.</p>
    
    <p>The quick brown fox jumped over the lazy
    dog's back.</p>
    
    <h3>Header 3</h3>
    
    <blockquote>
        <p>This is a blockquote.</p>
        
        <p>This is the second paragraph in the blockquote.</p>
        
        <h2>This is an H2 in a blockquote</h2>
    </blockquote>



### Phrase Emphasis ###

Markdown uses asterisks and underscores to indicate spans of emphasis.

Markdown:

    Some of these words *are emphasized*.
    Some of these words _are emphasized also_.
    
    Use two asterisks for **strong emphasis**.
    Or, if you prefer, __use two underscores instead__.

Output:

    <p>Some of these words <em>are emphasized</em>.
    Some of these words <em>are emphasized also</em>.</p>
    
    <p>Use two asterisks for <strong>strong emphasis</strong>.
    Or, if you prefer, <strong>use two underscores instead</strong>.</p>
   


## Lists ##

Unordered (bulleted) lists use asterisks, pluses, and hyphens (*,
+, and -) as list markers. These three markers are
interchangable; this:

    *   Candy.
    *   Gum.
    *   Booze.

this:

    +   Candy.
    +   Gum.
    +   Booze.

and this:

    -   Candy.
    -   Gum.
    -   Booze.

all produce the same output:

    <ul>
    <li>Candy.</li>
    <li>Gum.</li>
    <li>Booze.</li>
    </ul>

Ordered (numbered) lists use regular numbers, followed by periods, as
list markers:

    1.  Red
    2.  Green
    3.  Blue

Output:

    <ol>
    <li>Red</li>
    <li>Green</li>
    <li>Blue</li>
    </ol>

If you put blank lines between items, you'll get <p> tags for the
list item text. You can create multi-paragraph list items by indenting
the paragraphs by 4 spaces or 1 tab:

    *   A list item.
    
        With multiple paragraphs.

    *   Another item in the list.

Output:

    <ul>
    <li><p>A list item.</p>
    <p>With multiple paragraphs.</p></li>
    <li><p>Another item in the list.</p></li>
    </ul>
    


### Links ###

Markdown supports two styles for creating links: *inline* and
*reference*. With both styles, you use square brackets to delimit the
text you want to turn into a link.

Inline-style links use parentheses immediately after the link text.
For example:

    This is an [example link](http://example.com/).

Output:

    <p>This is an <a href="http://example.com/">
    example link</a>.</p>

Optionally, you may include a title attribute in the parentheses:

    This is an [example link](http://example.com/ "With a Title").

Output:

    <p>This is an <a href="http://example.com/" title="With a Title">
    example link</a>.</p>

Reference-style links allow you to refer to your links by names, which
you define elsewhere in your document:

    I get 10 times more traffic from [Google][1] than from
    [Yahoo][2] or [MSN][3].

    [1]: http://google.com/        "Google"
    [2]: http://search.yahoo.com/  "Yahoo Search"
    [3]: http://search.msn.com/    "MSN Search"

Output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from <a href="http://search.yahoo.com/"
    title="Yahoo Search">Yahoo</a> or <a href="http://search.msn.com/"
    title="MSN Search">MSN</a>.</p>

The title attribute is optional. Link names may contain letters,
numbers and spaces, but are *not* case sensitive:

    I start my morning with a cup of coffee and
    [The New York Times][NY Times].

    [ny times]: http://www.nytimes.com/

Output:

    <p>I start my morning with a cup of coffee and
    <a href="http://www.nytimes.com/">The New York Times</a>.</p>


### Images ###

Image syntax is very much like link syntax.

Inline (titles are optional):

    ![alt text](/path/to/img.jpg "Title")

Reference-style:

    ![alt text][id]

    [id]: /path/to/img.jpg "Title"

Both of the above examples produce the same output:

    <img src="/path/to/img.jpg" alt="alt text" title="Title" />



### Code ###

In a regular paragraph, you can create code span by wrapping text in
backtick quotes. Any ampersands (&) and angle brackets (< or
>) will automatically be translated into HTML entities. This makes
it easy to use Markdown to write about HTML example code:

    I strongly recommend against using any <blink> tags.

    I wish SmartyPants used named entities like &mdash;
    instead of decimal-encoded entites like &#8212;.

Output:

    <p>I strongly recommend against using any
    <code>&lt;blink&gt;</code> tags.</p>
    
    <p>I wish SmartyPants used named entities like
    <code>&amp;mdash;</code> instead of decimal-encoded
    entites like <code>&amp;#8212;</code>.</p>


To specify an entire block of pre-formatted code, indent every line of
the block by 4 spaces or 1 tab. Just like with code spans, &, <,
and > characters will be escaped automatically.

Markdown:

    If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:

        <blockquote>
            <p>For example.</p>
        </blockquote>

Output:

    <p>If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:</p>
    
    <pre><code>&lt;blockquote&gt;
        &lt;p&gt;For example.&lt;/p&gt;
    &lt;/blockquote&gt;
    </code></pre>
Markdown: Syntax
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a href="/projects/markdown/basics" title="Markdown Basics">Basics</a></li>
    <li><a class="selected" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


*   [Overview](#overview)
    *   [Philosophy](#philosophy)
    *   [Inline HTML](#html)
    *   [Automatic Escaping for Special Characters](#autoescape)
*   [Block Elements](#block)
    *   [Paragraphs and Line Breaks](#p)
    *   [Headers](#header)
    *   [Blockquotes](#blockquote)
    *   [Lists](#list)
    *   [Code Blocks](#precode)
    *   [Horizontal Rules](#hr)
*   [Span Elements](#span)
    *   [Links](#link)
    *   [Emphasis](#em)
    *   [Code](#code)
    *   [Images](#img)
*   [Miscellaneous](#misc)
    *   [Backslash Escapes](#backslash)
    *   [Automatic Links](#autolink)


**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL][src].

  [src]: /projects/markdown/syntax.text

* * *

<h2 id="overview">Overview</h2>

<h3 id="philosophy">Philosophy</h3>

Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

Readability, however, is emphasized above all else. A Markdown-formatted
document should be publishable as-is, as plain text, without looking
like it's been marked up with tags or formatting instructions. While
Markdown's syntax has been influenced by several existing text-to-HTML
filters -- including [Setext] [1], [atx] [2], [Textile] [3], [reStructuredText] [4],
[Grutatext] [5], and [EtText] [6] -- the single biggest source of
inspiration for Markdown's syntax is the format of plain text email.

  [1]: http://docutils.sourceforge.net/mirror/setext.html
  [2]: http://www.aaronsw.com/2002/atx/
  [3]: http://textism.com/tools/textile/
  [4]: http://docutils.sourceforge.net/rst.html
  [5]: http://www.triptico.com/software/grutatxt.html
  [6]: http://ettext.taint.org/doc/

To this end, Markdown's syntax is comprised entirely of punctuation
characters, which punctuation characters have been carefully chosen so
as to look like what they mean. E.g., asterisks around a word actually
look like \*emphasis\*. Markdown lists look like, well, lists. Even
blockquotes look like quoted passages of text, assuming you've ever
used email.



<h3 id="html">Inline HTML</h3>

Markdown's syntax is intended for one purpose: to be used as a
format for *writing* for the web.

Markdown is not a replacement for HTML, or even close to it. Its
syntax is very small, corresponding only to a very small subset of
HTML tags. The idea is *not* to create a syntax that makes it easier
to insert HTML tags. In my opinion, HTML tags are already easy to
insert. The idea for Markdown is to make it easy to read, write, and
edit prose. HTML is a *publishing* format; Markdown is a *writing*
format. Thus, Markdown's formatting syntax only addresses issues that
can be conveyed in plain text.

For any markup that is not covered by Markdown's syntax, you simply
use HTML itself. There's no need to preface it or delimit it to
indicate that you're switching from Markdown to HTML; you just use
the tags.

The only restrictions are that block-level HTML elements -- e.g. <div>,
<table>, <pre>, <p>, etc. -- must be separated from surrounding
content by blank lines, and the start and end tags of the block should
not be indented with tabs or spaces. Markdown is smart enough not
to add extra (unwanted) <p> tags around HTML block-level tags.

For example, to add an HTML table to a Markdown article:

    This is a regular paragraph.

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    This is another regular paragraph.

Note that Markdown formatting syntax is not processed within block-level
HTML tags. E.g., you can't use Markdown-style *emphasis* inside an
HTML block.

Span-level HTML tags -- e.g. <span>, <cite>, or <del> -- can be
used anywhere in a Markdown paragraph, list item, or header. If you
want, you can even use HTML tags instead of Markdown formatting; e.g. if
you'd prefer to use HTML <a> or <img> tags instead of Markdown's
link or image syntax, go right ahead.

Unlike block-level HTML tags, Markdown syntax *is* processed within
span-level tags.


<h3 id="autoescape">Automatic Escaping for Special Characters</h3>

In HTML, there are two characters that demand special treatment: <
and &. Left angle brackets are used to start tags; ampersands are
used to denote HTML entities. If you want to use them as literal
characters, you must escape them as entities, e.g. &lt;, and
&amp;.

Ampersands in particular are bedeviling for web writers. If you want to
write about 'AT&T', you need to write 'AT&amp;T'. You even need to
escape ampersands within URLs. Thus, if you want to link to:

    http://images.google.com/images?num=30&q=larry+bird

you need to encode the URL as:

    http://images.google.com/images?num=30&amp;q=larry+bird

in your anchor tag href attribute. Needless to say, this is easy to
forget, and is probably the single most common source of HTML validation
errors in otherwise well-marked-up web sites.

Markdown allows you to use these characters naturally, taking care of
all the necessary escaping for you. If you use an ampersand as part of
an HTML entity, it remains unchanged; otherwise it will be translated
into &amp;.

So, if you want to include a copyright symbol in your article, you can write:

    &copy;

and Markdown will leave it alone. But if you write:

    AT&T

Markdown will translate it to:

    AT&amp;T

Similarly, because Markdown supports [inline HTML](#html), if you use
angle brackets as delimiters for HTML tags, Markdown will treat them as
such. But if you write:

    4 < 5

Markdown will translate it to:

    4 &lt; 5

However, inside Markdown code spans and blocks, angle brackets and
ampersands are *always* encoded automatically. This makes it easy to use
Markdown to write about HTML code. (As opposed to raw HTML, which is a
terrible format for writing about HTML syntax, because every single <
and & in your example code needs to be escaped.)


* * *


<h2 id="block">Block Elements</h2>


<h3 id="p">Paragraphs and Line Breaks</h3>

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing but spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

The implication of the "one or more consecutive lines of text" rule is
that Markdown supports "hard-wrapped" text paragraphs. This differs
significantly from most other text-to-HTML formatters (including Movable
Type's "Convert Line Breaks" option) which translate every line break
character in a paragraph into a <br /> tag.

When you *do* want to insert a <br /> break tag using Markdown, you
end a line with two or more spaces, then type return.

Yes, this takes a tad more effort to create a <br />, but a simplistic
"every line break is a <br />" rule wouldn't work for Markdown.
Markdown's email-style [blockquoting][bq] and multi-paragraph [list items][l]
work best -- and look better -- when you format them with hard breaks.

  [bq]: #blockquote
  [l]:  #list



<h3 id="header">Headers</h3>

Markdown supports two styles of headers, [Setext] [1] and [atx] [2].

Setext-style headers are "underlined" using equal signs (for first-level
headers) and dashes (for second-level headers). For example:

    This is an H1
    =============

    This is an H2
    -------------

Any number of underlining ='s or -'s will work.

Atx-style headers use 1-6 hash characters at the start of the line,
corresponding to header levels 1-6. For example:

    # This is an H1

    ## This is an H2

    ###### This is an H6

Optionally, you may "close" atx-style headers. This is purely
cosmetic -- you can use this if you think it looks better. The
closing hashes don't even need to match the number of hashes
used to open the header. (The number of opening hashes
determines the header level.) :

    # This is an H1 #

    ## This is an H2 ##

    ### This is an H3 ######


<h3 id="blockquote">Blockquotes</h3>

Markdown uses email-style > characters for blockquoting. If you're
familiar with quoting passages of text in an email message, then you
know how to create a blockquote in Markdown. It looks best if you hard
wrap the text and put a > before every line:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    > 
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

Markdown allows you to be lazy and only put the > before the first
line of a hard-wrapped paragraph:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

Blockquotes can be nested (i.e. a blockquote-in-a-blockquote) by
adding additional levels of >:

    > This is the first level of quoting.
    >
    > > This is nested blockquote.
    >
    > Back to the first level.

Blockquotes can contain other Markdown elements, including headers, lists,
and code blocks:

	> ## This is a header.
	> 
	> 1.   This is the first list item.
	> 2.   This is the second list item.
	> 
	> Here's some example code:
	> 
	>     return shell_exec("echo $input | $markdown_script");

Any decent text editor should make email-style quoting easy. For
example, with BBEdit, you can make a selection and choose Increase
Quote Level from the Text menu.


<h3 id="list">Lists</h3>

Markdown supports ordered (numbered) and unordered (bulleted) lists.

Unordered lists use asterisks, pluses, and hyphens -- interchangably
-- as list markers:

    *   Red
    *   Green
    *   Blue

is equivalent to:

    +   Red
    +   Green
    +   Blue

and:

    -   Red
    -   Green
    -   Blue

Ordered lists use numbers followed by periods:

    1.  Bird
    2.  McHale
    3.  Parish

It's important to note that the actual numbers you use to mark the
list have no effect on the HTML output Markdown produces. The HTML
Markdown produces from the above list is:

    <ol>
    <li>Bird</li>
    <li>McHale</li>
    <li>Parish</li>
    </ol>

If you instead wrote the list in Markdown like this:

    1.  Bird
    1.  McHale
    1.  Parish

or even:

    3. Bird
    1. McHale
    8. Parish

you'd get the exact same HTML output. The point is, if you want to,
you can use ordinal numbers in your ordered Markdown lists, so that
the numbers in your source match the numbers in your published HTML.
But if you want to be lazy, you don't have to.

If you do use lazy list numbering, however, you should still start the
list with the number 1. At some point in the future, Markdown may support
starting ordered lists at an arbitrary number.

List markers typically start at the left margin, but may be indented by
up to three spaces. List markers must be followed by one or more spaces
or a tab.

To make lists look nice, you can wrap items with hanging indents:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
        Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
        viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
        Suspendisse id sem consectetuer libero luctus adipiscing.

But if you want to be lazy, you don't have to:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.

If list items are separated by blank lines, Markdown will wrap the
items in <p> tags in the HTML output. For example, this input:

    *   Bird
    *   Magic

will turn into:

    <ul>
    <li>Bird</li>
    <li>Magic</li>
    </ul>

But this:

    *   Bird

    *   Magic

will turn into:

    <ul>
    <li><p>Bird</p></li>
    <li><p>Magic</p></li>
    </ul>

List items may consist of multiple paragraphs. Each subsequent
paragraph in a list item must be intended by either 4 spaces
or one tab:

    1.  This is a list item with two paragraphs. Lorem ipsum dolor
        sit amet, consectetuer adipiscing elit. Aliquam hendrerit
        mi posuere lectus.

        Vestibulum enim wisi, viverra nec, fringilla in, laoreet
        vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
        sit amet velit.

    2.  Suspendisse id sem consectetuer libero luctus adipiscing.

It looks nice if you indent every line of the subsequent
paragraphs, but here again, Markdown will allow you to be
lazy:

    *   This is a list item with two paragraphs.

        This is the second paragraph in the list item. You're
    only required to indent the first line. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit.

    *   Another item in the same list.

To put a blockquote within a list item, the blockquote's >
delimiters need to be indented:

    *   A list item with a blockquote:

        > This is a blockquote
        > inside a list item.

To put a code block within a list item, the code block needs
to be indented *twice* -- 8 spaces or two tabs:

    *   A list item with a code block:

            <code goes here>


It's worth noting that it's possible to trigger an ordered list by
accident, by writing something like this:

    1986. What a great season.

In other words, a *number-period-space* sequence at the beginning of a
line. To avoid this, you can backslash-escape the period:

    1986\. What a great season.



<h3 id="precode">Code Blocks</h3>

Pre-formatted code blocks are used for writing about programming or
markup source code. Rather than forming normal paragraphs, the lines
of a code block are interpreted literally. Markdown wraps a code block
in both <pre> and <code> tags.

To produce a code block in Markdown, simply indent every line of the
block by at least 4 spaces or 1 tab. For example, given this input:

    This is a normal paragraph:

        This is a code block.

Markdown will generate:

    <p>This is a normal paragraph:</p>

    <pre><code>This is a code block.
    </code></pre>

One level of indentation -- 4 spaces or 1 tab -- is removed from each
line of the code block. For example, this:

    Here is an example of AppleScript:

        tell application "Foo"
            beep
        end tell

will turn into:

    <p>Here is an example of AppleScript:</p>

    <pre><code>tell application "Foo"
        beep
    end tell
    </code></pre>

A code block continues until it reaches a line that is not indented
(or the end of the article).

Within a code block, ampersands (&) and angle brackets (< and >)
are automatically converted into HTML entities. This makes it very
easy to include example HTML source code using Markdown -- just paste
it and indent it, and Markdown will handle the hassle of encoding the
ampersands and angle brackets. For example, this:

        <div class="footer">
            &copy; 2004 Foo Corporation
        </div>

will turn into:

    <pre><code>&lt;div class="footer"&gt;
        &amp;copy; 2004 Foo Corporation
    &lt;/div&gt;
    </code></pre>

Regular Markdown syntax is not processed within code blocks. E.g.,
asterisks are just literal asterisks within a code block. This means
it's also easy to use Markdown to write about Markdown's own syntax.



<h3 id="hr">Horizontal Rules</h3>

You can produce a horizontal rule tag (<hr />) by placing three or
more hyphens, asterisks, or underscores on a line by themselves. If you
wish, you may use spaces between the hyphens or asterisks. Each of the
following lines will produce a horizontal rule:

    * * *

    ***

    *****
	
    - - -

    ---------------------------------------

	_ _ _


* * *

<h2 id="span">Span Elements</h2>

<h3 id="link">Links</h3>

Markdown supports two style of links: *inline* and *reference*.

In both styles, the link text is delimited by [square brackets].

To create an inline link, use a set of regular parentheses immediately
after the link text's closing square bracket. Inside the parentheses,
put the URL where you want the link to point, along with an *optional*
title for the link, surrounded in quotes. For example:

    This is [an example](http://example.com/ "Title") inline link.

    [This link](http://example.net/) has no title attribute.

Will produce:

    <p>This is <a href="http://example.com/" title="Title">
    an example</a> inline link.</p>

    <p><a href="http://example.net/">This link</a> has no
    title attribute.</p>

If you're referring to a local resource on the same server, you can
use relative paths:

    See my [About](/about/) page for details.

Reference-style links use a second set of square brackets, inside
which you place a label of your choosing to identify the link:

    This is [an example][id] reference-style link.

You can optionally use a space to separate the sets of brackets:

    This is [an example] [id] reference-style link.

Then, anywhere in the document, you define your link label like this,
on a line by itself:

    [id]: http://example.com/  "Optional Title Here"

That is:

*   Square brackets containing the link identifier (optionally
    indented from the left margin using up to three spaces);
*   followed by a colon;
*   followed by one or more spaces (or tabs);
*   followed by the URL for the link;
*   optionally followed by a title attribute for the link, enclosed
    in double or single quotes.

The link URL may, optionally, be surrounded by angle brackets:

    [id]: <http://example.com/>  "Optional Title Here"

You can put the title attribute on the next line and use extra spaces
or tabs for padding, which tends to look better with longer URLs:

    [id]: http://example.com/longish/path/to/resource/here
        "Optional Title Here"

Link definitions are only used for creating links during Markdown
processing, and are stripped from your document in the HTML output.

Link definition names may constist of letters, numbers, spaces, and punctuation -- but they are *not* case sensitive. E.g. these two links:

	[link text][a]
	[link text][A]

are equivalent.

The *implicit link name* shortcut allows you to omit the name of the
link, in which case the link text itself is used as the name.
Just use an empty set of square brackets -- e.g., to link the word
"Google" to the google.com web site, you could simply write:

	[Google][]

And then define the link:

	[Google]: http://google.com/

Because link names may contain spaces, this shortcut even works for
multiple words in the link text:

	Visit [Daring Fireball][] for more information.

And then define the link:
	
	[Daring Fireball]: http://daringfireball.net/

Link definitions can be placed anywhere in your Markdown document. I
tend to put them immediately after each paragraph in which they're
used, but if you want, you can put them all at the end of your
document, sort of like footnotes.

Here's an example of reference links in action:

    I get 10 times more traffic from [Google] [1] than from
    [Yahoo] [2] or [MSN] [3].

      [1]: http://google.com/        "Google"
      [2]: http://search.yahoo.com/  "Yahoo Search"
      [3]: http://search.msn.com/    "MSN Search"

Using the implicit link name shortcut, you could instead write:

    I get 10 times more traffic from [Google][] than from
    [Yahoo][] or [MSN][].

      [google]: http://google.com/        "Google"
      [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
      [msn]:    http://search.msn.com/    "MSN Search"

Both of the above examples will produce the following HTML output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from
    <a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a>
    or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p>

For comparison, here is the same paragraph written using
Markdown's inline link style:

    I get 10 times more traffic from [Google](http://google.com/ "Google")
    than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or
    [MSN](http://search.msn.com/ "MSN Search").

The point of reference-style links is not that they're easier to
write. The point is that with reference-style links, your document
source is vastly more readable. Compare the above examples: using
reference-style links, the paragraph itself is only 81 characters
long; with inline-style links, it's 176 characters; and as raw HTML,
it's 234 characters. In the raw HTML, there's more markup than there
is text.

With Markdown's reference-style links, a source document much more
closely resembles the final output, as rendered in a browser. By
allowing you to move the markup-related metadata out of the paragraph,
you can add links without interrupting the narrative flow of your
prose.


<h3 id="em">Emphasis</h3>

Markdown treats asterisks (*) and underscores (_) as indicators of
emphasis. Text wrapped with one * or _ will be wrapped with an
HTML <em> tag; double *'s or _'s will be wrapped with an HTML
<strong> tag. E.g., this input:

    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__

will produce:

    <em>single asterisks</em>

    <em>single underscores</em>

    <strong>double asterisks</strong>

    <strong>double underscores</strong>

You can use whichever style you prefer; the lone restriction is that
the same character must be used to open and close an emphasis span.

Emphasis can be used in the middle of a word:

    un*fucking*believable

But if you surround an * or _ with spaces, it'll be treated as a
literal asterisk or underscore.

To produce a literal asterisk or underscore at a position where it
would otherwise be used as an emphasis delimiter, you can backslash
escape it:

    \*this text is surrounded by literal asterisks\*



<h3 id="code">Code</h3>

To indicate a span of code, wrap it with backtick quotes (  ).
Unlike a pre-formatted code block, a code span indicates code within a
normal paragraph. For example:

    Use the printf() function.

will produce:

    <p>Use the <code>printf()</code> function.</p>

To include a literal backtick character within a code span, you can use
multiple backticks as the opening and closing delimiters:

     There is a literal backtick () here.

which will produce this:

    <p><code>There is a literal backtick () here.</code></p>

The backtick delimiters surrounding a code span may include spaces --
one after the opening, one before the closing. This allows you to place
literal backtick characters at the beginning or end of a code span:

	A single backtick in a code span:     
	
	A backtick-delimited string in a code span:   foo  

will produce:

	<p>A single backtick in a code span: <code></code></p>
	
	<p>A backtick-delimited string in a code span: <code>foo</code></p>

With a code span, ampersands and angle brackets are encoded as HTML
entities automatically, which makes it easy to include example HTML
tags. Markdown will turn this:

    Please don't use any <blink> tags.

into:

    <p>Please don't use any <code>&lt;blink&gt;</code> tags.</p>

You can write this:

    &#8212; is the decimal-encoded equivalent of &mdash;.

to produce:

    <p><code>&amp;#8212;</code> is the decimal-encoded
    equivalent of <code>&amp;mdash;</code>.</p>



<h3 id="img">Images</h3>

Admittedly, it's fairly difficult to devise a "natural" syntax for
placing images into a plain text document format.

Markdown uses an image syntax that is intended to resemble the syntax
for links, allowing for two styles: *inline* and *reference*.

Inline image syntax looks like this:

    ![Alt text](/path/to/img.jpg)

    ![Alt text](/path/to/img.jpg "Optional title")

That is:

*   An exclamation mark: !;
*   followed by a set of square brackets, containing the alt
    attribute text for the image;
*   followed by a set of parentheses, containing the URL or path to
    the image, and an optional title attribute enclosed in double
    or single quotes.

Reference-style image syntax looks like this:

    ![Alt text][id]

Where "id" is the name of a defined image reference. Image references
are defined using syntax identical to link references:

    [id]: url/to/image  "Optional title attribute"

As of this writing, Markdown has no syntax for specifying the
dimensions of an image; if this is important to you, you can simply
use regular HTML <img> tags.


* * *


<h2 id="misc">Miscellaneous</h2>

<h3 id="autolink">Automatic Links</h3>

Markdown supports a shortcut style for creating "automatic" links for URLs and email addresses: simply surround the URL or email address with angle brackets. What this means is that if you want to show the actual text of a URL or email address, and also have it be a clickable link, you can do this:

    <http://example.com/>
    
Markdown will turn this into:

    <a href="http://example.com/">http://example.com/</a>

Automatic links for email addresses work similarly, except that
Markdown will also perform a bit of randomized decimal and hex
entity-encoding to help obscure your address from address-harvesting
spambots. For example, Markdown will turn this:

    <address@example.com>

into something like this:

    <a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
    &#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
    &#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
    &#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>

which will render in a browser as a clickable link to "address@example.com".

(This sort of entity-encoding trick will indeed fool many, if not
most, address-harvesting bots, but it definitely won't fool all of
them. It's better than nothing, but an address published in this way
will probably eventually start receiving spam.)



<h3 id="backslash">Backslash Escapes</h3>

Markdown allows you to use backslash escapes to generate literal
characters which would otherwise have special meaning in Markdown's
formatting syntax. For example, if you wanted to surround a word with
literal asterisks (instead of an HTML <em> tag), you can backslashes
before the asterisks, like this:

    \*literal asterisks\*

Markdown provides backslash escapes for the following characters:

    \   backslash
       backtick
    *   asterisk
    _   underscore
    {}  curly braces
    []  square brackets
    ()  parentheses
    #   hash mark
	+	plus sign
	-	minus sign (hyphen)
    .   dot
    !   exclamation mark

# Character Escapes

The MD5 value for + is "26b17225b626fb9238849fd60eabdf60".

# HTML Blocks

<p>test</p>

The MD5 value for <p>test</p> is:

6205333b793f34273d75379350b36826* test
+ test
- test

1. test
2. test

* test
+ test
- test

1. test
2. test
> foo
>
> > bar
>
> foo
Valid nesting:

**[Link](url)**

[**Link**](url)

**[**Link**](url)**

Invalid nesting:

[[Link](url)](url)## Unordered

Asterisks tight:

*	asterisk 1
*	asterisk 2
*	asterisk 3


Asterisks loose:

*	asterisk 1

*	asterisk 2

*	asterisk 3

* * *

Pluses tight:

+	Plus 1
+	Plus 2
+	Plus 3


Pluses loose:

+	Plus 1

+	Plus 2

+	Plus 3

* * *


Minuses tight:

-	Minus 1
-	Minus 2
-	Minus 3


Minuses loose:

-	Minus 1

-	Minus 2

-	Minus 3


## Ordered

Tight:

1.	First
2.	Second
3.	Third

and:

1. One
2. Two
3. Three


Loose using tabs:

1.	First

2.	Second

3.	Third

and using spaces:

1. One

2. Two

3. Three

Multiple paragraphs:

1.	Item 1, graf one.

	Item 2. graf two. The quick brown fox jumped over the lazy dog's
	back.
	
2.	Item 2.

3.	Item 3.



## Nested

*	Tab
	*	Tab
		*	Tab

Here's another:

1. First
2. Second:
	* Fee
	* Fie
	* Foe
3. Third

Same thing but with paragraphs:

1. First

2. Second:
	* Fee
	* Fie
	* Foe

3. Third


This was an error in Markdown 1.0.1:

*	this

	*	sub

	that
[Inline link 1 with parens](/url\(test\) "title").

[Inline link 2 with parens](</url\(test\)> "title").

[Inline link 3 with non-escaped parens](/url(test) "title").

[Inline link 4 with non-escaped parens](</url(test)> "title").

[Reference link 1 with parens][1].

[Reference link 2 with parens][2].

  [1]: /url(test) "title"
  [2]: </url(test)> "title"
This tests for a bug where quotes escaped by PHP when using 
preg_replace with the /e modifier must be correctly unescaped
(hence the _UnslashQuotes function found only in PHP Markdown).



Headers below should appear exactly as they are typed (no backslash
added or removed).

Header "quoted\" again \\""
===========================

Header "quoted\" again \\""
---------------------------

### Header "quoted\" again \\"" ###



Test with tabs for _Detab:

	Code	'block'	with	some	"tabs"	and	"quotes"
[Test](/"style="color:red)
[Test](/'style='color:red)

![](/"style="border-color:red;border-size:1px;border-style:solid)
![](/'style='border-color:red;border-size:1px;border-style:solid)
***This is strong and em.***

So is ***this*** word.

___This is strong and em.___

So is ___this___ word.
# Simple tables

Header 1  | Header 2
--------- | ---------
Cell 1    | Cell 2
Cell 3    | Cell 4

With leading pipes:

| Header 1  | Header 2
| --------- | ---------
| Cell 1    | Cell 2
| Cell 3    | Cell 4

With tailing pipes:

Header 1  | Header 2  |
--------- | --------- |
Cell 1    | Cell 2    |
Cell 3    | Cell 4    |

With leading and tailing pipes:

| Header 1  | Header 2  |
| --------- | --------- |
| Cell 1    | Cell 2    |
| Cell 3    | Cell 4    |

* * *

# One-column one-row table

With leading pipes:

| Header
| -------
| Cell

With tailing pipes:

Header  |
------- |
Cell    |

With leading and tailing pipes:

| Header  |
| ------- |
| Cell    |

* * *

Table alignement:

| Default   | Right     |  Center   |     Left  |
| --------- |:--------- |:---------:| ---------:|
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

Table alignement (alternate spacing):

| Default   | Right     |  Center   |     Left  |
| --------- | :-------- | :-------: | --------: |
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

* * * 

# Empty cells

| Header 1  | Header 2  |
| --------- | --------- |
| A         | B         |
| C         |           |

Header 1  | Header 2
--------- | ---------
A         | B
          | D

* * *

# Missing tailing pipe

Header 1  | Header 2  
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- 
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      

* * *

# Too many pipes in rows

| Header 1  | Header 2  |
| --------- 
| Cell      | Cell      | Extra cell? |
| Cell      | Cell      | Extra cell? |

+	this is a list item
	indented with tabs

+   this is a list item
    indented with spaces

Code:

	this code block is indented by one tab

And:

		this code block is indented by two tabs

And:

	+	this is an example list item
		indented with tabs
	
	+   this is an example list item
	    indented with spaces
> A list within a blockquote:
> 
> *	asterisk 1
> *	asterisk 2
> *	asterisk 3
Paragraph and no space:
* ciao

Paragraph and 1 space:
 * ciao

Paragraph and 3 spaces:
  * ciao

Paragraph and 4 spaces:
   * ciao

Paragraph before header:
#Header

Paragraph before blockquote:
>Some quote.
 .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>


As above: checking for bad interractions with the HTML block parser:

 html
<div>


Some *markdown* formatting.

 html
</div>


Some *markdown*


<div>
    <html>



function test();


<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">

<html>
    <title>

</div>

Two code blocks with no blank line between them:


<div>


<div>


Testing *confusion* with markers in the middle:


<div></div>


Testing mixing with title code blocks


<p>
 
<p>

 
<p>

<p>
 

<Fenced>


Code block starting and ending with empty lines:



<Fenced>




Indented code block containing fenced code block sample:

	
	<Fenced>
	

Fenced code block with indented code block sample:


Some text

	Indented code block sample code


Fenced code block with long markers:


Fenced


Fenced code block with fenced code block markers of different length in it:


In code block

Still in code block

Still in code block


Fenced code block with Markdown header and horizontal rule:


#test
---


Fenced code block with link definitions, footnote definition and 
abbreviation definitions:


[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language


* In a list item with smalish indent:

  
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
  
  
With HTML content.
  

<b>bold</b>


Bug with block level elements in this case:

  <div>
  </div>


Indented code block of a fenced code block:

    
	haha!
	

With class:
  
html
<b>bold</b>

  
 html
<b>bold</b>

  
.html
<b>bold</b>

  
 .html
<b>bold</b>


With extra attribute block:

{.html}
<b>bold</b>

  
 {.html #codeid}
<b>bold</b>


 .html{.bold}
<div>

  
 .html {#codeid}
</div>
First line. <br/>
Second line.

This is a first paragraph,
on multiple lines.
     
This is a second paragraph.
There are spaces in between the two.This is a first paragraph,
on multiple lines.

This is a second paragraph
which has multiple lines too.A first paragraph.



A second paragraph after 3 CR (carriage return).This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
     
A few spaces and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
	
1 tab to separate them and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.

A new long long long long long long long long long long long long long long long long paragraph on 1 line.An ampersand & in the text flow is escaped as an html entity.There is an [ampersand](http://validator.w3.org/check?uri=http://www.w3.org/&verbose=1) in the URI.This is \*an asterisk which should stay as is.This is * an asterisk which should stay as is.\\   backslash
\   backtick
\*   asterisk
\_   underscore
\{\}  curly braces
\[\]  square brackets
\(\)  parentheses
\#   hash mark
\+   plus sign
\-   minus sign (hyphen)
\.   dot
\!   exclamation mark> # heading level 1
> 
> paragraph>A blockquote with a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.

>and a second very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.>This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a blockquote.> A blockquote
> on multiple lines
> like this.>A blockquote 
>on multiple lines 
>like this. >A blockquote
>on multiple lines
>like this.
>
>But it has
>two paragraphs.>A blockquote
>on multiple lines
>like this> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.
> This is the first level of quoting.
>
> > This is nested blockquote.> This is the first level of quoting.
> > This is nested blockquote.
> Back to the first level.
> This is the first level of quoting.
> > This is nested blockquote.
	10 PRINT HELLO INFINITE
	20 GOTO 10    10 PRINT < > &
    20 GOTO 10    10 PRINT HELLO INFINITE
    20 GOTO 10# Contributing to Mardown Test Suite

1. [Getting Involved](#getting-involved)
2. [Discussion](#discussion)
3. [How To Report an Issue](#how-to-report-an-issue)
4. [Editing Markdown Specification](#editing-markdown-specification)
5. [Test Suite Guidelines](#test-suite-guidelines)
6. [Pull Request Guidelines](#pull-request-guidelines)

## Getting Involved

There are a number of ways to get involved with the development of the Markdown Test Suite. If you are a first time contributor to an open source project, you can still add value to this project. You may identify grammar issues, write prose, examples or documentation for the project. You may flag some errors and open new issues.

Read all bits of this document and that will guide you on how to participate.

## Discussion

### Mailing List

The Markdown Test Suite has been started a little bit after the start of the [Markdown Community Group](http://www.w3.org/community/markdown/). You may want to discuss about Markdown and this project on the [group mailing-list](http://lists.w3.org/Archives/Public/public-markdown/).

## How to Report an Issue

Don't be afraid to add details to your issue. The more context you give, the better for people participating to the project. Make a short summary, add a description with the context and give links to places which will help to understand.

## Editing Markdown Specification

There is much needed work on the [Markdown Specification](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html). It doesn't require strong competences in coding. Be systematic in the markup and follow the way it is already organized. Each time you added a new atomic section, create a commit for this specific part.

## Test Suite Guidelines

When proposing new tests, make sure they do not already exist in the current test suite. You will notice that there is a separate section dedicated to the specific extensions that some markdown generators have created. Keep them separate. We want to keep the core clean and close to the original specification of Markdown.

If you are not sure, create an issue.

### Markdown Extensions

Markdown extension tests are accepted. Use the following rules:

- place all extension tests under the test/extensions/ENGINE directory with filename equal to the feature name
- for each ENGINE and add a README.markdown under the engine directory with a link to its specification

where ENGINE is either of:

- a command line utility. E.g. pandoc, kramdown.
- a programming API. E.g. Redcarpet::Markdown.new().
- a programmatically accessible web service. E.g.: GFM via the GitHub API.
- a non programmatically accessible web service. E.g.: Stack Overflow flavored markdown.

To avoid test duplication for common features, use the following rules:

- if file tests/extensions/ENGINE/FEATURE.md is empty or not present, use tests/extensions/FEATURE.md instead
- if file tests/extensions/ENGINE/FEATURE.out not present, use tests/extensions/FEATURE.out instead
- for a given ENGINE, only features which have either a .md or a .out are implemented by that engine.
- in case of different outputs for a single feature input, keep directly under extensions/ only the output case that happens across the most engines

**version**

Only the latest stable version of each ENGINE is considered.

**options**

The IO behavior tested is for engine defaults, without any options (command line options, extra JSON parameters, etc.) passed to the engine.

**external state**

Tests that use external state not present in the markdown input shall not be included in this test suite.

For example, what GFM @user user tags render to also depends on the state of GitHub's databases (only render to a link if user exists), not only on the input markdown.

#### Examples

GFM and the "fenced code block" use the following file structure:

    tests/extensions/gfm/README.markdown
    tests/extensions/gfm/fenced-code-block.md
    tests/extensions/gfm/fenced-code-block.out

where README.markdown contains:

    https://help.github.com/articles/github-flavored-markdown

To avoid duplication with other engines, if the input / output (normalized to DOM) is the same across multiple engines use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

If the input is the same, and outputs are DOM different, but represent the same idea (e.g. both represent computer code) use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/gfm/fenced-code-block.out
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

#### New Extensions

Tests are modular, and if you want to test a new engine for your project, that should be easy to do.

If you feel that the new engine is reasonably popular, please send a pull request adding it.

## Commits and Pull Requests

* Keep your commits clean and commented
* Do not mix in one commit different things. Keep modifications related.
* Do not mix everything in one giant pull request. Create separate pull requests for different topic. That will help to have a more meaningful debate about the pull requests and will help to review the code.
* If it relates to a specific issue, add the number of the issue in the commit message.

Thanks for Contributing
as*te*risks*single asterisks*_single underscores_HTML entities are written using ampersand notation: &copy;These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

This is an H1
=============# This is an H1 # # This is an H1# this is an h1 with two trailing spaces  
A new paragraph.# This is an H1This is an H2
-------------## This is an H2 #### This is an H2### This is an H3 ###### This is an H3#### This is an H4 ######## This is an H4##### This is an H5 ########## This is an H5###### This is an H6  ############ This is an H6- - ----***___-------![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 for everyone"![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 logo for everyone")![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png)We love <code> and & for everything We love code for everything We love code for everything The MIT License (MIT)

Copyright (c) 2013 Karl Dubost

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
A first sentence  
and a line break.A first sentence     
and a line break.This is an automatic link <http://www.w3.org/>[W3C](http://www.w3.org/ "Discover w3c")[W3C](http://www.w3.org/)[World Wide Web Consortium][w3c]

[w3c]: <http://www.w3.org/>[World Wide Web Consortium][]

[World Wide Web Consortium]: http://www.w3.org/[w3c][]

[w3c]: http://www.w3.org/[World Wide Web Consortium] [w3c]

[w3c]: http://www.w3.org/[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/
   "Discover W3C"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ (Discover w3c)[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ 'Discover w3c'[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ "Discover w3c"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/*   a list containing a blockquote

    > this the blockquote in the list* a

        b
*   a list containing a block of code

	    10 PRINT HELLO INFINITE
	    20 GOTO 10*   This is a list item with two paragraphs. Lorem ipsum dolor
	sit amet, consectetuer adipiscing elit. Aliquam hendrerit
	mi posuere lectus.

	Vestibulum enim wisi, viverra nec, fringilla in, laoreet
	vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
	sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.*   This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.1\. ordered list escape1. 1

    - inner par list

2. 2
1. list item 1
8. list item 2
1. list item 31. list item 1
2. list item 2
3. list item 3This is a paragraph
on multiple lines
with hard return.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line. This is a paragraph with a trailing and leading space. This is a paragraph with 1 trailing tab.	  This is a paragraph with 2 leading spaces.   This is a paragraph with 3 leading spaces. This is a paragraph with 1 leading space.This is a paragraph with a trailing space. # Colophon - October 1st, 2014

This project was initiated to provide a test suite for Markdown markup, and eventually create a specification from this test results. A part of of the community has started a new endeavor which seems to get traction as [CommonMark](https://github.com/jgm/stmd). **We are then closing this project** and encourage you to contribute to CommonMark. 

The most interesting part of this project would not have been possible without the dedication of [Ciro Santilli](https://github.com/cirosantilli) @cirosantilli. So big applause and thank you to him.


The rest is kept around for archives and references.

# Markdown Test Suite

Inspired by questions on [W3C Markdown Community Group](http://www.w3.org/community/markdown).

Pull Requests are welcome. See the [CONTRIBUTING Guidelines](https://github.com/karlcow/markdown-testsuite/blob/master/CONTRIBUTING.md)

## Design goals

- Comprehensive.
- Small modularized tests.
- Easy to run tests using any programming language. In particular, data representations must have an implementation on all major languages.
- Develop a consensus based markdown specification at [markdown-spec.html](markdown-spec.html). Visualize it [here](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html).

## Test Scripts

Markdown Test Suite already includes tests for many important markdown engines.

To see what the scripts do run:

    ./cat-all.py -h
    ./run-tests.py -h

To configure the scripts do:

	cp config_local.py.example config_local.py

and edit config_local.py. It is already gitignored.

A Vagrantfile is provided with a provision script that installs all installable engines.

Sample output from run-tests.py:

    blackfriday   |......FFF..............FF...F....................................F....................................|   0.93s  102    7   6%
	gfm           |FF.....F.....F...FFFF..F....F........................FFFF...FF...............FF...F.......F...........| 262.88s  102   20  19%
    hoedown       |..............................F.................................................F.....................|   0.36s  102    2   1%
	kramdown      |......FFF.....FF.......FF.......FF.FFFFFFFFFFFFF.......................F..............................|  30.69s  102   23  22%
    lunamark      |FFFFFF.F.FFFFFFFFFFFF.F.....FFFF..FF............FFFFF..FFFFFFFFFF..............F...FFFFFFFFFFF........|   1.58s  103   53  51%
    markdown_pl   |.....................FFFF...............................F...............F.............................|   2.56s  102    6   5%
    markdown2     |......................................................................................................|   5.39s  103    0   0%
    marked        |..............F.................FFFFFFFFFFFFFFFF......................F.F.............................|   6.22s  102   19  18%
    maruku        |......FFF......F.......F.FFF...............................................FF.........................|  37.02s  102   10   9%
    md2html       |.........................FFF...F............................................FF........................|   7.42s  102    6   5%
    multimarkdown |......FFF....FF...F............FFF.FFFFFFFFFFFFF.....FFFF.........F...................................|   0.58s  102   27  26%
    pandoc        |FF...........F.F.FFFF..FFFFF....FF.FFFFFFFFFFFFF.....FFFF.....FF............FFF.FFF..................F|   1.11s  102   41  40%
    peg_markdown  |.................................................................F....................................|   0.46s  102    1   0%
    rdiscount     |.......F.........................................................F....................................|  25.19s  102    3   2%
    redcarpet     |......................................................................................................|  21.49s  102    0   0%
    showdown      |.......................................................................F..............................|   6.85s  102    1   0%

	Extensions:

    blackfriday   |F..|  0.04s    3    1  33%
	gfm           |F.|   2.37s    2    1  50%
    hoedown       |.|    0.00s    1    0   0%
    lunamark      |F.F|  0.05s    3    2  66%
    kramdown      |..|   0.62s    2    0   0%
    markdown_pl   ||     0.00s    0    0   0%
    markdown2     |F.|   0.14s    2    1  50%
    marked        |F.|   0.13s    2    1  50%
    maruku        |F..|  1.06s    3    1  33%
    md2html       |F.|   0.14s    2    0   0%
    multimarkdown |F.|   0.01s    2    1  50%
    pandoc        |F.|   0.02s    2    1  50%
    peg_markdown  |...|  0.02s    3    0   0%
    rdiscount     |F..|   0.74s    3    1  33%
    redcarpet     |..|   0.42s    2    0   0%
    showdown      |F..|  0.20s    3    1  33%

Where F indicates a failing test.

## Other Noticeable Test Suites

We haven't been the first test suite effort. Some projects have maintained their own test suite for a long time. Hopefully we can reach a state where people agree on the terms of what should be a good test suite for all developers.

- [Original test suite](http://daringfireball.net/projects/downloads/MarkdownTest_1.0.zip)
- [PHP markdown test suite:](https://github.com/michelf/mdtest/tree/master/Markdown.mdtest)
- [Markdown-js test suite](https://github.com/evilstreak/markdown-js/tree/master/test/features)
- [Python markdown 2 test suite](https://github.com/trentm/python-markdown2/tree/master/test/tm-cases)
- [multimarkdown test suite](https://github.com/fletcher/MMD-Test-Suite)
- [John MacFarlane's Standard Markdown spec](https://github.com/jgm/stmd)

In addition we should note the [wonderful work](http://johnmacfarlane.net/babelmark2/) made by John Mac Farlane. The Web service output the differences in between the different markdown implementations. It helps a lot when searching on the most common output.
as**te**risks**double asterisks**__double underscores__* list item 1
* list item 2
* list item 3
- list item 1
- list item 2
- list item 3 * list item 1
 * list item 2
 * list item 3  * list item 1
  * list item 2
  * list item 3   * list item 1
   * list item 2
   * list item 3+ list item 1
+ list item 2
+ list item 3* list item in paragraph

* another list item in paragraph*   This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a list.
*   and yet another long long long long long long long long long long long long long long long long long long long long long long line.*   This is a list item
    with the content on
    multiline and indented.
*   And this another list item
    with the same principle.€Some text about HTML, SGML and HTML4.

Let's talk about the U.S.A., (É.U. or É.-U. d'A. in French).

*[HTML4]: Hyper Text Markup Language version 4
*[HTML]: Hyper Text Markup Language
*[SGML]: Standard Generalized Markup Language
*[U.S.A.]: United States of America
*[É.U.] : États-Unis d'Amérique
*[É.-U. d'A.] : États-Unis d'Amérique

And here we have a CD, some CDs, and some other CD's.

*[CD]: Compact Disk

Let's transfert documents through TCP/IP, using TCP packets.

*[IP]: Internet Protocol
*[TCP]: Transmission Control Protocol

 ---

Bienvenue sur [CMS](http://www.bidulecms.com "Bidule CMS").

*[CMS]: Content Management System

 ---

ATCCE

*[ATCCE]: Abbreviation "Testing" Correct 'Character' < Escapes >* one
* two

1. three
2. four

* one
* two
1. three
2. fourAT&T has an ampersand in their name.

AT&amp;T is another way to write it.

This & that.

4 < 5.

6 > 5.

Here's a [link] [1] with an ampersand in the URL.

Here's a link with an amersand in the link text: [AT&T] [2].

Here's an inline [link](/script?foo=1&bar=2).

Here's an inline [link](</script?foo=1&bar=2>).


[1]: http://example.com/?foo=1&bar=2
[2]: http://att.com/  "AT&T"Link: <http://example.com/>.

With an ampersand: <http://example.com/?foo=1&bar=2>

* In a list?
* <http://example.com/>
* It should.

> Blockquoted: <http://example.com/>

Auto-links should not occur here: <http://example.com/>

	or here: <http://example.com/>These should all get escaped:

Backslash: \\

Backtick: \

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-



These should not, because they occur within a code block:

	Backslash: \\

	Backtick: \

	Asterisk: \*

	Underscore: \_

	Left brace: \{

	Right brace: \}

	Left bracket: \[

	Right bracket: \]

	Left paren: \(

	Right paren: \)

	Greater-than: \>

	Hash: \#

	Period: \.

	Bang: \!

	Plus: \+

	Minus: \-


Nor should these, which occur in code spans:

Backslash: \\

Backtick:   \  

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-


These should get escaped, even though they're matching pairs for
other Markdown constructs:

\*asterisks\*

\_underscores\_

\backticks\

This is a code span with a literal backslash-backtick sequence:   \  

This is a tag with unescaped backticks <span attr='ticks'>bar</span>.

This is a tag with backslashes <span attr='\\backslashes\\'>bar</span>.
  .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>
 

As above: checking for bad interractions with the HTML block parser:

  html
<div>
 

Some *markdown* formatting.

  html
</div>
 

Some *markdown*

 
<div>
    <html>
 

 
function test();
 

<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">
 
<html>
    <title>
 
</div>

Two code blocks with no blank line between them:

 
<div>
 
 
<div>
 

Testing *confusion* with code spans at the HTML block parser:

 
<div></div>
 

Testing mixing with title code blocks

 
<p>

<p>
 

<p>
 
<p>

 
<Fenced>
 

Code block starting and ending with empty lines:
 


<Fenced>


 

Indented code block containing fenced code block sample:

	 
	<Fenced>
	 

Fenced code block with indented code block sample:

 
Some text

	Indented code block sample code
 

Fenced code block with long markers:

 
Fenced
 

Fenced code block with fenced code block markers of different length in it:

 
In code block
 
Still in code block
 
Still in code block
 

Fenced code block with Markdown header and horizontal rule:

 
#test
---
 

Fenced code block with link definitions, footnote definition and
abbreviation definitions:

 
[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language
 

* In a list item with smalish indent:

   
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
   

With HTML content.

 
<b>bold</b>
 

Bug with block level elements in this case:
 
  <div>
  </div>
 

Indented code block of a fenced code block:

     
	haha!
	 

With class:

 html
<b>bold</b>
 

  html
<b>bold</b>
 

 .html
<b>bold</b>
 

  .html
<b>bold</b>
 

With extra attribute block:

 {.html}
<b>bold</b>
 

  {.html #codeid}
<b>bold</b>
 

  .html{.bold}
<div>
 
  
  .html {#codeid}
</div>
 > Example:
> 
>     sub status {
>         print "working";
>     }
> 
> Or:
> 
>     sub status {
>         return "working";
>     }

*	List Item:

		code block

		with a blank line

	within a list item.

*       code block
        as first element of a list item

*	List Item:
	
		code block with whitespace on preceding line
    Codeblock on second line
    <?php
    echo "hello!";
    ?>

foo bar

    <?php
    echo "hello!";

lorem ipsum

    echo "hello!";
    ?>
    
lorem ipsum	code block on the first line
	
Regular text.

    code block indented by spaces

Regular text.

	the lines in this block  
	all contain trailing spaces  

Regular Text.

	code block on the last line<test a=" content of attribute ">

Fix for backticks within HTML tag: <span attr='ticks'>like this</span>

Here's how you put   backticks   in a code span.A simple definition list:

Term 1
:   Definition 1

Term 2
:   Definition 2

With multiple terms:

Term 1
Term 2
:   Definition 1

Term 3
Term 4
:   Definition 2

With multiple definitions:

Term 1
:   Definition 1
:   Definition 2

Term 2
:   Definition 3
:   Definition 4

With multiple lines per definition:

Term 1
:   Definition 1 line 1 ...
Definition 1 line 2
:   Definition 2 line 1 ...
Definition 2 line 2

Term 2
:   Definition 3 line 2 ...
    Definition 3 line 2
:   Definition 4 line 2 ...
    Definition 4 line 2

With paragraphs:

Term 1

:   Definition 1 (paragraph)

Term 2

:   Definition 2 (paragraph)

With multiple paragraphs:

Term 1

:   Definition 1 paragraph 1 line 1 ...
	Definition 1 paragraph 1 line 2

    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)

    Definition 1 paragraph 2 line 1 ...
Definition 1 paragraph 2 line 2 (lazy)

* * *

A mix:

Term 1
Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)
    
    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

:   Definition 2 paragraph 1 line 1 ...
Definition 2 paragraph 1 line 2 (lazy)

Term 3
:   Definition 3 (no paragraph)
:   Definition 4 (no paragraph)
:   Definition 5 line 1 ...
    Definition 5 line 2 (no paragraph)

:   Definition 6 paragraph 1 line 1 ...
Definition 6 paragraph 1 line 2
:   Definition 7 (no paragraph)
:   Definition 8 paragraph 1 line 1 (forced paragraph) ...
    Definition 8 paragraph 1 line 2
    
    Definition 8 paragraph 2 line 1
    
Term 4
:   Definition 9 paragraph 1 line 1 (forced paragraph) ...
    Definition 9 paragraph 1 line 2
    
    Definition 9 paragraph 2 line 1
:   Definition 10 (no paragraph)

* * *

Special cases:

Term

:       code block
        as first element of a definition<michel.fortin@michelf.ca>

International domain names: <help@tūdaliņ.lv>


## Some weird valid email addresses

<abc.123@example.com>

<1234567890@example.com>

<_______@example.com>

<abc+mailbox/department=shipping@example.com>

<!#$%&'*+-/=?^_.{|}@example.com> (all of these characters are allowed)

<"abc@def"@example.com> (anything goes inside quotation marks)

<"Fred Bloggs"@example.com>

<jsmith@[192.0.2.1]>

<"A"@example.com>Combined emphasis:

1.  ***test test***
2.  ___test test___
3.  *test **test***
4.  **test *test***
5.  ***test* test**
6.  ***test** test*
7.  ***test* test**
8.  **test *test***
9.  *test **test***
10. _test __test___
11. __test _test___
12. ___test_ test__
13. ___test__ test_
14. ___test_ test__
15. __test _test___
16. _test __test___
17. *test __test__*
18. **test _test_**
19. **_test_ test**
20. *__test__ test*
21. **_test_ test**
22. **test _test_**
23. *test __test__*
24. _test **test**_
25. __test *test*__
26. __*test* test__
27. _**test** test_
28. __*test* test__
29. __test *test*__
30. _test **test**_


Incorrect nesting:

1.  *test  **test*  test**
2.  _test  __test_  test__
3.  **test  *test** test*
4.  __test  _test__ test_
5.  *test   *test*  test*
6.  _test   _test_  test_
7.  **test **test** test**
8.  __test __test__ test__
9. _**some text_**
10. *__some text*__
11. **_some text**_
12. *__some text*__

No emphasis:

1.  test*  test  *test
2.  test** test **test
3.  test_  test  _test
4.  test__ test __test



Middle-word emphasis (asterisks):

1.  *a*b
2.   a*b*
3.   a*b*c
4. **a**b
5.   a**b**
6.   a**b**c


Middle-word emphasis (underscore):

1.  _a_b
2.   a_b_
3.   a_b_c
4. __a__b
5.   a__b__
6.   a__b__c

my_precious_file.txt


## Tricky Cases

E**. **Test** TestTestTest

E**. **Test** Test Test Test


## Overlong emphasis

Name: ____________  
Organization: ____  
Region/Country: __

_____Cut here_____

____Cut here____

# Regression

_**Note**_: This _is emphasis_.
With asterisks

 * List item
 *
 * List item

With numbers

1. List item
2.
3. List item

With hyphens

- List item
-
- List item

With asterisks

 * List item
 * List item
 *

With numbers

1. List item
2. List item
3.

With hyphens

- List item
- List item
-
This is the first paragraph.[^first]

[^first]:  This is the first note.

* List item one.[^second]
* List item two.[^third]

[^third]: This is the third note, defined out of order.
[^second]: This is the second note.
[^fourth]: This is the fourth note.

# Header[^fourth]

Some paragraph with a footnote[^1], and another[^2].

[^1]: Content for fifth footnote.
[^2]: Content for sixth footnote spaning on 
    three lines, with some span-level markup like
    _emphasis_, a [link][].

[link]: http://michelf.ca/

Another paragraph with a named footnote[^fn-name].

[^fn-name]:
    Footnote beginning on the line next to the marker.

This paragraph should not have a footnote marker since 
the footnote is undefined.[^3]

This paragraph has a second footnote marker to footnote number one.[^1]

This paragraph links to a footnote with plenty of 
block-level content.[^block]

[^block]:
	Paragraph.
	
	*   List item
	
	> Blockquote
	
	    Code block

This paragraph host the footnote reference within a 
footnote test[^reference].

[^reference]:
	This footnote has a footnote of its own.[^nested]

[^nested]:
	This footnote should appear even though it is referenced
	from another footnote. But [^reference] should be litteral
	since the footnote with that name has already been used.

 - - -

Testing unusual footnote name[^1$^!"'].

[^1$^!"']: Haha!

 - - -
 
Footnotes mixed with images[^image-mixed]
![1800 Travel][img6]
![1830 Travel][img7]

[img6]: images/MGR-1800-travel.jpeg "Travel Speeds in 1800"
[^image-mixed]: Footnote Content
[img7]: images/MGR-1830-travel.jpeg "Travel Speeds in 1830"
In Markdown 1.0.0 and earlier. Version
8. This line turns into a list item.
Because a hard-wrapped line in the
middle of a paragraph looked like a
list item.

Here's one with a bullet.
* criminey.
Header  {#id1}
======

Header  { #id2}
------

### Header  {#id3 }
#### Header ##  { #id4 }

 - - -

Header  {.cl}
======

Header  { .cl}
------

### Header  {.cl }
#### Header ##  { .cl }

 - - -

Header  {.cl.class}
======

Header  { .cl .class}
------

### Header  {.cl .class }
#### Header ##  { .cl.class }

 - - -

Header  {#id5.cl.class}
======

Header  { #id6 .cl .class}
------

### Header  {.cl.class#id7 }
#### Header ##  { .cl.class#id8 }
Header
======

Header
------

### Header

 - - -

Header
======
Paragraph

Header
------
Paragraph

### Header
Paragraph

 - - -

Paragraph
Header
======
Paragraph

Paragraph
Header
------
Paragraph

Paragraph
### Header
ParagraphDashes:

---

 ---
 
  ---

   ---

	---

- - -

 - - -
 
  - - -

   - - -

	- - -


Asterisks:

***

 ***
 
  ***

   ***

	***

* * *

 * * *
 
  * * *

   * * *

	* * *


Underscores:

___

 ___
 
  ___

   ___

    ___

_ _ _

 _ _ _
 
  _ _ _

   _ _ _

    _ _ _
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")

Inline within a paragraph: [alt text](/url/).

![alt text](/url/  "title preceded by two spaces")

![alt text](/url/  "title has spaces afterward"  )

![alt text](</url/>)

![alt text](</url/> "with a title").

![Empty]()

![this is a stupid URL](http://example.com/(parens).jpg)


![alt text][foo]

  [foo]: /url/

![alt text][bar]

  [bar]: /url/ "Title here"Simple block on one line:

<div>foo</div>

And nested without indentation:

<div>
<div>
<div>
foo
</div>
<div style=">"/>
</div>
<div>bar</div>
</div>

And with attributes:

<div>
	<div id="foo">
	</div>
</div>

This was broken in 1.0.2b7:

<div class="inlinepage">
<div class="toggleableend">
foo
</div>
</div>
Here's a simple block:

<div>
	foo
</div>

This should be a code block, though:

	<div>
		foo
	</div>

As should this:

	<div>foo</div>

Now, nested:

<div>
	<div>
		<div>
			foo
		</div>
	</div>
</div>

This should just be an HTML comment:

<!-- Comment -->

Multiline:

<!--
Blah
Blah
-->

Code block:

	<!-- Comment -->

Just plain comment, with trailing spaces on the line:

<!-- foo -->   

Code:

	<hr />
	
Hr's:

<hr>

<hr/>

<hr />

<hr>   

<hr/>  

<hr /> 

<hr class="foo" id="bar" />

<hr class="foo" id="bar"/>

<hr class="foo" id="bar" >

<abbr title=" **Attribute Content Is Not A Code Span** ">ACINACS</abbr>

<abbr title="first backtick!">SB</abbr> 
<abbr title="second backtick!">SB</abbr>Paragraph one.

<!-- This is a simple comment -->

<!--
	This is another comment.
-->

Paragraph two.

<!-- one comment block -- -- with two comments -->

The end.
# Markdown inside code blocks

<div markdown="1">
foo
</div>

<div markdown='1'>
foo
</div>

<div markdown=1>
foo
</div>

<table>
<tr><td markdown="1">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="span">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="block">test _emphasis_ (block)</td></tr>
</table>

## More complicated

<table>
<tr><td markdown="1">
* this is _not_ a list item</td></tr>
<tr><td markdown="span">
* this is _not_ a list item</td></tr>
<tr><td markdown="block">
* this _is_ a list item
</td></tr>
</table>

## With indent

<div>
    <div markdown="1">
    This text is no code block: if it was, the 
    closing <div> would be too and the HTML block 
    would be invalid.

    Markdown content in HTML blocks is assumed to be 
    indented the same as the block opening tag.

    **This should be the third paragraph after the header.**
    </div>
</div>

## Code block with rogue </div>s in Markdown code span and block

<div>
    <div markdown="1">

    This is a code block however:

        </div>

    Funny isn't it? Here is a code span: </div>.

    </div>
</div>

<div>
  <div markdown="1">
    * List item, not a code block

Some text

      This is a code block.
  </div>
</div>

## No code block in markdown span mode

<p markdown="1">
    This is not a code block since Markdown parse paragraph 
    content as span. Code spans like </p> are allowed though.
</p>

<p markdown="1">_Hello_ _world_</p>

## Preserving attributes and tags on more than one line:

<p class="test" markdown="1" 
id="12">
Some _span_ content.
</p>


## Header confusion bug

<table class="canvas">
<tr>
<td id="main" markdown="1"> H e l l o   World!
============

Hello World!</td>
</tr>
</table>
Here is a block tag ins:

<ins>
<p>Some text</p>
</ins>

<ins>And here it is inside a paragraph.</ins>

And here it is <ins>in the middle of</ins> a paragraph.

<del>
<p>Some text</p>
</del>

<del>And here is ins as a paragraph.</del>

And here it is <del>in the middle of</del> a paragraph.
		    GNU GENERAL PUBLIC LICENSE
		       Version 2, June 1991

 Copyright (C) 1989, 1991 Free Software Foundation, Inc.,
 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

			    Preamble

  The licenses for most software are designed to take away your
freedom to share and change it.  By contrast, the GNU General Public
License is intended to guarantee your freedom to share and change free
software--to make sure the software is free for all its users.  This
General Public License applies to most of the Free Software
Foundation's software and to any other program whose authors commit to
using it.  (Some other Free Software Foundation software is covered by
the GNU Lesser General Public License instead.)  You can apply it to
your programs, too.

  When we speak of free software, we are referring to freedom, not
price.  Our General Public Licenses are designed to make sure that you
have the freedom to distribute copies of free software (and charge for
this service if you wish), that you receive source code or can get it
if you want it, that you can change the software or use pieces of it
in new free programs; and that you know you can do these things.

  To protect your rights, we need to make restrictions that forbid
anyone to deny you these rights or to ask you to surrender the rights.
These restrictions translate to certain responsibilities for you if you
distribute copies of the software, or if you modify it.

  For example, if you distribute copies of such a program, whether
gratis or for a fee, you must give the recipients all the rights that
you have.  You must make sure that they, too, receive or can get the
source code.  And you must show them these terms so they know their
rights.

  We protect your rights with two steps: (1) copyright the software, and
(2) offer you this license which gives you legal permission to copy,
distribute and/or modify the software.

  Also, for each author's protection and ours, we want to make certain
that everyone understands that there is no warranty for this free
software.  If the software is modified by someone else and passed on, we
want its recipients to know that what they have is not the original, so
that any problems introduced by others will not reflect on the original
authors' reputations.

  Finally, any free program is threatened constantly by software
patents.  We wish to avoid the danger that redistributors of a free
program will individually obtain patent licenses, in effect making the
program proprietary.  To prevent this, we have made it clear that any
patent must be licensed for everyone's free use or not licensed at all.

  The precise terms and conditions for copying, distribution and
modification follow.

		    GNU GENERAL PUBLIC LICENSE
   TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

  0. This License applies to any program or other work which contains
a notice placed by the copyright holder saying it may be distributed
under the terms of this General Public License.  The "Program", below,
refers to any such program or work, and a "work based on the Program"
means either the Program or any derivative work under copyright law:
that is to say, a work containing the Program or a portion of it,
either verbatim or with modifications and/or translated into another
language.  (Hereinafter, translation is included without limitation in
the term "modification".)  Each licensee is addressed as "you".

Activities other than copying, distribution and modification are not
covered by this License; they are outside its scope.  The act of
running the Program is not restricted, and the output from the Program
is covered only if its contents constitute a work based on the
Program (independent of having been made by running the Program).
Whether that is true depends on what the Program does.

  1. You may copy and distribute verbatim copies of the Program's
source code as you receive it, in any medium, provided that you
conspicuously and appropriately publish on each copy an appropriate
copyright notice and disclaimer of warranty; keep intact all the
notices that refer to this License and to the absence of any warranty;
and give any other recipients of the Program a copy of this License
along with the Program.

You may charge a fee for the physical act of transferring a copy, and
you may at your option offer warranty protection in exchange for a fee.

  2. You may modify your copy or copies of the Program or any portion
of it, thus forming a work based on the Program, and copy and
distribute such modifications or work under the terms of Section 1
above, provided that you also meet all of these conditions:

    a) You must cause the modified files to carry prominent notices
    stating that you changed the files and the date of any change.

    b) You must cause any work that you distribute or publish, that in
    whole or in part contains or is derived from the Program or any
    part thereof, to be licensed as a whole at no charge to all third
    parties under the terms of this License.

    c) If the modified program normally reads commands interactively
    when run, you must cause it, when started running for such
    interactive use in the most ordinary way, to print or display an
    announcement including an appropriate copyright notice and a
    notice that there is no warranty (or else, saying that you provide
    a warranty) and that users may redistribute the program under
    these conditions, and telling the user how to view a copy of this
    License.  (Exception: if the Program itself is interactive but
    does not normally print such an announcement, your work based on
    the Program is not required to print an announcement.)

These requirements apply to the modified work as a whole.  If
identifiable sections of that work are not derived from the Program,
and can be reasonably considered independent and separate works in
themselves, then this License, and its terms, do not apply to those
sections when you distribute them as separate works.  But when you
distribute the same sections as part of a whole which is a work based
on the Program, the distribution of the whole must be on the terms of
this License, whose permissions for other licensees extend to the
entire whole, and thus to each and every part regardless of who wrote it.

Thus, it is not the intent of this section to claim rights or contest
your rights to work written entirely by you; rather, the intent is to
exercise the right to control the distribution of derivative or
collective works based on the Program.

In addition, mere aggregation of another work not based on the Program
with the Program (or with a work based on the Program) on a volume of
a storage or distribution medium does not bring the other work under
the scope of this License.

  3. You may copy and distribute the Program (or a work based on it,
under Section 2) in object code or executable form under the terms of
Sections 1 and 2 above provided that you also do one of the following:

    a) Accompany it with the complete corresponding machine-readable
    source code, which must be distributed under the terms of Sections
    1 and 2 above on a medium customarily used for software interchange; or,

    b) Accompany it with a written offer, valid for at least three
    years, to give any third party, for a charge no more than your
    cost of physically performing source distribution, a complete
    machine-readable copy of the corresponding source code, to be
    distributed under the terms of Sections 1 and 2 above on a medium
    customarily used for software interchange; or,

    c) Accompany it with the information you received as to the offer
    to distribute corresponding source code.  (This alternative is
    allowed only for noncommercial distribution and only if you
    received the program in object code or executable form with such
    an offer, in accord with Subsection b above.)

The source code for a work means the preferred form of the work for
making modifications to it.  For an executable work, complete source
code means all the source code for all modules it contains, plus any
associated interface definition files, plus the scripts used to
control compilation and installation of the executable.  However, as a
special exception, the source code distributed need not include
anything that is normally distributed (in either source or binary
form) with the major components (compiler, kernel, and so on) of the
operating system on which the executable runs, unless that component
itself accompanies the executable.

If distribution of executable or object code is made by offering
access to copy from a designated place, then offering equivalent
access to copy the source code from the same place counts as
distribution of the source code, even though third parties are not
compelled to copy the source along with the object code.

  4. You may not copy, modify, sublicense, or distribute the Program
except as expressly provided under this License.  Any attempt
otherwise to copy, modify, sublicense or distribute the Program is
void, and will automatically terminate your rights under this License.
However, parties who have received copies, or rights, from you under
this License will not have their licenses terminated so long as such
parties remain in full compliance.

  5. You are not required to accept this License, since you have not
signed it.  However, nothing else grants you permission to modify or
distribute the Program or its derivative works.  These actions are
prohibited by law if you do not accept this License.  Therefore, by
modifying or distributing the Program (or any work based on the
Program), you indicate your acceptance of this License to do so, and
all its terms and conditions for copying, distributing or modifying
the Program or works based on it.

  6. Each time you redistribute the Program (or any work based on the
Program), the recipient automatically receives a license from the
original licensor to copy, distribute or modify the Program subject to
these terms and conditions.  You may not impose any further
restrictions on the recipients' exercise of the rights granted herein.
You are not responsible for enforcing compliance by third parties to
this License.

  7. If, as a consequence of a court judgment or allegation of patent
infringement or for any other reason (not limited to patent issues),
conditions are imposed on you (whether by court order, agreement or
otherwise) that contradict the conditions of this License, they do not
excuse you from the conditions of this License.  If you cannot
distribute so as to satisfy simultaneously your obligations under this
License and any other pertinent obligations, then as a consequence you
may not distribute the Program at all.  For example, if a patent
license would not permit royalty-free redistribution of the Program by
all those who receive copies directly or indirectly through you, then
the only way you could satisfy both it and this License would be to
refrain entirely from distribution of the Program.

If any portion of this section is held invalid or unenforceable under
any particular circumstance, the balance of the section is intended to
apply and the section as a whole is intended to apply in other
circumstances.

It is not the purpose of this section to induce you to infringe any
patents or other property right claims or to contest validity of any
such claims; this section has the sole purpose of protecting the
integrity of the free software distribution system, which is
implemented by public license practices.  Many people have made
generous contributions to the wide range of software distributed
through that system in reliance on consistent application of that
system; it is up to the author/donor to decide if he or she is willing
to distribute software through any other system and a licensee cannot
impose that choice.

This section is intended to make thoroughly clear what is believed to
be a consequence of the rest of this License.

  8. If the distribution and/or use of the Program is restricted in
certain countries either by patents or by copyrighted interfaces, the
original copyright holder who places the Program under this License
may add an explicit geographical distribution limitation excluding
those countries, so that distribution is permitted only in or among
countries not thus excluded.  In such case, this License incorporates
the limitation as if written in the body of this License.

  9. The Free Software Foundation may publish revised and/or new versions
of the General Public License from time to time.  Such new versions will
be similar in spirit to the present version, but may differ in detail to
address new problems or concerns.

Each version is given a distinguishing version number.  If the Program
specifies a version number of this License which applies to it and "any
later version", you have the option of following the terms and conditions
either of that version or of any later version published by the Free
Software Foundation.  If the Program does not specify a version number of
this License, you may choose any version ever published by the Free Software
Foundation.

  10. If you wish to incorporate parts of the Program into other free
programs whose distribution conditions are different, write to the author
to ask for permission.  For software which is copyrighted by the Free
Software Foundation, write to the Free Software Foundation; we sometimes
make exceptions for this.  Our decision will be guided by the two goals
of preserving the free status of all derivatives of our free software and
of promoting the sharing and reuse of software generally.

			    NO WARRANTY

  11. BECAUSE THE PROGRAM IS LICENSED FREE OF CHARGE, THERE IS NO WARRANTY
FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW.  EXCEPT WHEN
OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES
PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED
OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.  THE ENTIRE RISK AS
TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU.  SHOULD THE
PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING,
REPAIR OR CORRECTION.

  12. IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING
WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MAY MODIFY AND/OR
REDISTRIBUTE THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES,
INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING
OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED
TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY
YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER
PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES.

		     END OF TERMS AND CONDITIONS

	    How to Apply These Terms to Your New Programs

  If you develop a new program, and you want it to be of the greatest
possible use to the public, the best way to achieve this is to make it
free software which everyone can redistribute and change under these terms.

  To do so, attach the following notices to the program.  It is safest
to attach them to the start of each source file to most effectively
convey the exclusion of warranty; and each file should have at least
the "copyright" line and a pointer to where the full notice is found.

    <one line to give the program's name and a brief idea of what it does.>
    Copyright (C) <year>  <name of author>

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

Also add information on how to contact you by electronic and paper mail.

If the program is interactive, make it output a short notice like this
when it starts in an interactive mode:

    Gnomovision version 69, Copyright (C) year name of author
    Gnomovision comes with ABSOLUTELY NO WARRANTY; for details type show w'.
    This is free software, and you are welcome to redistribute it
    under certain conditions; type show c' for details.

The hypothetical commands show w' and show c' should show the appropriate
parts of the General Public License.  Of course, the commands you use may
be called something other than show w' and show c'; they could even be
mouse-clicks or menu items--whatever suits your program.

You should also get your employer (if you work as a programmer) or your
school, if any, to sign a "copyright disclaimer" for the program, if
necessary.  Here is a sample; alter the names:

  Yoyodyne, Inc., hereby disclaims all copyright interest in the program
  Gnomovision' (which makes passes at compilers) written by James Hacker.

  <signature of Ty Coon>, 1 April 1989
  Ty Coon, President of Vice

This General Public License does not permit incorporating your program into
proprietary programs.  If your program is a subroutine library, you may
consider it more useful to permit linking proprietary applications with the
library.  If this is what you want to do, use the GNU Lesser General
Public License instead of this License.
This is an [inline link](/url "title"){.class #inline-link}.

This is a [reference link][refid].

This is an ![inline image](/img "title"){.class #inline-img}.

This is a ![reference image][refid].

[refid]: /path/to/something (Title) { .class #ref data-key=val }

Just a [URL](/url/).

[URL and title](/url/ "title").

[URL and title](/url/  "title preceded by two spaces").

[URL and title](/url/	"title preceded by a tab").

[URL and title](/url/ "title has spaces afterward"  ).

[URL wrapped in angle brackets](</url/>).

[URL w/ angle brackets + title](</url/> "Here's the title").

[Empty]().

[With parens in the URL](http://en.wikipedia.org/wiki/WIMP_(computing))

(With outer parens and [parens in url](/foo(bar)))


[With parens in the URL](/foo(bar) "and a title")

(With outer parens and [parens in url](/foo(bar) "and a title"))
Foo [bar] [1].

Foo [bar][1].

Foo [bar]
[1].

[1]: /url/  "Title"


With [embedded [brackets]] [b].


Indented [once][].

Indented [twice][].

Indented [thrice][].

Indented [four][] times.

 [once]: /url

  [twice]: /url

   [thrice]: /url

    [four]: /url


[b]: /url/

* * *

[this] [this] should work

So should [this][this].

And [this] [].

And [this][].

And [this].

But not [that] [].

Nor [that][].

Nor [that].

[Something in brackets like [this][] should work]

[Same with [this].]

In this case, [this](/somethingelse/) points to something else.

Backslashing should suppress \[this] and [this\].

[this]: foo


* * *

Here's one where the [link
breaks] across lines.

Here's another where the [link 
breaks] across lines, but with a line-ending space.


[link breaks]: /url/
This is the [simple case].

[simple case]: /simple



This one has a [line
break].

This one has a [line 
break] with a line-ending space.

[line break]: /foo


[this] [that] and the [other]

[this]: /this
[that]: /that
[other]: /other
Foo [bar][].

Foo [bar](/url/ "Title with "quotes" inside").


  [bar]: /url/ "Title with "quotes" inside"

Markdown: Basics
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a class="selected" title="Markdown Basics">Basics</a></li>
    <li><a href="/projects/markdown/syntax" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


Getting the Gist of Markdown's Formatting Syntax
------------------------------------------------

This page offers a brief overview of what it's like to use Markdown.
The [syntax page] [s] provides complete, detailed documentation for
every feature, but Markdown should be very easy to pick up simply by
looking at a few examples of it in action. The examples on this page
are written in a before/after style, showing example syntax and the
HTML output produced by Markdown.

It's also helpful to simply try Markdown out; the [Dingus] [d] is a
web application that allows you type your own Markdown-formatted text
and translate it to XHTML.

**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL] [src].

  [s]: /projects/markdown/syntax  "Markdown Syntax"
  [d]: /projects/markdown/dingus  "Markdown Dingus"
  [src]: /projects/markdown/basics.text


## Paragraphs, Headers, Blockquotes ##

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

Markdown offers two styles of headers: *Setext* and *atx*.
Setext-style headers for <h1> and <h2> are created by
"underlining" with equal signs (=) and hyphens (-), respectively.
To create an atx-style header, you put 1-6 hash marks (#) at the
beginning of the line -- the number of hashes equals the resulting
HTML header level.

Blockquotes are indicated using email-style '>' angle brackets.

Markdown:

    A First Level Header
    ====================
    
    A Second Level Header
    ---------------------

    Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.

    The quick brown fox jumped over the lazy
    dog's back.
    
    ### Header 3

    > This is a blockquote.
    > 
    > This is the second paragraph in the blockquote.
    >
    > ## This is an H2 in a blockquote


Output:

    <h1>A First Level Header</h1>
    
    <h2>A Second Level Header</h2>
    
    <p>Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.</p>
    
    <p>The quick brown fox jumped over the lazy
    dog's back.</p>
    
    <h3>Header 3</h3>
    
    <blockquote>
        <p>This is a blockquote.</p>
        
        <p>This is the second paragraph in the blockquote.</p>
        
        <h2>This is an H2 in a blockquote</h2>
    </blockquote>



### Phrase Emphasis ###

Markdown uses asterisks and underscores to indicate spans of emphasis.

Markdown:

    Some of these words *are emphasized*.
    Some of these words _are emphasized also_.
    
    Use two asterisks for **strong emphasis**.
    Or, if you prefer, __use two underscores instead__.

Output:

    <p>Some of these words <em>are emphasized</em>.
    Some of these words <em>are emphasized also</em>.</p>
    
    <p>Use two asterisks for <strong>strong emphasis</strong>.
    Or, if you prefer, <strong>use two underscores instead</strong>.</p>
   


## Lists ##

Unordered (bulleted) lists use asterisks, pluses, and hyphens (*,
+, and -) as list markers. These three markers are
interchangable; this:

    *   Candy.
    *   Gum.
    *   Booze.

this:

    +   Candy.
    +   Gum.
    +   Booze.

and this:

    -   Candy.
    -   Gum.
    -   Booze.

all produce the same output:

    <ul>
    <li>Candy.</li>
    <li>Gum.</li>
    <li>Booze.</li>
    </ul>

Ordered (numbered) lists use regular numbers, followed by periods, as
list markers:

    1.  Red
    2.  Green
    3.  Blue

Output:

    <ol>
    <li>Red</li>
    <li>Green</li>
    <li>Blue</li>
    </ol>

If you put blank lines between items, you'll get <p> tags for the
list item text. You can create multi-paragraph list items by indenting
the paragraphs by 4 spaces or 1 tab:

    *   A list item.
    
        With multiple paragraphs.

    *   Another item in the list.

Output:

    <ul>
    <li><p>A list item.</p>
    <p>With multiple paragraphs.</p></li>
    <li><p>Another item in the list.</p></li>
    </ul>
    


### Links ###

Markdown supports two styles for creating links: *inline* and
*reference*. With both styles, you use square brackets to delimit the
text you want to turn into a link.

Inline-style links use parentheses immediately after the link text.
For example:

    This is an [example link](http://example.com/).

Output:

    <p>This is an <a href="http://example.com/">
    example link</a>.</p>

Optionally, you may include a title attribute in the parentheses:

    This is an [example link](http://example.com/ "With a Title").

Output:

    <p>This is an <a href="http://example.com/" title="With a Title">
    example link</a>.</p>

Reference-style links allow you to refer to your links by names, which
you define elsewhere in your document:

    I get 10 times more traffic from [Google][1] than from
    [Yahoo][2] or [MSN][3].

    [1]: http://google.com/        "Google"
    [2]: http://search.yahoo.com/  "Yahoo Search"
    [3]: http://search.msn.com/    "MSN Search"

Output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from <a href="http://search.yahoo.com/"
    title="Yahoo Search">Yahoo</a> or <a href="http://search.msn.com/"
    title="MSN Search">MSN</a>.</p>

The title attribute is optional. Link names may contain letters,
numbers and spaces, but are *not* case sensitive:

    I start my morning with a cup of coffee and
    [The New York Times][NY Times].

    [ny times]: http://www.nytimes.com/

Output:

    <p>I start my morning with a cup of coffee and
    <a href="http://www.nytimes.com/">The New York Times</a>.</p>


### Images ###

Image syntax is very much like link syntax.

Inline (titles are optional):

    ![alt text](/path/to/img.jpg "Title")

Reference-style:

    ![alt text][id]

    [id]: /path/to/img.jpg "Title"

Both of the above examples produce the same output:

    <img src="/path/to/img.jpg" alt="alt text" title="Title" />



### Code ###

In a regular paragraph, you can create code span by wrapping text in
backtick quotes. Any ampersands (&) and angle brackets (< or
>) will automatically be translated into HTML entities. This makes
it easy to use Markdown to write about HTML example code:

    I strongly recommend against using any <blink> tags.

    I wish SmartyPants used named entities like &mdash;
    instead of decimal-encoded entites like &#8212;.

Output:

    <p>I strongly recommend against using any
    <code>&lt;blink&gt;</code> tags.</p>
    
    <p>I wish SmartyPants used named entities like
    <code>&amp;mdash;</code> instead of decimal-encoded
    entites like <code>&amp;#8212;</code>.</p>


To specify an entire block of pre-formatted code, indent every line of
the block by 4 spaces or 1 tab. Just like with code spans, &, <,
and > characters will be escaped automatically.

Markdown:

    If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:

        <blockquote>
            <p>For example.</p>
        </blockquote>

Output:

    <p>If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:</p>
    
    <pre><code>&lt;blockquote&gt;
        &lt;p&gt;For example.&lt;/p&gt;
    &lt;/blockquote&gt;
    </code></pre>
Markdown: Syntax
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a href="/projects/markdown/basics" title="Markdown Basics">Basics</a></li>
    <li><a class="selected" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


*   [Overview](#overview)
    *   [Philosophy](#philosophy)
    *   [Inline HTML](#html)
    *   [Automatic Escaping for Special Characters](#autoescape)
*   [Block Elements](#block)
    *   [Paragraphs and Line Breaks](#p)
    *   [Headers](#header)
    *   [Blockquotes](#blockquote)
    *   [Lists](#list)
    *   [Code Blocks](#precode)
    *   [Horizontal Rules](#hr)
*   [Span Elements](#span)
    *   [Links](#link)
    *   [Emphasis](#em)
    *   [Code](#code)
    *   [Images](#img)
*   [Miscellaneous](#misc)
    *   [Backslash Escapes](#backslash)
    *   [Automatic Links](#autolink)


**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL][src].

  [src]: /projects/markdown/syntax.text

* * *

<h2 id="overview">Overview</h2>

<h3 id="philosophy">Philosophy</h3>

Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

Readability, however, is emphasized above all else. A Markdown-formatted
document should be publishable as-is, as plain text, without looking
like it's been marked up with tags or formatting instructions. While
Markdown's syntax has been influenced by several existing text-to-HTML
filters -- including [Setext] [1], [atx] [2], [Textile] [3], [reStructuredText] [4],
[Grutatext] [5], and [EtText] [6] -- the single biggest source of
inspiration for Markdown's syntax is the format of plain text email.

  [1]: http://docutils.sourceforge.net/mirror/setext.html
  [2]: http://www.aaronsw.com/2002/atx/
  [3]: http://textism.com/tools/textile/
  [4]: http://docutils.sourceforge.net/rst.html
  [5]: http://www.triptico.com/software/grutatxt.html
  [6]: http://ettext.taint.org/doc/

To this end, Markdown's syntax is comprised entirely of punctuation
characters, which punctuation characters have been carefully chosen so
as to look like what they mean. E.g., asterisks around a word actually
look like \*emphasis\*. Markdown lists look like, well, lists. Even
blockquotes look like quoted passages of text, assuming you've ever
used email.



<h3 id="html">Inline HTML</h3>

Markdown's syntax is intended for one purpose: to be used as a
format for *writing* for the web.

Markdown is not a replacement for HTML, or even close to it. Its
syntax is very small, corresponding only to a very small subset of
HTML tags. The idea is *not* to create a syntax that makes it easier
to insert HTML tags. In my opinion, HTML tags are already easy to
insert. The idea for Markdown is to make it easy to read, write, and
edit prose. HTML is a *publishing* format; Markdown is a *writing*
format. Thus, Markdown's formatting syntax only addresses issues that
can be conveyed in plain text.

For any markup that is not covered by Markdown's syntax, you simply
use HTML itself. There's no need to preface it or delimit it to
indicate that you're switching from Markdown to HTML; you just use
the tags.

The only restrictions are that block-level HTML elements -- e.g. <div>,
<table>, <pre>, <p>, etc. -- must be separated from surrounding
content by blank lines, and the start and end tags of the block should
not be indented with tabs or spaces. Markdown is smart enough not
to add extra (unwanted) <p> tags around HTML block-level tags.

For example, to add an HTML table to a Markdown article:

    This is a regular paragraph.

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    This is another regular paragraph.

Note that Markdown formatting syntax is not processed within block-level
HTML tags. E.g., you can't use Markdown-style *emphasis* inside an
HTML block.

Span-level HTML tags -- e.g. <span>, <cite>, or <del> -- can be
used anywhere in a Markdown paragraph, list item, or header. If you
want, you can even use HTML tags instead of Markdown formatting; e.g. if
you'd prefer to use HTML <a> or <img> tags instead of Markdown's
link or image syntax, go right ahead.

Unlike block-level HTML tags, Markdown syntax *is* processed within
span-level tags.


<h3 id="autoescape">Automatic Escaping for Special Characters</h3>

In HTML, there are two characters that demand special treatment: <
and &. Left angle brackets are used to start tags; ampersands are
used to denote HTML entities. If you want to use them as literal
characters, you must escape them as entities, e.g. &lt;, and
&amp;.

Ampersands in particular are bedeviling for web writers. If you want to
write about 'AT&T', you need to write 'AT&amp;T'. You even need to
escape ampersands within URLs. Thus, if you want to link to:

    http://images.google.com/images?num=30&q=larry+bird

you need to encode the URL as:

    http://images.google.com/images?num=30&amp;q=larry+bird

in your anchor tag href attribute. Needless to say, this is easy to
forget, and is probably the single most common source of HTML validation
errors in otherwise well-marked-up web sites.

Markdown allows you to use these characters naturally, taking care of
all the necessary escaping for you. If you use an ampersand as part of
an HTML entity, it remains unchanged; otherwise it will be translated
into &amp;.

So, if you want to include a copyright symbol in your article, you can write:

    &copy;

and Markdown will leave it alone. But if you write:

    AT&T

Markdown will translate it to:

    AT&amp;T

Similarly, because Markdown supports [inline HTML](#html), if you use
angle brackets as delimiters for HTML tags, Markdown will treat them as
such. But if you write:

    4 < 5

Markdown will translate it to:

    4 &lt; 5

However, inside Markdown code spans and blocks, angle brackets and
ampersands are *always* encoded automatically. This makes it easy to use
Markdown to write about HTML code. (As opposed to raw HTML, which is a
terrible format for writing about HTML syntax, because every single <
and & in your example code needs to be escaped.)


* * *


<h2 id="block">Block Elements</h2>


<h3 id="p">Paragraphs and Line Breaks</h3>

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing but spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

The implication of the "one or more consecutive lines of text" rule is
that Markdown supports "hard-wrapped" text paragraphs. This differs
significantly from most other text-to-HTML formatters (including Movable
Type's "Convert Line Breaks" option) which translate every line break
character in a paragraph into a <br /> tag.

When you *do* want to insert a <br /> break tag using Markdown, you
end a line with two or more spaces, then type return.

Yes, this takes a tad more effort to create a <br />, but a simplistic
"every line break is a <br />" rule wouldn't work for Markdown.
Markdown's email-style [blockquoting][bq] and multi-paragraph [list items][l]
work best -- and look better -- when you format them with hard breaks.

  [bq]: #blockquote
  [l]:  #list



<h3 id="header">Headers</h3>

Markdown supports two styles of headers, [Setext] [1] and [atx] [2].

Setext-style headers are "underlined" using equal signs (for first-level
headers) and dashes (for second-level headers). For example:

    This is an H1
    =============

    This is an H2
    -------------

Any number of underlining ='s or -'s will work.

Atx-style headers use 1-6 hash characters at the start of the line,
corresponding to header levels 1-6. For example:

    # This is an H1

    ## This is an H2

    ###### This is an H6

Optionally, you may "close" atx-style headers. This is purely
cosmetic -- you can use this if you think it looks better. The
closing hashes don't even need to match the number of hashes
used to open the header. (The number of opening hashes
determines the header level.) :

    # This is an H1 #

    ## This is an H2 ##

    ### This is an H3 ######


<h3 id="blockquote">Blockquotes</h3>

Markdown uses email-style > characters for blockquoting. If you're
familiar with quoting passages of text in an email message, then you
know how to create a blockquote in Markdown. It looks best if you hard
wrap the text and put a > before every line:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    > 
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

Markdown allows you to be lazy and only put the > before the first
line of a hard-wrapped paragraph:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

Blockquotes can be nested (i.e. a blockquote-in-a-blockquote) by
adding additional levels of >:

    > This is the first level of quoting.
    >
    > > This is nested blockquote.
    >
    > Back to the first level.

Blockquotes can contain other Markdown elements, including headers, lists,
and code blocks:

	> ## This is a header.
	> 
	> 1.   This is the first list item.
	> 2.   This is the second list item.
	> 
	> Here's some example code:
	> 
	>     return shell_exec("echo $input | $markdown_script");

Any decent text editor should make email-style quoting easy. For
example, with BBEdit, you can make a selection and choose Increase
Quote Level from the Text menu.


<h3 id="list">Lists</h3>

Markdown supports ordered (numbered) and unordered (bulleted) lists.

Unordered lists use asterisks, pluses, and hyphens -- interchangably
-- as list markers:

    *   Red
    *   Green
    *   Blue

is equivalent to:

    +   Red
    +   Green
    +   Blue

and:

    -   Red
    -   Green
    -   Blue

Ordered lists use numbers followed by periods:

    1.  Bird
    2.  McHale
    3.  Parish

It's important to note that the actual numbers you use to mark the
list have no effect on the HTML output Markdown produces. The HTML
Markdown produces from the above list is:

    <ol>
    <li>Bird</li>
    <li>McHale</li>
    <li>Parish</li>
    </ol>

If you instead wrote the list in Markdown like this:

    1.  Bird
    1.  McHale
    1.  Parish

or even:

    3. Bird
    1. McHale
    8. Parish

you'd get the exact same HTML output. The point is, if you want to,
you can use ordinal numbers in your ordered Markdown lists, so that
the numbers in your source match the numbers in your published HTML.
But if you want to be lazy, you don't have to.

If you do use lazy list numbering, however, you should still start the
list with the number 1. At some point in the future, Markdown may support
starting ordered lists at an arbitrary number.

List markers typically start at the left margin, but may be indented by
up to three spaces. List markers must be followed by one or more spaces
or a tab.

To make lists look nice, you can wrap items with hanging indents:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
        Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
        viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
        Suspendisse id sem consectetuer libero luctus adipiscing.

But if you want to be lazy, you don't have to:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.

If list items are separated by blank lines, Markdown will wrap the
items in <p> tags in the HTML output. For example, this input:

    *   Bird
    *   Magic

will turn into:

    <ul>
    <li>Bird</li>
    <li>Magic</li>
    </ul>

But this:

    *   Bird

    *   Magic

will turn into:

    <ul>
    <li><p>Bird</p></li>
    <li><p>Magic</p></li>
    </ul>

List items may consist of multiple paragraphs. Each subsequent
paragraph in a list item must be intended by either 4 spaces
or one tab:

    1.  This is a list item with two paragraphs. Lorem ipsum dolor
        sit amet, consectetuer adipiscing elit. Aliquam hendrerit
        mi posuere lectus.

        Vestibulum enim wisi, viverra nec, fringilla in, laoreet
        vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
        sit amet velit.

    2.  Suspendisse id sem consectetuer libero luctus adipiscing.

It looks nice if you indent every line of the subsequent
paragraphs, but here again, Markdown will allow you to be
lazy:

    *   This is a list item with two paragraphs.

        This is the second paragraph in the list item. You're
    only required to indent the first line. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit.

    *   Another item in the same list.

To put a blockquote within a list item, the blockquote's >
delimiters need to be indented:

    *   A list item with a blockquote:

        > This is a blockquote
        > inside a list item.

To put a code block within a list item, the code block needs
to be indented *twice* -- 8 spaces or two tabs:

    *   A list item with a code block:

            <code goes here>


It's worth noting that it's possible to trigger an ordered list by
accident, by writing something like this:

    1986. What a great season.

In other words, a *number-period-space* sequence at the beginning of a
line. To avoid this, you can backslash-escape the period:

    1986\. What a great season.



<h3 id="precode">Code Blocks</h3>

Pre-formatted code blocks are used for writing about programming or
markup source code. Rather than forming normal paragraphs, the lines
of a code block are interpreted literally. Markdown wraps a code block
in both <pre> and <code> tags.

To produce a code block in Markdown, simply indent every line of the
block by at least 4 spaces or 1 tab. For example, given this input:

    This is a normal paragraph:

        This is a code block.

Markdown will generate:

    <p>This is a normal paragraph:</p>

    <pre><code>This is a code block.
    </code></pre>

One level of indentation -- 4 spaces or 1 tab -- is removed from each
line of the code block. For example, this:

    Here is an example of AppleScript:

        tell application "Foo"
            beep
        end tell

will turn into:

    <p>Here is an example of AppleScript:</p>

    <pre><code>tell application "Foo"
        beep
    end tell
    </code></pre>

A code block continues until it reaches a line that is not indented
(or the end of the article).

Within a code block, ampersands (&) and angle brackets (< and >)
are automatically converted into HTML entities. This makes it very
easy to include example HTML source code using Markdown -- just paste
it and indent it, and Markdown will handle the hassle of encoding the
ampersands and angle brackets. For example, this:

        <div class="footer">
            &copy; 2004 Foo Corporation
        </div>

will turn into:

    <pre><code>&lt;div class="footer"&gt;
        &amp;copy; 2004 Foo Corporation
    &lt;/div&gt;
    </code></pre>

Regular Markdown syntax is not processed within code blocks. E.g.,
asterisks are just literal asterisks within a code block. This means
it's also easy to use Markdown to write about Markdown's own syntax.



<h3 id="hr">Horizontal Rules</h3>

You can produce a horizontal rule tag (<hr />) by placing three or
more hyphens, asterisks, or underscores on a line by themselves. If you
wish, you may use spaces between the hyphens or asterisks. Each of the
following lines will produce a horizontal rule:

    * * *

    ***

    *****
	
    - - -

    ---------------------------------------

	_ _ _


* * *

<h2 id="span">Span Elements</h2>

<h3 id="link">Links</h3>

Markdown supports two style of links: *inline* and *reference*.

In both styles, the link text is delimited by [square brackets].

To create an inline link, use a set of regular parentheses immediately
after the link text's closing square bracket. Inside the parentheses,
put the URL where you want the link to point, along with an *optional*
title for the link, surrounded in quotes. For example:

    This is [an example](http://example.com/ "Title") inline link.

    [This link](http://example.net/) has no title attribute.

Will produce:

    <p>This is <a href="http://example.com/" title="Title">
    an example</a> inline link.</p>

    <p><a href="http://example.net/">This link</a> has no
    title attribute.</p>

If you're referring to a local resource on the same server, you can
use relative paths:

    See my [About](/about/) page for details.

Reference-style links use a second set of square brackets, inside
which you place a label of your choosing to identify the link:

    This is [an example][id] reference-style link.

You can optionally use a space to separate the sets of brackets:

    This is [an example] [id] reference-style link.

Then, anywhere in the document, you define your link label like this,
on a line by itself:

    [id]: http://example.com/  "Optional Title Here"

That is:

*   Square brackets containing the link identifier (optionally
    indented from the left margin using up to three spaces);
*   followed by a colon;
*   followed by one or more spaces (or tabs);
*   followed by the URL for the link;
*   optionally followed by a title attribute for the link, enclosed
    in double or single quotes.

The link URL may, optionally, be surrounded by angle brackets:

    [id]: <http://example.com/>  "Optional Title Here"

You can put the title attribute on the next line and use extra spaces
or tabs for padding, which tends to look better with longer URLs:

    [id]: http://example.com/longish/path/to/resource/here
        "Optional Title Here"

Link definitions are only used for creating links during Markdown
processing, and are stripped from your document in the HTML output.

Link definition names may constist of letters, numbers, spaces, and punctuation -- but they are *not* case sensitive. E.g. these two links:

	[link text][a]
	[link text][A]

are equivalent.

The *implicit link name* shortcut allows you to omit the name of the
link, in which case the link text itself is used as the name.
Just use an empty set of square brackets -- e.g., to link the word
"Google" to the google.com web site, you could simply write:

	[Google][]

And then define the link:

	[Google]: http://google.com/

Because link names may contain spaces, this shortcut even works for
multiple words in the link text:

	Visit [Daring Fireball][] for more information.

And then define the link:
	
	[Daring Fireball]: http://daringfireball.net/

Link definitions can be placed anywhere in your Markdown document. I
tend to put them immediately after each paragraph in which they're
used, but if you want, you can put them all at the end of your
document, sort of like footnotes.

Here's an example of reference links in action:

    I get 10 times more traffic from [Google] [1] than from
    [Yahoo] [2] or [MSN] [3].

      [1]: http://google.com/        "Google"
      [2]: http://search.yahoo.com/  "Yahoo Search"
      [3]: http://search.msn.com/    "MSN Search"

Using the implicit link name shortcut, you could instead write:

    I get 10 times more traffic from [Google][] than from
    [Yahoo][] or [MSN][].

      [google]: http://google.com/        "Google"
      [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
      [msn]:    http://search.msn.com/    "MSN Search"

Both of the above examples will produce the following HTML output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from
    <a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a>
    or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p>

For comparison, here is the same paragraph written using
Markdown's inline link style:

    I get 10 times more traffic from [Google](http://google.com/ "Google")
    than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or
    [MSN](http://search.msn.com/ "MSN Search").

The point of reference-style links is not that they're easier to
write. The point is that with reference-style links, your document
source is vastly more readable. Compare the above examples: using
reference-style links, the paragraph itself is only 81 characters
long; with inline-style links, it's 176 characters; and as raw HTML,
it's 234 characters. In the raw HTML, there's more markup than there
is text.

With Markdown's reference-style links, a source document much more
closely resembles the final output, as rendered in a browser. By
allowing you to move the markup-related metadata out of the paragraph,
you can add links without interrupting the narrative flow of your
prose.


<h3 id="em">Emphasis</h3>

Markdown treats asterisks (*) and underscores (_) as indicators of
emphasis. Text wrapped with one * or _ will be wrapped with an
HTML <em> tag; double *'s or _'s will be wrapped with an HTML
<strong> tag. E.g., this input:

    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__

will produce:

    <em>single asterisks</em>

    <em>single underscores</em>

    <strong>double asterisks</strong>

    <strong>double underscores</strong>

You can use whichever style you prefer; the lone restriction is that
the same character must be used to open and close an emphasis span.

Emphasis can be used in the middle of a word:

    un*fucking*believable

But if you surround an * or _ with spaces, it'll be treated as a
literal asterisk or underscore.

To produce a literal asterisk or underscore at a position where it
would otherwise be used as an emphasis delimiter, you can backslash
escape it:

    \*this text is surrounded by literal asterisks\*



<h3 id="code">Code</h3>

To indicate a span of code, wrap it with backtick quotes (  ).
Unlike a pre-formatted code block, a code span indicates code within a
normal paragraph. For example:

    Use the printf() function.

will produce:

    <p>Use the <code>printf()</code> function.</p>

To include a literal backtick character within a code span, you can use
multiple backticks as the opening and closing delimiters:

     There is a literal backtick () here.

which will produce this:

    <p><code>There is a literal backtick () here.</code></p>

The backtick delimiters surrounding a code span may include spaces --
one after the opening, one before the closing. This allows you to place
literal backtick characters at the beginning or end of a code span:

	A single backtick in a code span:     
	
	A backtick-delimited string in a code span:   foo  

will produce:

	<p>A single backtick in a code span: <code></code></p>
	
	<p>A backtick-delimited string in a code span: <code>foo</code></p>

With a code span, ampersands and angle brackets are encoded as HTML
entities automatically, which makes it easy to include example HTML
tags. Markdown will turn this:

    Please don't use any <blink> tags.

into:

    <p>Please don't use any <code>&lt;blink&gt;</code> tags.</p>

You can write this:

    &#8212; is the decimal-encoded equivalent of &mdash;.

to produce:

    <p><code>&amp;#8212;</code> is the decimal-encoded
    equivalent of <code>&amp;mdash;</code>.</p>



<h3 id="img">Images</h3>

Admittedly, it's fairly difficult to devise a "natural" syntax for
placing images into a plain text document format.

Markdown uses an image syntax that is intended to resemble the syntax
for links, allowing for two styles: *inline* and *reference*.

Inline image syntax looks like this:

    ![Alt text](/path/to/img.jpg)

    ![Alt text](/path/to/img.jpg "Optional title")

That is:

*   An exclamation mark: !;
*   followed by a set of square brackets, containing the alt
    attribute text for the image;
*   followed by a set of parentheses, containing the URL or path to
    the image, and an optional title attribute enclosed in double
    or single quotes.

Reference-style image syntax looks like this:

    ![Alt text][id]

Where "id" is the name of a defined image reference. Image references
are defined using syntax identical to link references:

    [id]: url/to/image  "Optional title attribute"

As of this writing, Markdown has no syntax for specifying the
dimensions of an image; if this is important to you, you can simply
use regular HTML <img> tags.


* * *


<h2 id="misc">Miscellaneous</h2>

<h3 id="autolink">Automatic Links</h3>

Markdown supports a shortcut style for creating "automatic" links for URLs and email addresses: simply surround the URL or email address with angle brackets. What this means is that if you want to show the actual text of a URL or email address, and also have it be a clickable link, you can do this:

    <http://example.com/>
    
Markdown will turn this into:

    <a href="http://example.com/">http://example.com/</a>

Automatic links for email addresses work similarly, except that
Markdown will also perform a bit of randomized decimal and hex
entity-encoding to help obscure your address from address-harvesting
spambots. For example, Markdown will turn this:

    <address@example.com>

into something like this:

    <a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
    &#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
    &#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
    &#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>

which will render in a browser as a clickable link to "address@example.com".

(This sort of entity-encoding trick will indeed fool many, if not
most, address-harvesting bots, but it definitely won't fool all of
them. It's better than nothing, but an address published in this way
will probably eventually start receiving spam.)



<h3 id="backslash">Backslash Escapes</h3>

Markdown allows you to use backslash escapes to generate literal
characters which would otherwise have special meaning in Markdown's
formatting syntax. For example, if you wanted to surround a word with
literal asterisks (instead of an HTML <em> tag), you can backslashes
before the asterisks, like this:

    \*literal asterisks\*

Markdown provides backslash escapes for the following characters:

    \   backslash
       backtick
    *   asterisk
    _   underscore
    {}  curly braces
    []  square brackets
    ()  parentheses
    #   hash mark
	+	plus sign
	-	minus sign (hyphen)
    .   dot
    !   exclamation mark

# Character Escapes

The MD5 value for + is "26b17225b626fb9238849fd60eabdf60".

# HTML Blocks

<p>test</p>

The MD5 value for <p>test</p> is:

6205333b793f34273d75379350b36826* test
+ test
- test

1. test
2. test

* test
+ test
- test

1. test
2. test
> foo
>
> > bar
>
> foo
Valid nesting:

**[Link](url)**

[**Link**](url)

**[**Link**](url)**

Invalid nesting:

[[Link](url)](url)## Unordered

Asterisks tight:

*	asterisk 1
*	asterisk 2
*	asterisk 3


Asterisks loose:

*	asterisk 1

*	asterisk 2

*	asterisk 3

* * *

Pluses tight:

+	Plus 1
+	Plus 2
+	Plus 3


Pluses loose:

+	Plus 1

+	Plus 2

+	Plus 3

* * *


Minuses tight:

-	Minus 1
-	Minus 2
-	Minus 3


Minuses loose:

-	Minus 1

-	Minus 2

-	Minus 3


## Ordered

Tight:

1.	First
2.	Second
3.	Third

and:

1. One
2. Two
3. Three


Loose using tabs:

1.	First

2.	Second

3.	Third

and using spaces:

1. One

2. Two

3. Three

Multiple paragraphs:

1.	Item 1, graf one.

	Item 2. graf two. The quick brown fox jumped over the lazy dog's
	back.
	
2.	Item 2.

3.	Item 3.



## Nested

*	Tab
	*	Tab
		*	Tab

Here's another:

1. First
2. Second:
	* Fee
	* Fie
	* Foe
3. Third

Same thing but with paragraphs:

1. First

2. Second:
	* Fee
	* Fie
	* Foe

3. Third


This was an error in Markdown 1.0.1:

*	this

	*	sub

	that
[Inline link 1 with parens](/url\(test\) "title").

[Inline link 2 with parens](</url\(test\)> "title").

[Inline link 3 with non-escaped parens](/url(test) "title").

[Inline link 4 with non-escaped parens](</url(test)> "title").

[Reference link 1 with parens][1].

[Reference link 2 with parens][2].

  [1]: /url(test) "title"
  [2]: </url(test)> "title"
This tests for a bug where quotes escaped by PHP when using 
preg_replace with the /e modifier must be correctly unescaped
(hence the _UnslashQuotes function found only in PHP Markdown).



Headers below should appear exactly as they are typed (no backslash
added or removed).

Header "quoted\" again \\""
===========================

Header "quoted\" again \\""
---------------------------

### Header "quoted\" again \\"" ###



Test with tabs for _Detab:

	Code	'block'	with	some	"tabs"	and	"quotes"
[Test](/"style="color:red)
[Test](/'style='color:red)

![](/"style="border-color:red;border-size:1px;border-style:solid)
![](/'style='border-color:red;border-size:1px;border-style:solid)
***This is strong and em.***

So is ***this*** word.

___This is strong and em.___

So is ___this___ word.
# Simple tables

Header 1  | Header 2
--------- | ---------
Cell 1    | Cell 2
Cell 3    | Cell 4

With leading pipes:

| Header 1  | Header 2
| --------- | ---------
| Cell 1    | Cell 2
| Cell 3    | Cell 4

With tailing pipes:

Header 1  | Header 2  |
--------- | --------- |
Cell 1    | Cell 2    |
Cell 3    | Cell 4    |

With leading and tailing pipes:

| Header 1  | Header 2  |
| --------- | --------- |
| Cell 1    | Cell 2    |
| Cell 3    | Cell 4    |

* * *

# One-column one-row table

With leading pipes:

| Header
| -------
| Cell

With tailing pipes:

Header  |
------- |
Cell    |

With leading and tailing pipes:

| Header  |
| ------- |
| Cell    |

* * *

Table alignement:

| Default   | Right     |  Center   |     Left  |
| --------- |:--------- |:---------:| ---------:|
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

Table alignement (alternate spacing):

| Default   | Right     |  Center   |     Left  |
| --------- | :-------- | :-------: | --------: |
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

* * * 

# Empty cells

| Header 1  | Header 2  |
| --------- | --------- |
| A         | B         |
| C         |           |

Header 1  | Header 2
--------- | ---------
A         | B
          | D

* * *

# Missing tailing pipe

Header 1  | Header 2  
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- 
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      

* * *

# Too many pipes in rows

| Header 1  | Header 2  |
| --------- 
| Cell      | Cell      | Extra cell? |
| Cell      | Cell      | Extra cell? |

+	this is a list item
	indented with tabs

+   this is a list item
    indented with spaces

Code:

	this code block is indented by one tab

And:

		this code block is indented by two tabs

And:

	+	this is an example list item
		indented with tabs
	
	+   this is an example list item
	    indented with spaces
> A list within a blockquote:
> 
> *	asterisk 1
> *	asterisk 2
> *	asterisk 3
Paragraph and no space:
* ciao

Paragraph and 1 space:
 * ciao

Paragraph and 3 spaces:
  * ciao

Paragraph and 4 spaces:
   * ciao

Paragraph before header:
#Header

Paragraph before blockquote:
>Some quote.
 .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>


As above: checking for bad interractions with the HTML block parser:

 html
<div>


Some *markdown* formatting.

 html
</div>


Some *markdown*


<div>
    <html>



function test();


<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">

<html>
    <title>

</div>

Two code blocks with no blank line between them:


<div>


<div>


Testing *confusion* with markers in the middle:


<div></div>


Testing mixing with title code blocks


<p>
 
<p>

 
<p>

<p>
 

<Fenced>


Code block starting and ending with empty lines:



<Fenced>




Indented code block containing fenced code block sample:

	
	<Fenced>
	

Fenced code block with indented code block sample:


Some text

	Indented code block sample code


Fenced code block with long markers:


Fenced


Fenced code block with fenced code block markers of different length in it:


In code block

Still in code block

Still in code block


Fenced code block with Markdown header and horizontal rule:


#test
---


Fenced code block with link definitions, footnote definition and 
abbreviation definitions:


[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language


* In a list item with smalish indent:

  
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
  
  
With HTML content.
  

<b>bold</b>


Bug with block level elements in this case:

  <div>
  </div>


Indented code block of a fenced code block:

    
	haha!
	

With class:
  
html
<b>bold</b>

  
 html
<b>bold</b>

  
.html
<b>bold</b>

  
 .html
<b>bold</b>


With extra attribute block:

{.html}
<b>bold</b>

  
 {.html #codeid}
<b>bold</b>


 .html{.bold}
<div>

  
 .html {#codeid}
</div>
First line. <br/>
Second line.

This is a first paragraph,
on multiple lines.
     
This is a second paragraph.
There are spaces in between the two.This is a first paragraph,
on multiple lines.

This is a second paragraph
which has multiple lines too.A first paragraph.



A second paragraph after 3 CR (carriage return).This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
     
A few spaces and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
	
1 tab to separate them and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.

A new long long long long long long long long long long long long long long long long paragraph on 1 line.An ampersand & in the text flow is escaped as an html entity.There is an [ampersand](http://validator.w3.org/check?uri=http://www.w3.org/&verbose=1) in the URI.This is \*an asterisk which should stay as is.This is * an asterisk which should stay as is.\\   backslash
\   backtick
\*   asterisk
\_   underscore
\{\}  curly braces
\[\]  square brackets
\(\)  parentheses
\#   hash mark
\+   plus sign
\-   minus sign (hyphen)
\.   dot
\!   exclamation mark> # heading level 1
> 
> paragraph>A blockquote with a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.

>and a second very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.>This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a blockquote.> A blockquote
> on multiple lines
> like this.>A blockquote 
>on multiple lines 
>like this. >A blockquote
>on multiple lines
>like this.
>
>But it has
>two paragraphs.>A blockquote
>on multiple lines
>like this> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.
> This is the first level of quoting.
>
> > This is nested blockquote.> This is the first level of quoting.
> > This is nested blockquote.
> Back to the first level.
> This is the first level of quoting.
> > This is nested blockquote.
	10 PRINT HELLO INFINITE
	20 GOTO 10    10 PRINT < > &
    20 GOTO 10    10 PRINT HELLO INFINITE
    20 GOTO 10# Contributing to Mardown Test Suite

1. [Getting Involved](#getting-involved)
2. [Discussion](#discussion)
3. [How To Report an Issue](#how-to-report-an-issue)
4. [Editing Markdown Specification](#editing-markdown-specification)
5. [Test Suite Guidelines](#test-suite-guidelines)
6. [Pull Request Guidelines](#pull-request-guidelines)

## Getting Involved

There are a number of ways to get involved with the development of the Markdown Test Suite. If you are a first time contributor to an open source project, you can still add value to this project. You may identify grammar issues, write prose, examples or documentation for the project. You may flag some errors and open new issues.

Read all bits of this document and that will guide you on how to participate.

## Discussion

### Mailing List

The Markdown Test Suite has been started a little bit after the start of the [Markdown Community Group](http://www.w3.org/community/markdown/). You may want to discuss about Markdown and this project on the [group mailing-list](http://lists.w3.org/Archives/Public/public-markdown/).

## How to Report an Issue

Don't be afraid to add details to your issue. The more context you give, the better for people participating to the project. Make a short summary, add a description with the context and give links to places which will help to understand.

## Editing Markdown Specification

There is much needed work on the [Markdown Specification](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html). It doesn't require strong competences in coding. Be systematic in the markup and follow the way it is already organized. Each time you added a new atomic section, create a commit for this specific part.

## Test Suite Guidelines

When proposing new tests, make sure they do not already exist in the current test suite. You will notice that there is a separate section dedicated to the specific extensions that some markdown generators have created. Keep them separate. We want to keep the core clean and close to the original specification of Markdown.

If you are not sure, create an issue.

### Markdown Extensions

Markdown extension tests are accepted. Use the following rules:

- place all extension tests under the test/extensions/ENGINE directory with filename equal to the feature name
- for each ENGINE and add a README.markdown under the engine directory with a link to its specification

where ENGINE is either of:

- a command line utility. E.g. pandoc, kramdown.
- a programming API. E.g. Redcarpet::Markdown.new().
- a programmatically accessible web service. E.g.: GFM via the GitHub API.
- a non programmatically accessible web service. E.g.: Stack Overflow flavored markdown.

To avoid test duplication for common features, use the following rules:

- if file tests/extensions/ENGINE/FEATURE.md is empty or not present, use tests/extensions/FEATURE.md instead
- if file tests/extensions/ENGINE/FEATURE.out not present, use tests/extensions/FEATURE.out instead
- for a given ENGINE, only features which have either a .md or a .out are implemented by that engine.
- in case of different outputs for a single feature input, keep directly under extensions/ only the output case that happens across the most engines

**version**

Only the latest stable version of each ENGINE is considered.

**options**

The IO behavior tested is for engine defaults, without any options (command line options, extra JSON parameters, etc.) passed to the engine.

**external state**

Tests that use external state not present in the markdown input shall not be included in this test suite.

For example, what GFM @user user tags render to also depends on the state of GitHub's databases (only render to a link if user exists), not only on the input markdown.

#### Examples

GFM and the "fenced code block" use the following file structure:

    tests/extensions/gfm/README.markdown
    tests/extensions/gfm/fenced-code-block.md
    tests/extensions/gfm/fenced-code-block.out

where README.markdown contains:

    https://help.github.com/articles/github-flavored-markdown

To avoid duplication with other engines, if the input / output (normalized to DOM) is the same across multiple engines use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

If the input is the same, and outputs are DOM different, but represent the same idea (e.g. both represent computer code) use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/gfm/fenced-code-block.out
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

#### New Extensions

Tests are modular, and if you want to test a new engine for your project, that should be easy to do.

If you feel that the new engine is reasonably popular, please send a pull request adding it.

## Commits and Pull Requests

* Keep your commits clean and commented
* Do not mix in one commit different things. Keep modifications related.
* Do not mix everything in one giant pull request. Create separate pull requests for different topic. That will help to have a more meaningful debate about the pull requests and will help to review the code.
* If it relates to a specific issue, add the number of the issue in the commit message.

Thanks for Contributing
as*te*risks*single asterisks*_single underscores_HTML entities are written using ampersand notation: &copy;These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

This is an H1
=============# This is an H1 # # This is an H1# this is an h1 with two trailing spaces  
A new paragraph.# This is an H1This is an H2
-------------## This is an H2 #### This is an H2### This is an H3 ###### This is an H3#### This is an H4 ######## This is an H4##### This is an H5 ########## This is an H5###### This is an H6  ############ This is an H6- - ----***___-------![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 for everyone"![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 logo for everyone")![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png)We love <code> and & for everything We love code for everything We love code for everything The MIT License (MIT)

Copyright (c) 2013 Karl Dubost

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
A first sentence  
and a line break.A first sentence     
and a line break.This is an automatic link <http://www.w3.org/>[W3C](http://www.w3.org/ "Discover w3c")[W3C](http://www.w3.org/)[World Wide Web Consortium][w3c]

[w3c]: <http://www.w3.org/>[World Wide Web Consortium][]

[World Wide Web Consortium]: http://www.w3.org/[w3c][]

[w3c]: http://www.w3.org/[World Wide Web Consortium] [w3c]

[w3c]: http://www.w3.org/[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/
   "Discover W3C"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ (Discover w3c)[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ 'Discover w3c'[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ "Discover w3c"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/*   a list containing a blockquote

    > this the blockquote in the list* a

        b
*   a list containing a block of code

	    10 PRINT HELLO INFINITE
	    20 GOTO 10*   This is a list item with two paragraphs. Lorem ipsum dolor
	sit amet, consectetuer adipiscing elit. Aliquam hendrerit
	mi posuere lectus.

	Vestibulum enim wisi, viverra nec, fringilla in, laoreet
	vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
	sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.*   This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.1\. ordered list escape1. 1

    - inner par list

2. 2
1. list item 1
8. list item 2
1. list item 31. list item 1
2. list item 2
3. list item 3This is a paragraph
on multiple lines
with hard return.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line. This is a paragraph with a trailing and leading space. This is a paragraph with 1 trailing tab.	  This is a paragraph with 2 leading spaces.   This is a paragraph with 3 leading spaces. This is a paragraph with 1 leading space.This is a paragraph with a trailing space. # Colophon - October 1st, 2014

This project was initiated to provide a test suite for Markdown markup, and eventually create a specification from this test results. A part of of the community has started a new endeavor which seems to get traction as [CommonMark](https://github.com/jgm/stmd). **We are then closing this project** and encourage you to contribute to CommonMark. 

The most interesting part of this project would not have been possible without the dedication of [Ciro Santilli](https://github.com/cirosantilli) @cirosantilli. So big applause and thank you to him.


The rest is kept around for archives and references.

# Markdown Test Suite

Inspired by questions on [W3C Markdown Community Group](http://www.w3.org/community/markdown).

Pull Requests are welcome. See the [CONTRIBUTING Guidelines](https://github.com/karlcow/markdown-testsuite/blob/master/CONTRIBUTING.md)

## Design goals

- Comprehensive.
- Small modularized tests.
- Easy to run tests using any programming language. In particular, data representations must have an implementation on all major languages.
- Develop a consensus based markdown specification at [markdown-spec.html](markdown-spec.html). Visualize it [here](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html).

## Test Scripts

Markdown Test Suite already includes tests for many important markdown engines.

To see what the scripts do run:

    ./cat-all.py -h
    ./run-tests.py -h

To configure the scripts do:

	cp config_local.py.example config_local.py

and edit config_local.py. It is already gitignored.

A Vagrantfile is provided with a provision script that installs all installable engines.

Sample output from run-tests.py:

    blackfriday   |......FFF..............FF...F....................................F....................................|   0.93s  102    7   6%
	gfm           |FF.....F.....F...FFFF..F....F........................FFFF...FF...............FF...F.......F...........| 262.88s  102   20  19%
    hoedown       |..............................F.................................................F.....................|   0.36s  102    2   1%
	kramdown      |......FFF.....FF.......FF.......FF.FFFFFFFFFFFFF.......................F..............................|  30.69s  102   23  22%
    lunamark      |FFFFFF.F.FFFFFFFFFFFF.F.....FFFF..FF............FFFFF..FFFFFFFFFF..............F...FFFFFFFFFFF........|   1.58s  103   53  51%
    markdown_pl   |.....................FFFF...............................F...............F.............................|   2.56s  102    6   5%
    markdown2     |......................................................................................................|   5.39s  103    0   0%
    marked        |..............F.................FFFFFFFFFFFFFFFF......................F.F.............................|   6.22s  102   19  18%
    maruku        |......FFF......F.......F.FFF...............................................FF.........................|  37.02s  102   10   9%
    md2html       |.........................FFF...F............................................FF........................|   7.42s  102    6   5%
    multimarkdown |......FFF....FF...F............FFF.FFFFFFFFFFFFF.....FFFF.........F...................................|   0.58s  102   27  26%
    pandoc        |FF...........F.F.FFFF..FFFFF....FF.FFFFFFFFFFFFF.....FFFF.....FF............FFF.FFF..................F|   1.11s  102   41  40%
    peg_markdown  |.................................................................F....................................|   0.46s  102    1   0%
    rdiscount     |.......F.........................................................F....................................|  25.19s  102    3   2%
    redcarpet     |......................................................................................................|  21.49s  102    0   0%
    showdown      |.......................................................................F..............................|   6.85s  102    1   0%

	Extensions:

    blackfriday   |F..|  0.04s    3    1  33%
	gfm           |F.|   2.37s    2    1  50%
    hoedown       |.|    0.00s    1    0   0%
    lunamark      |F.F|  0.05s    3    2  66%
    kramdown      |..|   0.62s    2    0   0%
    markdown_pl   ||     0.00s    0    0   0%
    markdown2     |F.|   0.14s    2    1  50%
    marked        |F.|   0.13s    2    1  50%
    maruku        |F..|  1.06s    3    1  33%
    md2html       |F.|   0.14s    2    0   0%
    multimarkdown |F.|   0.01s    2    1  50%
    pandoc        |F.|   0.02s    2    1  50%
    peg_markdown  |...|  0.02s    3    0   0%
    rdiscount     |F..|   0.74s    3    1  33%
    redcarpet     |..|   0.42s    2    0   0%
    showdown      |F..|  0.20s    3    1  33%

Where F indicates a failing test.

## Other Noticeable Test Suites

We haven't been the first test suite effort. Some projects have maintained their own test suite for a long time. Hopefully we can reach a state where people agree on the terms of what should be a good test suite for all developers.

- [Original test suite](http://daringfireball.net/projects/downloads/MarkdownTest_1.0.zip)
- [PHP markdown test suite:](https://github.com/michelf/mdtest/tree/master/Markdown.mdtest)
- [Markdown-js test suite](https://github.com/evilstreak/markdown-js/tree/master/test/features)
- [Python markdown 2 test suite](https://github.com/trentm/python-markdown2/tree/master/test/tm-cases)
- [multimarkdown test suite](https://github.com/fletcher/MMD-Test-Suite)
- [John MacFarlane's Standard Markdown spec](https://github.com/jgm/stmd)

In addition we should note the [wonderful work](http://johnmacfarlane.net/babelmark2/) made by John Mac Farlane. The Web service output the differences in between the different markdown implementations. It helps a lot when searching on the most common output.
as**te**risks**double asterisks**__double underscores__* list item 1
* list item 2
* list item 3
- list item 1
- list item 2
- list item 3 * list item 1
 * list item 2
 * list item 3  * list item 1
  * list item 2
  * list item 3   * list item 1
   * list item 2
   * list item 3+ list item 1
+ list item 2
+ list item 3* list item in paragraph

* another list item in paragraph*   This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a list.
*   and yet another long long long long long long long long long long long long long long long long long long long long long long line.*   This is a list item
    with the content on
    multiline and indented.
*   And this another list item
    with the same principle.€Some text about HTML, SGML and HTML4.

Let's talk about the U.S.A., (É.U. or É.-U. d'A. in French).

*[HTML4]: Hyper Text Markup Language version 4
*[HTML]: Hyper Text Markup Language
*[SGML]: Standard Generalized Markup Language
*[U.S.A.]: United States of America
*[É.U.] : États-Unis d'Amérique
*[É.-U. d'A.] : États-Unis d'Amérique

And here we have a CD, some CDs, and some other CD's.

*[CD]: Compact Disk

Let's transfert documents through TCP/IP, using TCP packets.

*[IP]: Internet Protocol
*[TCP]: Transmission Control Protocol

 ---

Bienvenue sur [CMS](http://www.bidulecms.com "Bidule CMS").

*[CMS]: Content Management System

 ---

ATCCE

*[ATCCE]: Abbreviation "Testing" Correct 'Character' < Escapes >* one
* two

1. three
2. four

* one
* two
1. three
2. fourAT&T has an ampersand in their name.

AT&amp;T is another way to write it.

This & that.

4 < 5.

6 > 5.

Here's a [link] [1] with an ampersand in the URL.

Here's a link with an amersand in the link text: [AT&T] [2].

Here's an inline [link](/script?foo=1&bar=2).

Here's an inline [link](</script?foo=1&bar=2>).


[1]: http://example.com/?foo=1&bar=2
[2]: http://att.com/  "AT&T"Link: <http://example.com/>.

With an ampersand: <http://example.com/?foo=1&bar=2>

* In a list?
* <http://example.com/>
* It should.

> Blockquoted: <http://example.com/>

Auto-links should not occur here: <http://example.com/>

	or here: <http://example.com/>These should all get escaped:

Backslash: \\

Backtick: \

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-



These should not, because they occur within a code block:

	Backslash: \\

	Backtick: \

	Asterisk: \*

	Underscore: \_

	Left brace: \{

	Right brace: \}

	Left bracket: \[

	Right bracket: \]

	Left paren: \(

	Right paren: \)

	Greater-than: \>

	Hash: \#

	Period: \.

	Bang: \!

	Plus: \+

	Minus: \-


Nor should these, which occur in code spans:

Backslash: \\

Backtick:   \  

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-


These should get escaped, even though they're matching pairs for
other Markdown constructs:

\*asterisks\*

\_underscores\_

\backticks\

This is a code span with a literal backslash-backtick sequence:   \  

This is a tag with unescaped backticks <span attr='ticks'>bar</span>.

This is a tag with backslashes <span attr='\\backslashes\\'>bar</span>.
  .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>
 

As above: checking for bad interractions with the HTML block parser:

  html
<div>
 

Some *markdown* formatting.

  html
</div>
 

Some *markdown*

 
<div>
    <html>
 

 
function test();
 

<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">
 
<html>
    <title>
 
</div>

Two code blocks with no blank line between them:

 
<div>
 
 
<div>
 

Testing *confusion* with code spans at the HTML block parser:

 
<div></div>
 

Testing mixing with title code blocks

 
<p>

<p>
 

<p>
 
<p>

 
<Fenced>
 

Code block starting and ending with empty lines:
 


<Fenced>


 

Indented code block containing fenced code block sample:

	 
	<Fenced>
	 

Fenced code block with indented code block sample:

 
Some text

	Indented code block sample code
 

Fenced code block with long markers:

 
Fenced
 

Fenced code block with fenced code block markers of different length in it:

 
In code block
 
Still in code block
 
Still in code block
 

Fenced code block with Markdown header and horizontal rule:

 
#test
---
 

Fenced code block with link definitions, footnote definition and
abbreviation definitions:

 
[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language
 

* In a list item with smalish indent:

   
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
   

With HTML content.

 
<b>bold</b>
 

Bug with block level elements in this case:
 
  <div>
  </div>
 

Indented code block of a fenced code block:

     
	haha!
	 

With class:

 html
<b>bold</b>
 

  html
<b>bold</b>
 

 .html
<b>bold</b>
 

  .html
<b>bold</b>
 

With extra attribute block:

 {.html}
<b>bold</b>
 

  {.html #codeid}
<b>bold</b>
 

  .html{.bold}
<div>
 
  
  .html {#codeid}
</div>
 > Example:
> 
>     sub status {
>         print "working";
>     }
> 
> Or:
> 
>     sub status {
>         return "working";
>     }

*	List Item:

		code block

		with a blank line

	within a list item.

*       code block
        as first element of a list item

*	List Item:
	
		code block with whitespace on preceding line
    Codeblock on second line
    <?php
    echo "hello!";
    ?>

foo bar

    <?php
    echo "hello!";

lorem ipsum

    echo "hello!";
    ?>
    
lorem ipsum	code block on the first line
	
Regular text.

    code block indented by spaces

Regular text.

	the lines in this block  
	all contain trailing spaces  

Regular Text.

	code block on the last line<test a=" content of attribute ">

Fix for backticks within HTML tag: <span attr='ticks'>like this</span>

Here's how you put   backticks   in a code span.A simple definition list:

Term 1
:   Definition 1

Term 2
:   Definition 2

With multiple terms:

Term 1
Term 2
:   Definition 1

Term 3
Term 4
:   Definition 2

With multiple definitions:

Term 1
:   Definition 1
:   Definition 2

Term 2
:   Definition 3
:   Definition 4

With multiple lines per definition:

Term 1
:   Definition 1 line 1 ...
Definition 1 line 2
:   Definition 2 line 1 ...
Definition 2 line 2

Term 2
:   Definition 3 line 2 ...
    Definition 3 line 2
:   Definition 4 line 2 ...
    Definition 4 line 2

With paragraphs:

Term 1

:   Definition 1 (paragraph)

Term 2

:   Definition 2 (paragraph)

With multiple paragraphs:

Term 1

:   Definition 1 paragraph 1 line 1 ...
	Definition 1 paragraph 1 line 2

    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)

    Definition 1 paragraph 2 line 1 ...
Definition 1 paragraph 2 line 2 (lazy)

* * *

A mix:

Term 1
Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)
    
    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

:   Definition 2 paragraph 1 line 1 ...
Definition 2 paragraph 1 line 2 (lazy)

Term 3
:   Definition 3 (no paragraph)
:   Definition 4 (no paragraph)
:   Definition 5 line 1 ...
    Definition 5 line 2 (no paragraph)

:   Definition 6 paragraph 1 line 1 ...
Definition 6 paragraph 1 line 2
:   Definition 7 (no paragraph)
:   Definition 8 paragraph 1 line 1 (forced paragraph) ...
    Definition 8 paragraph 1 line 2
    
    Definition 8 paragraph 2 line 1
    
Term 4
:   Definition 9 paragraph 1 line 1 (forced paragraph) ...
    Definition 9 paragraph 1 line 2
    
    Definition 9 paragraph 2 line 1
:   Definition 10 (no paragraph)

* * *

Special cases:

Term

:       code block
        as first element of a definition<michel.fortin@michelf.ca>

International domain names: <help@tūdaliņ.lv>


## Some weird valid email addresses

<abc.123@example.com>

<1234567890@example.com>

<_______@example.com>

<abc+mailbox/department=shipping@example.com>

<!#$%&'*+-/=?^_.{|}@example.com> (all of these characters are allowed)

<"abc@def"@example.com> (anything goes inside quotation marks)

<"Fred Bloggs"@example.com>

<jsmith@[192.0.2.1]>

<"A"@example.com>Combined emphasis:

1.  ***test test***
2.  ___test test___
3.  *test **test***
4.  **test *test***
5.  ***test* test**
6.  ***test** test*
7.  ***test* test**
8.  **test *test***
9.  *test **test***
10. _test __test___
11. __test _test___
12. ___test_ test__
13. ___test__ test_
14. ___test_ test__
15. __test _test___
16. _test __test___
17. *test __test__*
18. **test _test_**
19. **_test_ test**
20. *__test__ test*
21. **_test_ test**
22. **test _test_**
23. *test __test__*
24. _test **test**_
25. __test *test*__
26. __*test* test__
27. _**test** test_
28. __*test* test__
29. __test *test*__
30. _test **test**_


Incorrect nesting:

1.  *test  **test*  test**
2.  _test  __test_  test__
3.  **test  *test** test*
4.  __test  _test__ test_
5.  *test   *test*  test*
6.  _test   _test_  test_
7.  **test **test** test**
8.  __test __test__ test__
9. _**some text_**
10. *__some text*__
11. **_some text**_
12. *__some text*__

No emphasis:

1.  test*  test  *test
2.  test** test **test
3.  test_  test  _test
4.  test__ test __test



Middle-word emphasis (asterisks):

1.  *a*b
2.   a*b*
3.   a*b*c
4. **a**b
5.   a**b**
6.   a**b**c


Middle-word emphasis (underscore):

1.  _a_b
2.   a_b_
3.   a_b_c
4. __a__b
5.   a__b__
6.   a__b__c

my_precious_file.txt


## Tricky Cases

E**. **Test** TestTestTest

E**. **Test** Test Test Test


## Overlong emphasis

Name: ____________  
Organization: ____  
Region/Country: __

_____Cut here_____

____Cut here____

# Regression

_**Note**_: This _is emphasis_.
With asterisks

 * List item
 *
 * List item

With numbers

1. List item
2.
3. List item

With hyphens

- List item
-
- List item

With asterisks

 * List item
 * List item
 *

With numbers

1. List item
2. List item
3.

With hyphens

- List item
- List item
-
This is the first paragraph.[^first]

[^first]:  This is the first note.

* List item one.[^second]
* List item two.[^third]

[^third]: This is the third note, defined out of order.
[^second]: This is the second note.
[^fourth]: This is the fourth note.

# Header[^fourth]

Some paragraph with a footnote[^1], and another[^2].

[^1]: Content for fifth footnote.
[^2]: Content for sixth footnote spaning on 
    three lines, with some span-level markup like
    _emphasis_, a [link][].

[link]: http://michelf.ca/

Another paragraph with a named footnote[^fn-name].

[^fn-name]:
    Footnote beginning on the line next to the marker.

This paragraph should not have a footnote marker since 
the footnote is undefined.[^3]

This paragraph has a second footnote marker to footnote number one.[^1]

This paragraph links to a footnote with plenty of 
block-level content.[^block]

[^block]:
	Paragraph.
	
	*   List item
	
	> Blockquote
	
	    Code block

This paragraph host the footnote reference within a 
footnote test[^reference].

[^reference]:
	This footnote has a footnote of its own.[^nested]

[^nested]:
	This footnote should appear even though it is referenced
	from another footnote. But [^reference] should be litteral
	since the footnote with that name has already been used.

 - - -

Testing unusual footnote name[^1$^!"'].

[^1$^!"']: Haha!

 - - -
 
Footnotes mixed with images[^image-mixed]
![1800 Travel][img6]
![1830 Travel][img7]

[img6]: images/MGR-1800-travel.jpeg "Travel Speeds in 1800"
[^image-mixed]: Footnote Content
[img7]: images/MGR-1830-travel.jpeg "Travel Speeds in 1830"
In Markdown 1.0.0 and earlier. Version
8. This line turns into a list item.
Because a hard-wrapped line in the
middle of a paragraph looked like a
list item.

Here's one with a bullet.
* criminey.
Header  {#id1}
======

Header  { #id2}
------

### Header  {#id3 }
#### Header ##  { #id4 }

 - - -

Header  {.cl}
======

Header  { .cl}
------

### Header  {.cl }
#### Header ##  { .cl }

 - - -

Header  {.cl.class}
======

Header  { .cl .class}
------

### Header  {.cl .class }
#### Header ##  { .cl.class }

 - - -

Header  {#id5.cl.class}
======

Header  { #id6 .cl .class}
------

### Header  {.cl.class#id7 }
#### Header ##  { .cl.class#id8 }
Header
======

Header
------

### Header

 - - -

Header
======
Paragraph

Header
------
Paragraph

### Header
Paragraph

 - - -

Paragraph
Header
======
Paragraph

Paragraph
Header
------
Paragraph

Paragraph
### Header
ParagraphDashes:

---

 ---
 
  ---

   ---

	---

- - -

 - - -
 
  - - -

   - - -

	- - -


Asterisks:

***

 ***
 
  ***

   ***

	***

* * *

 * * *
 
  * * *

   * * *

	* * *


Underscores:

___

 ___
 
  ___

   ___

    ___

_ _ _

 _ _ _
 
  _ _ _

   _ _ _

    _ _ _
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")

Inline within a paragraph: [alt text](/url/).

![alt text](/url/  "title preceded by two spaces")

![alt text](/url/  "title has spaces afterward"  )

![alt text](</url/>)

![alt text](</url/> "with a title").

![Empty]()

![this is a stupid URL](http://example.com/(parens).jpg)


![alt text][foo]

  [foo]: /url/

![alt text][bar]

  [bar]: /url/ "Title here"Simple block on one line:

<div>foo</div>

And nested without indentation:

<div>
<div>
<div>
foo
</div>
<div style=">"/>
</div>
<div>bar</div>
</div>

And with attributes:

<div>
	<div id="foo">
	</div>
</div>

This was broken in 1.0.2b7:

<div class="inlinepage">
<div class="toggleableend">
foo
</div>
</div>
Here's a simple block:

<div>
	foo
</div>

This should be a code block, though:

	<div>
		foo
	</div>

As should this:

	<div>foo</div>

Now, nested:

<div>
	<div>
		<div>
			foo
		</div>
	</div>
</div>

This should just be an HTML comment:

<!-- Comment -->

Multiline:

<!--
Blah
Blah
-->

Code block:

	<!-- Comment -->

Just plain comment, with trailing spaces on the line:

<!-- foo -->   

Code:

	<hr />
	
Hr's:

<hr>

<hr/>

<hr />

<hr>   

<hr/>  

<hr /> 

<hr class="foo" id="bar" />

<hr class="foo" id="bar"/>

<hr class="foo" id="bar" >

<abbr title=" **Attribute Content Is Not A Code Span** ">ACINACS</abbr>

<abbr title="first backtick!">SB</abbr> 
<abbr title="second backtick!">SB</abbr>Paragraph one.

<!-- This is a simple comment -->

<!--
	This is another comment.
-->

Paragraph two.

<!-- one comment block -- -- with two comments -->

The end.
# Markdown inside code blocks

<div markdown="1">
foo
</div>

<div markdown='1'>
foo
</div>

<div markdown=1>
foo
</div>

<table>
<tr><td markdown="1">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="span">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="block">test _emphasis_ (block)</td></tr>
</table>

## More complicated

<table>
<tr><td markdown="1">
* this is _not_ a list item</td></tr>
<tr><td markdown="span">
* this is _not_ a list item</td></tr>
<tr><td markdown="block">
* this _is_ a list item
</td></tr>
</table>

## With indent

<div>
    <div markdown="1">
    This text is no code block: if it was, the 
    closing <div> would be too and the HTML block 
    would be invalid.

    Markdown content in HTML blocks is assumed to be 
    indented the same as the block opening tag.

    **This should be the third paragraph after the header.**
    </div>
</div>

## Code block with rogue </div>s in Markdown code span and block

<div>
    <div markdown="1">

    This is a code block however:

        </div>

    Funny isn't it? Here is a code span: </div>.

    </div>
</div>

<div>
  <div markdown="1">
    * List item, not a code block

Some text

      This is a code block.
  </div>
</div>

## No code block in markdown span mode

<p markdown="1">
    This is not a code block since Markdown parse paragraph 
    content as span. Code spans like </p> are allowed though.
</p>

<p markdown="1">_Hello_ _world_</p>

## Preserving attributes and tags on more than one line:

<p class="test" markdown="1" 
id="12">
Some _span_ content.
</p>


## Header confusion bug

<table class="canvas">
<tr>
<td id="main" markdown="1">Hello World!
============

Hello World!</td>
</tr>
</table>
Here is a block tag ins:

<ins>
<p>Some text</p>
</ins>

<ins>And here it is inside a paragraph.</ins>

And here it is <ins>in the middle of</ins> a paragraph.

<del>
<p>Some text</p>
</del>

<del>And here is ins as a paragraph.</del>

And here it is <del>in the middle of</del> a paragraph.
		    GNU GENERAL PUBLIC LICENSE
		       Version 2, June 1991

 Copyright (C) 1989, 1991 Free Software Foundation, Inc.,
 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

			    Preamble

  The licenses for most software are designed to take away your
freedom to share and change it.  By contrast, the GNU General Public
License is intended to guarantee your freedom to share and change free
software--to make sure the software is free for all its users.  This
General Public License applies to most of the Free Software
Foundation's software and to any other program whose authors commit to
using it.  (Some other Free Software Foundation software is covered by
the GNU Lesser General Public License instead.)  You can apply it to
your programs, too.

  When we speak of free software, we are referring to freedom, not
price.  Our General Public Licenses are designed to make sure that you
have the freedom to distribute copies of free software (and charge for
this service if you wish), that you receive source code or can get it
if you want it, that you can change the software or use pieces of it
in new free programs; and that you know you can do these things.

  To protect your rights, we need to make restrictions that forbid
anyone to deny you these rights or to ask you to surrender the rights.
These restrictions translate to certain responsibilities for you if you
distribute copies of the software, or if you modify it.

  For example, if you distribute copies of such a program, whether
gratis or for a fee, you must give the recipients all the rights that
you have.  You must make sure that they, too, receive or can get the
source code.  And you must show them these terms so they know their
rights.

  We protect your rights with two steps: (1) copyright the software, and
(2) offer you this license which gives you legal permission to copy,
distribute and/or modify the software.

  Also, for each author's protection and ours, we want to make certain
that everyone understands that there is no warranty for this free
software.  If the software is modified by someone else and passed on, we
want its recipients to know that what they have is not the original, so
that any problems introduced by others will not reflect on the original
authors' reputations.

  Finally, any free program is threatened constantly by software
patents.  We wish to avoid the danger that redistributors of a free
program will individually obtain patent licenses, in effect making the
program proprietary.  To prevent this, we have made it clear that any
patent must be licensed for everyone's free use or not licensed at all.

  The precise terms and conditions for copying, distribution and
modification follow.

		    GNU GENERAL PUBLIC LICENSE
   TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

  0. This License applies to any program or other work which contains
a notice placed by the copyright holder saying it may be distributed
under the terms of this General Public License.  The "Program", below,
refers to any such program or work, and a "work based on the Program"
means either the Program or any derivative work under copyright law:
that is to say, a work containing the Program or a portion of it,
either verbatim or with modifications and/or translated into another
language.  (Hereinafter, translation is included without limitation in
the term "modification".)  Each licensee is addressed as "you".

Activities other than copying, distribution and modification are not
covered by this License; they are outside its scope.  The act of
running the Program is not restricted, and the output from the Program
is covered only if its contents constitute a work based on the
Program (independent of having been made by running the Program).
Whether that is true depends on what the Program does.

  1. You may copy and distribute verbatim copies of the Program's
source code as you receive it, in any medium, provided that you
conspicuously and appropriately publish on each copy an appropriate
copyright notice and disclaimer of warranty; keep intact all the
notices that refer to this License and to the absence of any warranty;
and give any other recipients of the Program a copy of this License
along with the Program.

You may charge a fee for the physical act of transferring a copy, and
you may at your option offer warranty protection in exchange for a fee.

  2. You may modify your copy or copies of the Program or any portion
of it, thus forming a work based on the Program, and copy and
distribute such modifications or work under the terms of Section 1
above, provided that you also meet all of these conditions:

    a) You must cause the modified files to carry prominent notices
    stating that you changed the files and the date of any change.

    b) You must cause any work that you distribute or publish, that in
    whole or in part contains or is derived from the Program or any
    part thereof, to be licensed as a whole at no charge to all third
    parties under the terms of this License.

    c) If the modified program normally reads commands interactively
    when run, you must cause it, when started running for such
    interactive use in the most ordinary way, to print or display an
    announcement including an appropriate copyright notice and a
    notice that there is no warranty (or else, saying that you provide
    a warranty) and that users may redistribute the program under
    these conditions, and telling the user how to view a copy of this
    License.  (Exception: if the Program itself is interactive but
    does not normally print such an announcement, your work based on
    the Program is not required to print an announcement.)

These requirements apply to the modified work as a whole.  If
identifiable sections of that work are not derived from the Program,
and can be reasonably considered independent and separate works in
themselves, then this License, and its terms, do not apply to those
sections when you distribute them as separate works.  But when you
distribute the same sections as part of a whole which is a work based
on the Program, the distribution of the whole must be on the terms of
this License, whose permissions for other licensees extend to the
entire whole, and thus to each and every part regardless of who wrote it.

Thus, it is not the intent of this section to claim rights or contest
your rights to work written entirely by you; rather, the intent is to
exercise the right to control the distribution of derivative or
collective works based on the Program.

In addition, mere aggregation of another work not based on the Program
with the Program (or with a work based on the Program) on a volume of
a storage or distribution medium does not bring the other work under
the scope of this License.

  3. You may copy and distribute the Program (or a work based on it,
under Section 2) in object code or executable form under the terms of
Sections 1 and 2 above provided that you also do one of the following:

    a) Accompany it with the complete corresponding machine-readable
    source code, which must be distributed under the terms of Sections
    1 and 2 above on a medium customarily used for software interchange; or,

    b) Accompany it with a written offer, valid for at least three
    years, to give any third party, for a charge no more than your
    cost of physically performing source distribution, a complete
    machine-readable copy of the corresponding source code, to be
    distributed under the terms of Sections 1 and 2 above on a medium
    customarily used for software interchange; or,

    c) Accompany it with the information you received as to the offer
    to distribute corresponding source code.  (This alternative is
    allowed only for noncommercial distribution and only if you
    received the program in object code or executable form with such
    an offer, in accord with Subsection b above.)

The source code for a work means the preferred form of the work for
making modifications to it.  For an executable work, complete source
code means all the source code for all modules it contains, plus any
associated interface definition files, plus the scripts used to
control compilation and installation of the executable.  However, as a
special exception, the source code distributed need not include
anything that is normally distributed (in either source or binary
form) with the major components (compiler, kernel, and so on) of the
operating system on which the executable runs, unless that component
itself accompanies the executable.

If distribution of executable or object code is made by offering
access to copy from a designated place, then offering equivalent
access to copy the source code from the same place counts as
distribution of the source code, even though third parties are not
compelled to copy the source along with the object code.

  4. You may not copy, modify, sublicense, or distribute the Program
except as expressly provided under this License.  Any attempt
otherwise to copy, modify, sublicense or distribute the Program is
void, and will automatically terminate your rights under this License.
However, parties who have received copies, or rights, from you under
this License will not have their licenses terminated so long as such
parties remain in full compliance.

  5. You are not required to accept this License, since you have not
signed it.  However, nothing else grants you permission to modify or
distribute the Program or its derivative works.  These actions are
prohibited by law if you do not accept this License.  Therefore, by
modifying or distributing the Program (or any work based on the
Program), you indicate your acceptance of this License to do so, and
all its terms and conditions for copying, distributing or modifying
the Program or works based on it.

  6. Each time you redistribute the Program (or any work based on the
Program), the recipient automatically receives a license from the
original licensor to copy, distribute or modify the Program subject to
these terms and conditions.  You may not impose any further
restrictions on the recipients' exercise of the rights granted herein.
You are not responsible for enforcing compliance by third parties to
this License.

  7. If, as a consequence of a court judgment or allegation of patent
infringement or for any other reason (not limited to patent issues),
conditions are imposed on you (whether by court order, agreement or
otherwise) that contradict the conditions of this License, they do not
excuse you from the conditions of this License.  If you cannot
distribute so as to satisfy simultaneously your obligations under this
License and any other pertinent obligations, then as a consequence you
may not distribute the Program at all.  For example, if a patent
license would not permit royalty-free redistribution of the Program by
all those who receive copies directly or indirectly through you, then
the only way you could satisfy both it and this License would be to
refrain entirely from distribution of the Program.

If any portion of this section is held invalid or unenforceable under
any particular circumstance, the balance of the section is intended to
apply and the section as a whole is intended to apply in other
circumstances.

It is not the purpose of this section to induce you to infringe any
patents or other property right claims or to contest validity of any
such claims; this section has the sole purpose of protecting the
integrity of the free software distribution system, which is
implemented by public license practices.  Many people have made
generous contributions to the wide range of software distributed
through that system in reliance on consistent application of that
system; it is up to the author/donor to decide if he or she is willing
to distribute software through any other system and a licensee cannot
impose that choice.

This section is intended to make thoroughly clear what is believed to
be a consequence of the rest of this License.

  8. If the distribution and/or use of the Program is restricted in
certain countries either by patents or by copyrighted interfaces, the
original copyright holder who places the Program under this License
may add an explicit geographical distribution limitation excluding
those countries, so that distribution is permitted only in or among
countries not thus excluded.  In such case, this License incorporates
the limitation as if written in the body of this License.

  9. The Free Software Foundation may publish revised and/or new versions
of the General Public License from time to time.  Such new versions will
be similar in spirit to the present version, but may differ in detail to
address new problems or concerns.

Each version is given a distinguishing version number.  If the Program
specifies a version number of this License which applies to it and "any
later version", you have the option of following the terms and conditions
either of that version or of any later version published by the Free
Software Foundation.  If the Program does not specify a version number of
this License, you may choose any version ever published by the Free Software
Foundation.

  10. If you wish to incorporate parts of the Program into other free
programs whose distribution conditions are different, write to the author
to ask for permission.  For software which is copyrighted by the Free
Software Foundation, write to the Free Software Foundation; we sometimes
make exceptions for this.  Our decision will be guided by the two goals
of preserving the free status of all derivatives of our free software and
of promoting the sharing and reuse of software generally.

			    NO WARRANTY

  11. BECAUSE THE PROGRAM IS LICENSED FREE OF CHARGE, THERE IS NO WARRANTY
FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW.  EXCEPT WHEN
OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES
PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED
OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.  THE ENTIRE RISK AS
TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU.  SHOULD THE
PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING,
REPAIR OR CORRECTION.

  12. IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING
WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MAY MODIFY AND/OR
REDISTRIBUTE THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES,
INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING
OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED
TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY
YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER
PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES.

		     END OF TERMS AND CONDITIONS

	    How to Apply These Terms to Your New Programs

  If you develop a new program, and you want it to be of the greatest
possible use to the public, the best way to achieve this is to make it
free software which everyone can redistribute and change under these terms.

  To do so, attach the following notices to the program.  It is safest
to attach them to the start of each source file to most effectively
convey the exclusion of warranty; and each file should have at least
the "copyright" line and a pointer to where the full notice is found.

    <one line to give the program's name and a brief idea of what it does.>
    Copyright (C) <year>  <name of author>

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

Also add information on how to contact you by electronic and paper mail.

If the program is interactive, make it output a short notice like this
when it starts in an interactive mode:

    Gnomovision version 69, Copyright (C) year name of author
    Gnomovision comes with ABSOLUTELY NO WARRANTY; for details type show w'.
    This is free software, and you are welcome to redistribute it
    under certain conditions; type show c' for details.

The hypothetical commands show w' and show c' should show the appropriate
parts of the General Public License.  Of course, the commands you use may
be called something other than show w' and show c'; they could even be
mouse-clicks or menu items--whatever suits your program.

You should also get your employer (if you work as a programmer) or your
school, if any, to sign a "copyright disclaimer" for the program, if
necessary.  Here is a sample; alter the names:

  Yoyodyne, Inc., hereby disclaims all copyright interest in the program
  Gnomovision' (which makes passes at compilers) written by James Hacker.

  <signature of Ty Coon>, 1 April 1989
  Ty Coon, President of Vice

This General Public License does not permit incorporating your program into
proprietary programs.  If your program is a subroutine library, you may
consider it more useful to permit linking proprietary applications with the
library.  If this is what you want to do, use the GNU Lesser General
Public License instead of this License.
This is an [inline link](/url "title"){.class #inline-link}.

This is a [reference link][refid].

This is an ![inline image](/img "title"){.class #inline-img}.

This is a ![reference image][refid].

[refid]: /path/to/something (Title) { .class #ref data-key=val }

Just a [URL](/url/).

[URL and title](/url/ "title").

[URL and title](/url/  "title preceded by two spaces").

[URL and title](/url/	"title preceded by a tab").

[URL and title](/url/ "title has spaces afterward"  ).

[URL wrapped in angle brackets](</url/>).

[URL w/ angle brackets + title](</url/> "Here's the title").

[Empty]().

[With parens in the URL](http://en.wikipedia.org/wiki/WIMP_(computing))

(With outer parens and [parens in url](/foo(bar)))


[With parens in the URL](/foo(bar) "and a title")

(With outer parens and [parens in url](/foo(bar) "and a title"))
Foo [bar] [1].

Foo [bar][1].

Foo [bar]
[1].

[1]: /url/  "Title"


With [embedded [brackets]] [b].


Indented [once][].

Indented [twice][].

Indented [thrice][].

Indented [four][] times.

 [once]: /url

  [twice]: /url

   [thrice]: /url

    [four]: /url


[b]: /url/

* * *

[this] [this] should work

So should [this][this].

And [this] [].

And [this][].

And [this].

But not [that] [].

Nor [that][].

Nor [that].

[Something in brackets like [this][] should work]

[Same with [this].]

In this case, [this](/somethingelse/) points to something else.

Backslashing should suppress \[this] and [this\].

[this]: foo


* * *

Here's one where the [link
breaks] across lines.

Here's another where the [link 
breaks] across lines, but with a line-ending space.


[link breaks]: /url/
This is the [simple case].

[simple case]: /simple



This one has a [line
break].

This one has a [line 
break] with a line-ending space.

[line break]: /foo


[this] [that] and the [other]

[this]: /this
[that]: /that
[other]: /other
Foo [bar][].

Foo [bar](/url/ "Title with "quotes" inside").


  [bar]: /url/ "Title with "quotes" inside"

Markdown: Basics
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a class="selected" title="Markdown Basics">Basics</a></li>
    <li><a href="/projects/markdown/syntax" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


Getting the Gist of Markdown's Formatting Syntax
------------------------------------------------

This page offers a brief overview of what it's like to use Markdown.
The [syntax page] [s] provides complete, detailed documentation for
every feature, but Markdown should be very easy to pick up simply by
looking at a few examples of it in action. The examples on this page
are written in a before/after style, showing example syntax and the
HTML output produced by Markdown.

It's also helpful to simply try Markdown out; the [Dingus] [d] is a
web application that allows you type your own Markdown-formatted text
and translate it to XHTML.

**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL] [src].

  [s]: /projects/markdown/syntax  "Markdown Syntax"
  [d]: /projects/markdown/dingus  "Markdown Dingus"
  [src]: /projects/markdown/basics.text


## Paragraphs, Headers, Blockquotes ##

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

Markdown offers two styles of headers: *Setext* and *atx*.
Setext-style headers for <h1> and <h2> are created by
"underlining" with equal signs (=) and hyphens (-), respectively.
To create an atx-style header, you put 1-6 hash marks (#) at the
beginning of the line -- the number of hashes equals the resulting
HTML header level.

Blockquotes are indicated using email-style '>' angle brackets.

Markdown:

    A First Level Header
    ====================
    
    A Second Level Header
    ---------------------

    Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.

    The quick brown fox jumped over the lazy
    dog's back.
    
    ### Header 3

    > This is a blockquote.
    > 
    > This is the second paragraph in the blockquote.
    >
    > ## This is an H2 in a blockquote


Output:

    <h1>A First Level Header</h1>
    
    <h2>A Second Level Header</h2>
    
    <p>Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.</p>
    
    <p>The quick brown fox jumped over the lazy
    dog's back.</p>
    
    <h3>Header 3</h3>
    
    <blockquote>
        <p>This is a blockquote.</p>
        
        <p>This is the second paragraph in the blockquote.</p>
        
        <h2>This is an H2 in a blockquote</h2>
    </blockquote>



### Phrase Emphasis ###

Markdown uses asterisks and underscores to indicate spans of emphasis.

Markdown:

    Some of these words *are emphasized*.
    Some of these words _are emphasized also_.
    
    Use two asterisks for **strong emphasis**.
    Or, if you prefer, __use two underscores instead__.

Output:

    <p>Some of these words <em>are emphasized</em>.
    Some of these words <em>are emphasized also</em>.</p>
    
    <p>Use two asterisks for <strong>strong emphasis</strong>.
    Or, if you prefer, <strong>use two underscores instead</strong>.</p>
   


## Lists ##

Unordered (bulleted) lists use asterisks, pluses, and hyphens (*,
+, and -) as list markers. These three markers are
interchangable; this:

    *   Candy.
    *   Gum.
    *   Booze.

this:

    +   Candy.
    +   Gum.
    +   Booze.

and this:

    -   Candy.
    -   Gum.
    -   Booze.

all produce the same output:

    <ul>
    <li>Candy.</li>
    <li>Gum.</li>
    <li>Booze.</li>
    </ul>

Ordered (numbered) lists use regular numbers, followed by periods, as
list markers:

    1.  Red
    2.  Green
    3.  Blue

Output:

    <ol>
    <li>Red</li>
    <li>Green</li>
    <li>Blue</li>
    </ol>

If you put blank lines between items, you'll get <p> tags for the
list item text. You can create multi-paragraph list items by indenting
the paragraphs by 4 spaces or 1 tab:

    *   A list item.
    
        With multiple paragraphs.

    *   Another item in the list.

Output:

    <ul>
    <li><p>A list item.</p>
    <p>With multiple paragraphs.</p></li>
    <li><p>Another item in the list.</p></li>
    </ul>
    


### Links ###

Markdown supports two styles for creating links: *inline* and
*reference*. With both styles, you use square brackets to delimit the
text you want to turn into a link.

Inline-style links use parentheses immediately after the link text.
For example:

    This is an [example link](http://example.com/).

Output:

    <p>This is an <a href="http://example.com/">
    example link</a>.</p>

Optionally, you may include a title attribute in the parentheses:

    This is an [example link](http://example.com/ "With a Title").

Output:

    <p>This is an <a href="http://example.com/" title="With a Title">
    example link</a>.</p>

Reference-style links allow you to refer to your links by names, which
you define elsewhere in your document:

    I get 10 times more traffic from [Google][1] than from
    [Yahoo][2] or [MSN][3].

    [1]: http://google.com/        "Google"
    [2]: http://search.yahoo.com/  "Yahoo Search"
    [3]: http://search.msn.com/    "MSN Search"

Output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from <a href="http://search.yahoo.com/"
    title="Yahoo Search">Yahoo</a> or <a href="http://search.msn.com/"
    title="MSN Search">MSN</a>.</p>

The title attribute is optional. Link names may contain letters,
numbers and spaces, but are *not* case sensitive:

    I start my morning with a cup of coffee and
    [The New York Times][NY Times].

    [ny times]: http://www.nytimes.com/

Output:

    <p>I start my morning with a cup of coffee and
    <a href="http://www.nytimes.com/">The New York Times</a>.</p>


### Images ###

Image syntax is very much like link syntax.

Inline (titles are optional):

    ![alt text](/path/to/img.jpg "Title")

Reference-style:

    ![alt text][id]

    [id]: /path/to/img.jpg "Title"

Both of the above examples produce the same output:

    <img src="/path/to/img.jpg" alt="alt text" title="Title" />



### Code ###

In a regular paragraph, you can create code span by wrapping text in
backtick quotes. Any ampersands (&) and angle brackets (< or
>) will automatically be translated into HTML entities. This makes
it easy to use Markdown to write about HTML example code:

    I strongly recommend against using any <blink> tags.

    I wish SmartyPants used named entities like &mdash;
    instead of decimal-encoded entites like &#8212;.

Output:

    <p>I strongly recommend against using any
    <code>&lt;blink&gt;</code> tags.</p>
    
    <p>I wish SmartyPants used named entities like
    <code>&amp;mdash;</code> instead of decimal-encoded
    entites like <code>&amp;#8212;</code>.</p>


To specify an entire block of pre-formatted code, indent every line of
the block by 4 spaces or 1 tab. Just like with code spans, &, <,
and > characters will be escaped automatically.

Markdown:

    If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:

        <blockquote>
            <p>For example.</p>
        </blockquote>

Output:

    <p>If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:</p>
    
    <pre><code>&lt;blockquote&gt;
        &lt;p&gt;For example.&lt;/p&gt;
    &lt;/blockquote&gt;
    </code></pre>
Markdown: Syntax
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a href="/projects/markdown/basics" title="Markdown Basics">Basics</a></li>
    <li><a class="selected" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


*   [Overview](#overview)
    *   [Philosophy](#philosophy)
    *   [Inline HTML](#html)
    *   [Automatic Escaping for Special Characters](#autoescape)
*   [Block Elements](#block)
    *   [Paragraphs and Line Breaks](#p)
    *   [Headers](#header)
    *   [Blockquotes](#blockquote)
    *   [Lists](#list)
    *   [Code Blocks](#precode)
    *   [Horizontal Rules](#hr)
*   [Span Elements](#span)
    *   [Links](#link)
    *   [Emphasis](#em)
    *   [Code](#code)
    *   [Images](#img)
*   [Miscellaneous](#misc)
    *   [Backslash Escapes](#backslash)
    *   [Automatic Links](#autolink)


**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL][src].

  [src]: /projects/markdown/syntax.text

* * *

<h2 id="overview">Overview</h2>

<h3 id="philosophy">Philosophy</h3>

Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

Readability, however, is emphasized above all else. A Markdown-formatted
document should be publishable as-is, as plain text, without looking
like it's been marked up with tags or formatting instructions. While
Markdown's syntax has been influenced by several existing text-to-HTML
filters -- including [Setext] [1], [atx] [2], [Textile] [3], [reStructuredText] [4],
[Grutatext] [5], and [EtText] [6] -- the single biggest source of
inspiration for Markdown's syntax is the format of plain text email.

  [1]: http://docutils.sourceforge.net/mirror/setext.html
  [2]: http://www.aaronsw.com/2002/atx/
  [3]: http://textism.com/tools/textile/
  [4]: http://docutils.sourceforge.net/rst.html
  [5]: http://www.triptico.com/software/grutatxt.html
  [6]: http://ettext.taint.org/doc/

To this end, Markdown's syntax is comprised entirely of punctuation
characters, which punctuation characters have been carefully chosen so
as to look like what they mean. E.g., asterisks around a word actually
look like \*emphasis\*. Markdown lists look like, well, lists. Even
blockquotes look like quoted passages of text, assuming you've ever
used email.



<h3 id="html">Inline HTML</h3>

Markdown's syntax is intended for one purpose: to be used as a
format for *writing* for the web.

Markdown is not a replacement for HTML, or even close to it. Its
syntax is very small, corresponding only to a very small subset of
HTML tags. The idea is *not* to create a syntax that makes it easier
to insert HTML tags. In my opinion, HTML tags are already easy to
insert. The idea for Markdown is to make it easy to read, write, and
edit prose. HTML is a *publishing* format; Markdown is a *writing*
format. Thus, Markdown's formatting syntax only addresses issues that
can be conveyed in plain text.

For any markup that is not covered by Markdown's syntax, you simply
use HTML itself. There's no need to preface it or delimit it to
indicate that you're switching from Markdown to HTML; you just use
the tags.

The only restrictions are that block-level HTML elements -- e.g. <div>,
<table>, <pre>, <p>, etc. -- must be separated from surrounding
content by blank lines, and the start and end tags of the block should
not be indented with tabs or spaces. Markdown is smart enough not
to add extra (unwanted) <p> tags around HTML block-level tags.

For example, to add an HTML table to a Markdown article:

    This is a regular paragraph.

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    This is another regular paragraph.

Note that Markdown formatting syntax is not processed within block-level
HTML tags. E.g., you can't use Markdown-style *emphasis* inside an
HTML block.

Span-level HTML tags -- e.g. <span>, <cite>, or <del> -- can be
used anywhere in a Markdown paragraph, list item, or header. If you
want, you can even use HTML tags instead of Markdown formatting; e.g. if
you'd prefer to use HTML <a> or <img> tags instead of Markdown's
link or image syntax, go right ahead.

Unlike block-level HTML tags, Markdown syntax *is* processed within
span-level tags.


<h3 id="autoescape">Automatic Escaping for Special Characters</h3>

In HTML, there are two characters that demand special treatment: <
and &. Left angle brackets are used to start tags; ampersands are
used to denote HTML entities. If you want to use them as literal
characters, you must escape them as entities, e.g. &lt;, and
&amp;.

Ampersands in particular are bedeviling for web writers. If you want to
write about 'AT&T', you need to write 'AT&amp;T'. You even need to
escape ampersands within URLs. Thus, if you want to link to:

    http://images.google.com/images?num=30&q=larry+bird

you need to encode the URL as:

    http://images.google.com/images?num=30&amp;q=larry+bird

in your anchor tag href attribute. Needless to say, this is easy to
forget, and is probably the single most common source of HTML validation
errors in otherwise well-marked-up web sites.

Markdown allows you to use these characters naturally, taking care of
all the necessary escaping for you. If you use an ampersand as part of
an HTML entity, it remains unchanged; otherwise it will be translated
into &amp;.

So, if you want to include a copyright symbol in your article, you can write:

    &copy;

and Markdown will leave it alone. But if you write:

    AT&T

Markdown will translate it to:

    AT&amp;T

Similarly, because Markdown supports [inline HTML](#html), if you use
angle brackets as delimiters for HTML tags, Markdown will treat them as
such. But if you write:

    4 < 5

Markdown will translate it to:

    4 &lt; 5

However, inside Markdown code spans and blocks, angle brackets and
ampersands are *always* encoded automatically. This makes it easy to use
Markdown to write about HTML code. (As opposed to raw HTML, which is a
terrible format for writing about HTML syntax, because every single <
and & in your example code needs to be escaped.)


* * *


<h2 id="block">Block Elements</h2>


<h3 id="p">Paragraphs and Line Breaks</h3>

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing but spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

The implication of the "one or more consecutive lines of text" rule is
that Markdown supports "hard-wrapped" text paragraphs. This differs
significantly from most other text-to-HTML formatters (including Movable
Type's "Convert Line Breaks" option) which translate every line break
character in a paragraph into a <br /> tag.

When you *do* want to insert a <br /> break tag using Markdown, you
end a line with two or more spaces, then type return.

Yes, this takes a tad more effort to create a <br />, but a simplistic
"every line break is a <br />" rule wouldn't work for Markdown.
Markdown's email-style [blockquoting][bq] and multi-paragraph [list items][l]
work best -- and look better -- when you format them with hard breaks.

  [bq]: #blockquote
  [l]:  #list



<h3 id="header">Headers</h3>

Markdown supports two styles of headers, [Setext] [1] and [atx] [2].

Setext-style headers are "underlined" using equal signs (for first-level
headers) and dashes (for second-level headers). For example:

    This is an H1
    =============

    This is an H2
    -------------

Any number of underlining ='s or -'s will work.

Atx-style headers use 1-6 hash characters at the start of the line,
corresponding to header levels 1-6. For example:

    # This is an H1

    ## This is an H2

    ###### This is an H6

Optionally, you may "close" atx-style headers. This is purely
cosmetic -- you can use this if you think it looks better. The
closing hashes don't even need to match the number of hashes
used to open the header. (The number of opening hashes
determines the header level.) :

    # This is an H1 #

    ## This is an H2 ##

    ### This is an H3 ######


<h3 id="blockquote">Blockquotes</h3>

Markdown uses email-style > characters for blockquoting. If you're
familiar with quoting passages of text in an email message, then you
know how to create a blockquote in Markdown. It looks best if you hard
wrap the text and put a > before every line:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    > 
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

Markdown allows you to be lazy and only put the > before the first
line of a hard-wrapped paragraph:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

Blockquotes can be nested (i.e. a blockquote-in-a-blockquote) by
adding additional levels of >:

    > This is the first level of quoting.
    >
    > > This is nested blockquote.
    >
    > Back to the first level.

Blockquotes can contain other Markdown elements, including headers, lists,
and code blocks:

	> ## This is a header.
	> 
	> 1.   This is the first list item.
	> 2.   This is the second list item.
	> 
	> Here's some example code:
	> 
	>     return shell_exec("echo $input | $markdown_script");

Any decent text editor should make email-style quoting easy. For
example, with BBEdit, you can make a selection and choose Increase
Quote Level from the Text menu.


<h3 id="list">Lists</h3>

Markdown supports ordered (numbered) and unordered (bulleted) lists.

Unordered lists use asterisks, pluses, and hyphens -- interchangably
-- as list markers:

    *   Red
    *   Green
    *   Blue

is equivalent to:

    +   Red
    +   Green
    +   Blue

and:

    -   Red
    -   Green
    -   Blue

Ordered lists use numbers followed by periods:

    1.  Bird
    2.  McHale
    3.  Parish

It's important to note that the actual numbers you use to mark the
list have no effect on the HTML output Markdown produces. The HTML
Markdown produces from the above list is:

    <ol>
    <li>Bird</li>
    <li>McHale</li>
    <li>Parish</li>
    </ol>

If you instead wrote the list in Markdown like this:

    1.  Bird
    1.  McHale
    1.  Parish

or even:

    3. Bird
    1. McHale
    8. Parish

you'd get the exact same HTML output. The point is, if you want to,
you can use ordinal numbers in your ordered Markdown lists, so that
the numbers in your source match the numbers in your published HTML.
But if you want to be lazy, you don't have to.

If you do use lazy list numbering, however, you should still start the
list with the number 1. At some point in the future, Markdown may support
starting ordered lists at an arbitrary number.

List markers typically start at the left margin, but may be indented by
up to three spaces. List markers must be followed by one or more spaces
or a tab.

To make lists look nice, you can wrap items with hanging indents:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
        Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
        viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
        Suspendisse id sem consectetuer libero luctus adipiscing.

But if you want to be lazy, you don't have to:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.

If list items are separated by blank lines, Markdown will wrap the
items in <p> tags in the HTML output. For example, this input:

    *   Bird
    *   Magic

will turn into:

    <ul>
    <li>Bird</li>
    <li>Magic</li>
    </ul>

But this:

    *   Bird

    *   Magic

will turn into:

    <ul>
    <li><p>Bird</p></li>
    <li><p>Magic</p></li>
    </ul>

List items may consist of multiple paragraphs. Each subsequent
paragraph in a list item must be intended by either 4 spaces
or one tab:

    1.  This is a list item with two paragraphs. Lorem ipsum dolor
        sit amet, consectetuer adipiscing elit. Aliquam hendrerit
        mi posuere lectus.

        Vestibulum enim wisi, viverra nec, fringilla in, laoreet
        vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
        sit amet velit.

    2.  Suspendisse id sem consectetuer libero luctus adipiscing.

It looks nice if you indent every line of the subsequent
paragraphs, but here again, Markdown will allow you to be
lazy:

    *   This is a list item with two paragraphs.

        This is the second paragraph in the list item. You're
    only required to indent the first line. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit.

    *   Another item in the same list.

To put a blockquote within a list item, the blockquote's >
delimiters need to be indented:

    *   A list item with a blockquote:

        > This is a blockquote
        > inside a list item.

To put a code block within a list item, the code block needs
to be indented *twice* -- 8 spaces or two tabs:

    *   A list item with a code block:

            <code goes here>


It's worth noting that it's possible to trigger an ordered list by
accident, by writing something like this:

    1986. What a great season.

In other words, a *number-period-space* sequence at the beginning of a
line. To avoid this, you can backslash-escape the period:

    1986\. What a great season.



<h3 id="precode">Code Blocks</h3>

Pre-formatted code blocks are used for writing about programming or
markup source code. Rather than forming normal paragraphs, the lines
of a code block are interpreted literally. Markdown wraps a code block
in both <pre> and <code> tags.

To produce a code block in Markdown, simply indent every line of the
block by at least 4 spaces or 1 tab. For example, given this input:

    This is a normal paragraph:

        This is a code block.

Markdown will generate:

    <p>This is a normal paragraph:</p>

    <pre><code>This is a code block.
    </code></pre>

One level of indentation -- 4 spaces or 1 tab -- is removed from each
line of the code block. For example, this:

    Here is an example of AppleScript:

        tell application "Foo"
            beep
        end tell

will turn into:

    <p>Here is an example of AppleScript:</p>

    <pre><code>tell application "Foo"
        beep
    end tell
    </code></pre>

A code block continues until it reaches a line that is not indented
(or the end of the article).

Within a code block, ampersands (&) and angle brackets (< and >)
are automatically converted into HTML entities. This makes it very
easy to include example HTML source code using Markdown -- just paste
it and indent it, and Markdown will handle the hassle of encoding the
ampersands and angle brackets. For example, this:

        <div class="footer">
            &copy; 2004 Foo Corporation
        </div>

will turn into:

    <pre><code>&lt;div class="footer"&gt;
        &amp;copy; 2004 Foo Corporation
    &lt;/div&gt;
    </code></pre>

Regular Markdown syntax is not processed within code blocks. E.g.,
asterisks are just literal asterisks within a code block. This means
it's also easy to use Markdown to write about Markdown's own syntax.



<h3 id="hr">Horizontal Rules</h3>

You can produce a horizontal rule tag (<hr />) by placing three or
more hyphens, asterisks, or underscores on a line by themselves. If you
wish, you may use spaces between the hyphens or asterisks. Each of the
following lines will produce a horizontal rule:

    * * *

    ***

    *****
	
    - - -

    ---------------------------------------

	_ _ _


* * *

<h2 id="span">Span Elements</h2>

<h3 id="link">Links</h3>

Markdown supports two style of links: *inline* and *reference*.

In both styles, the link text is delimited by [square brackets].

To create an inline link, use a set of regular parentheses immediately
after the link text's closing square bracket. Inside the parentheses,
put the URL where you want the link to point, along with an *optional*
title for the link, surrounded in quotes. For example:

    This is [an example](http://example.com/ "Title") inline link.

    [This link](http://example.net/) has no title attribute.

Will produce:

    <p>This is <a href="http://example.com/" title="Title">
    an example</a> inline link.</p>

    <p><a href="http://example.net/">This link</a> has no
    title attribute.</p>

If you're referring to a local resource on the same server, you can
use relative paths:

    See my [About](/about/) page for details.

Reference-style links use a second set of square brackets, inside
which you place a label of your choosing to identify the link:

    This is [an example][id] reference-style link.

You can optionally use a space to separate the sets of brackets:

    This is [an example] [id] reference-style link.

Then, anywhere in the document, you define your link label like this,
on a line by itself:

    [id]: http://example.com/  "Optional Title Here"

That is:

*   Square brackets containing the link identifier (optionally
    indented from the left margin using up to three spaces);
*   followed by a colon;
*   followed by one or more spaces (or tabs);
*   followed by the URL for the link;
*   optionally followed by a title attribute for the link, enclosed
    in double or single quotes.

The link URL may, optionally, be surrounded by angle brackets:

    [id]: <http://example.com/>  "Optional Title Here"

You can put the title attribute on the next line and use extra spaces
or tabs for padding, which tends to look better with longer URLs:

    [id]: http://example.com/longish/path/to/resource/here
        "Optional Title Here"

Link definitions are only used for creating links during Markdown
processing, and are stripped from your document in the HTML output.

Link definition names may constist of letters, numbers, spaces, and punctuation -- but they are *not* case sensitive. E.g. these two links:

	[link text][a]
	[link text][A]

are equivalent.

The *implicit link name* shortcut allows you to omit the name of the
link, in which case the link text itself is used as the name.
Just use an empty set of square brackets -- e.g., to link the word
"Google" to the google.com web site, you could simply write:

	[Google][]

And then define the link:

	[Google]: http://google.com/

Because link names may contain spaces, this shortcut even works for
multiple words in the link text:

	Visit [Daring Fireball][] for more information.

And then define the link:
	
	[Daring Fireball]: http://daringfireball.net/

Link definitions can be placed anywhere in your Markdown document. I
tend to put them immediately after each paragraph in which they're
used, but if you want, you can put them all at the end of your
document, sort of like footnotes.

Here's an example of reference links in action:

    I get 10 times more traffic from [Google] [1] than from
    [Yahoo] [2] or [MSN] [3].

      [1]: http://google.com/        "Google"
      [2]: http://search.yahoo.com/  "Yahoo Search"
      [3]: http://search.msn.com/    "MSN Search"

Using the implicit link name shortcut, you could instead write:

    I get 10 times more traffic from [Google][] than from
    [Yahoo][] or [MSN][].

      [google]: http://google.com/        "Google"
      [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
      [msn]:    http://search.msn.com/    "MSN Search"

Both of the above examples will produce the following HTML output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from
    <a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a>
    or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p>

For comparison, here is the same paragraph written using
Markdown's inline link style:

    I get 10 times more traffic from [Google](http://google.com/ "Google")
    than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or
    [MSN](http://search.msn.com/ "MSN Search").

The point of reference-style links is not that they're easier to
write. The point is that with reference-style links, your document
source is vastly more readable. Compare the above examples: using
reference-style links, the paragraph itself is only 81 characters
long; with inline-style links, it's 176 characters; and as raw HTML,
it's 234 characters. In the raw HTML, there's more markup than there
is text.

With Markdown's reference-style links, a source document much more
closely resembles the final output, as rendered in a browser. By
allowing you to move the markup-related metadata out of the paragraph,
you can add links without interrupting the narrative flow of your
prose.


<h3 id="em">Emphasis</h3>

Markdown treats asterisks (*) and underscores (_) as indicators of
emphasis. Text wrapped with one * or _ will be wrapped with an
HTML <em> tag; double *'s or _'s will be wrapped with an HTML
<strong> tag. E.g., this input:

    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__

will produce:

    <em>single asterisks</em>

    <em>single underscores</em>

    <strong>double asterisks</strong>

    <strong>double underscores</strong>

You can use whichever style you prefer; the lone restriction is that
the same character must be used to open and close an emphasis span.

Emphasis can be used in the middle of a word:

    un*fucking*believable

But if you surround an * or _ with spaces, it'll be treated as a
literal asterisk or underscore.

To produce a literal asterisk or underscore at a position where it
would otherwise be used as an emphasis delimiter, you can backslash
escape it:

    \*this text is surrounded by literal asterisks\*



<h3 id="code">Code</h3>

To indicate a span of code, wrap it with backtick quotes (  ).
Unlike a pre-formatted code block, a code span indicates code within a
normal paragraph. For example:

    Use the printf() function.

will produce:

    <p>Use the <code>printf()</code> function.</p>

To include a literal backtick character within a code span, you can use
multiple backticks as the opening and closing delimiters:

     There is a literal backtick () here.

which will produce this:

    <p><code>There is a literal backtick () here.</code></p>

The backtick delimiters surrounding a code span may include spaces --
one after the opening, one before the closing. This allows you to place
literal backtick characters at the beginning or end of a code span:

	A single backtick in a code span:     
	
	A backtick-delimited string in a code span:   foo  

will produce:

	<p>A single backtick in a code span: <code></code></p>
	
	<p>A backtick-delimited string in a code span: <code>foo</code></p>

With a code span, ampersands and angle brackets are encoded as HTML
entities automatically, which makes it easy to include example HTML
tags. Markdown will turn this:

    Please don't use any <blink> tags.

into:

    <p>Please don't use any <code>&lt;blink&gt;</code> tags.</p>

You can write this:

    &#8212; is the decimal-encoded equivalent of &mdash;.

to produce:

    <p><code>&amp;#8212;</code> is the decimal-encoded
    equivalent of <code>&amp;mdash;</code>.</p>



<h3 id="img">Images</h3>

Admittedly, it's fairly difficult to devise a "natural" syntax for
placing images into a plain text document format.

Markdown uses an image syntax that is intended to resemble the syntax
for links, allowing for two styles: *inline* and *reference*.

Inline image syntax looks like this:

    ![Alt text](/path/to/img.jpg)

    ![Alt text](/path/to/img.jpg "Optional title")

That is:

*   An exclamation mark: !;
*   followed by a set of square brackets, containing the alt
    attribute text for the image;
*   followed by a set of parentheses, containing the URL or path to
    the image, and an optional title attribute enclosed in double
    or single quotes.

Reference-style image syntax looks like this:

    ![Alt text][id]

Where "id" is the name of a defined image reference. Image references
are defined using syntax identical to link references:

    [id]: url/to/image  "Optional title attribute"

As of this writing, Markdown has no syntax for specifying the
dimensions of an image; if this is important to you, you can simply
use regular HTML <img> tags.


* * *


<h2 id="misc">Miscellaneous</h2>

<h3 id="autolink">Automatic Links</h3>

Markdown supports a shortcut style for creating "automatic" links for URLs and email addresses: simply surround the URL or email address with angle brackets. What this means is that if you want to show the actual text of a URL or email address, and also have it be a clickable link, you can do this:

    <http://example.com/>
    
Markdown will turn this into:

    <a href="http://example.com/">http://example.com/</a>

Automatic links for email addresses work similarly, except that
Markdown will also perform a bit of randomized decimal and hex
entity-encoding to help obscure your address from address-harvesting
spambots. For example, Markdown will turn this:

    <address@example.com>

into something like this:

    <a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
    &#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
    &#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
    &#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>

which will render in a browser as a clickable link to "address@example.com".

(This sort of entity-encoding trick will indeed fool many, if not
most, address-harvesting bots, but it definitely won't fool all of
them. It's better than nothing, but an address published in this way
will probably eventually start receiving spam.)



<h3 id="backslash">Backslash Escapes</h3>

Markdown allows you to use backslash escapes to generate literal
characters which would otherwise have special meaning in Markdown's
formatting syntax. For example, if you wanted to surround a word with
literal asterisks (instead of an HTML <em> tag), you can backslashes
before the asterisks, like this:

    \*literal asterisks\*

Markdown provides backslash escapes for the following characters:

    \   backslash
       backtick
    *   asterisk
    _   underscore
    {}  curly braces
    []  square brackets
    ()  parentheses
    #   hash mark
	+	plus sign
	-	minus sign (hyphen)
    .   dot
    !   exclamation mark

# Character Escapes

The MD5 value for + is "26b17225b626fb9238849fd60eabdf60".

# HTML Blocks

<p>test</p>

The MD5 value for <p>test</p> is:

6205333b793f34273d75379350b36826* test
+ test
- test

1. test
2. test

* test
+ test
- test

1. test
2. test
> foo
>
> > bar
>
> foo
Valid nesting:

**[Link](url)**

[**Link**](url)

**[**Link**](url)**

Invalid nesting:

[[Link](url)](url)## Unordered

Asterisks tight:

*	asterisk 1
*	asterisk 2
*	asterisk 3


Asterisks loose:

*	asterisk 1

*	asterisk 2

*	asterisk 3

* * *

Pluses tight:

+	Plus 1
+	Plus 2
+	Plus 3


Pluses loose:

+	Plus 1

+	Plus 2

+	Plus 3

* * *


Minuses tight:

-	Minus 1
-	Minus 2
-	Minus 3


Minuses loose:

-	Minus 1

-	Minus 2

-	Minus 3


## Ordered

Tight:

1.	First
2.	Second
3.	Third

and:

1. One
2. Two
3. Three


Loose using tabs:

1.	First

2.	Second

3.	Third

and using spaces:

1. One

2. Two

3. Three

Multiple paragraphs:

1.	Item 1, graf one.

	Item 2. graf two. The quick brown fox jumped over the lazy dog's
	back.
	
2.	Item 2.

3.	Item 3.



## Nested

*	Tab
	*	Tab
		*	Tab

Here's another:

1. First
2. Second:
	* Fee
	* Fie
	* Foe
3. Third

Same thing but with paragraphs:

1. First

2. Second:
	* Fee
	* Fie
	* Foe

3. Third


This was an error in Markdown 1.0.1:

*	this

	*	sub

	that
[Inline link 1 with parens](/url\(test\) "title").

[Inline link 2 with parens](</url\(test\)> "title").

[Inline link 3 with non-escaped parens](/url(test) "title").

[Inline link 4 with non-escaped parens](</url(test)> "title").

[Reference link 1 with parens][1].

[Reference link 2 with parens][2].

  [1]: /url(test) "title"
  [2]: </url(test)> "title"
This tests for a bug where quotes escaped by PHP when using 
preg_replace with the /e modifier must be correctly unescaped
(hence the _UnslashQuotes function found only in PHP Markdown).



Headers below should appear exactly as they are typed (no backslash
added or removed).

Header "quoted\" again \\""
===========================

Header "quoted\" again \\""
---------------------------

### Header "quoted\" again \\"" ###



Test with tabs for _Detab:

	Code	'block'	with	some	"tabs"	and	"quotes"
[Test](/"style="color:red)
[Test](/'style='color:red)

![](/"style="border-color:red;border-size:1px;border-style:solid)
![](/'style='border-color:red;border-size:1px;border-style:solid)
***This is strong and em.***

So is ***this*** word.

___This is strong and em.___

So is ___this___ word.
# Simple tables

Header 1  | Header 2
--------- | ---------
Cell 1    | Cell 2
Cell 3    | Cell 4

With leading pipes:

| Header 1  | Header 2
| --------- | ---------
| Cell 1    | Cell 2
| Cell 3    | Cell 4

With tailing pipes:

Header 1  | Header 2  |
--------- | --------- |
Cell 1    | Cell 2    |
Cell 3    | Cell 4    |

With leading and tailing pipes:

| Header 1  | Header 2  |
| --------- | --------- |
| Cell 1    | Cell 2    |
| Cell 3    | Cell 4    |

* * *

# One-column one-row table

With leading pipes:

| Header
| -------
| Cell

With tailing pipes:

Header  |
------- |
Cell    |

With leading and tailing pipes:

| Header  |
| ------- |
| Cell    |

* * *

Table alignement:

| Default   | Right     |  Center   |     Left  |
| --------- |:--------- |:---------:| ---------:|
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

Table alignement (alternate spacing):

| Default   | Right     |  Center   |     Left  |
| --------- | :-------- | :-------: | --------: |
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

* * * 

# Empty cells

| Header 1  | Header 2  |
| --------- | --------- |
| A         | B         |
| C         |           |

Header 1  | Header 2
--------- | ---------
A         | B
          | D

* * *

# Missing tailing pipe

Header 1  | Header 2  
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- 
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      

* * *

# Too many pipes in rows

| Header 1  | Header 2  |
| --------- 
| Cell      | Cell      | Extra cell? |
| Cell      | Cell      | Extra cell? |

+	this is a list item
	indented with tabs

+   this is a list item
    indented with spaces

Code:

	this code block is indented by one tab

And:

		this code block is indented by two tabs

And:

	+	this is an example list item
		indented with tabs
	
	+   this is an example list item
	    indented with spaces
> A list within a blockquote:
> 
> *	asterisk 1
> *	asterisk 2
> *	asterisk 3
Paragraph and no space:
* ciao

Paragraph and 1 space:
 * ciao

Paragraph and 3 spaces:
  * ciao

Paragraph and 4 spaces:
   * ciao

Paragraph before header:
#Header

Paragraph before blockquote:
>Some quote.
 .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>


As above: checking for bad interractions with the HTML block parser:

 html
<div>


Some *markdown* formatting.

 html
</div>


Some *markdown*


<div>
    <html>



function test();


<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">

<html>
    <title>

</div>

Two code blocks with no blank line between them:


<div>


<div>


Testing *confusion* with markers in the middle:


<div></div>


Testing mixing with title code blocks


<p>
 
<p>

 
<p>

<p>
 

<Fenced>


Code block starting and ending with empty lines:



<Fenced>




Indented code block containing fenced code block sample:

	
	<Fenced>
	

Fenced code block with indented code block sample:


Some text

	Indented code block sample code


Fenced code block with long markers:


Fenced


Fenced code block with fenced code block markers of different length in it:


In code block

Still in code block

Still in code block


Fenced code block with Markdown header and horizontal rule:


#test
---


Fenced code block with link definitions, footnote definition and 
abbreviation definitions:


[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language


* In a list item with smalish indent:

  
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
  
  
With HTML content.
  

<b>bold</b>


Bug with block level elements in this case:

  <div>
  </div>


Indented code block of a fenced code block:

    
	haha!
	

With class:
  
html
<b>bold</b>

  
 html
<b>bold</b>

  
.html
<b>bold</b>

  
 .html
<b>bold</b>


With extra attribute block:

{.html}
<b>bold</b>

  
 {.html #codeid}
<b>bold</b>


 .html{.bold}
<div>

  
 .html {#codeid}
</div>
First line. <br/>
Second line.

This is a first paragraph,
on multiple lines.
     
This is a second paragraph.
There are spaces in between the two.This is a first paragraph,
on multiple lines.

This is a second paragraph
which has multiple lines too.A first paragraph.



A second paragraph after 3 CR (carriage return).This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
     
A few spaces and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
	
1 tab to separate them and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.

A new long long long long long long long long long long long long long long long long paragraph on 1 line.An ampersand & in the text flow is escaped as an html entity.There is an [ampersand](http://validator.w3.org/check?uri=http://www.w3.org/&verbose=1) in the URI.This is \*an asterisk which should stay as is.This is * an asterisk which should stay as is.\\   backslash
\   backtick
\*   asterisk
\_   underscore
\{\}  curly braces
\[\]  square brackets
\(\)  parentheses
\#   hash mark
\+   plus sign
\-   minus sign (hyphen)
\.   dot
\!   exclamation mark> # heading level 1
> 
> paragraph>A blockquote with a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.

>and a second very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.>This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a blockquote.> A blockquote
> on multiple lines
> like this.>A blockquote 
>on multiple lines 
>like this. >A blockquote
>on multiple lines
>like this.
>
>But it has
>two paragraphs.>A blockquote
>on multiple lines
>like this> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.
> This is the first level of quoting.
>
> > This is nested blockquote.> This is the first level of quoting.
> > This is nested blockquote.
> Back to the first level.
> This is the first level of quoting.
> > This is nested blockquote.
	10 PRINT HELLO INFINITE
	20 GOTO 10    10 PRINT < > &
    20 GOTO 10    10 PRINT HELLO INFINITE
    20 GOTO 10# Contributing to Mardown Test Suite

1. [Getting Involved](#getting-involved)
2. [Discussion](#discussion)
3. [How To Report an Issue](#how-to-report-an-issue)
4. [Editing Markdown Specification](#editing-markdown-specification)
5. [Test Suite Guidelines](#test-suite-guidelines)
6. [Pull Request Guidelines](#pull-request-guidelines)

## Getting Involved

There are a number of ways to get involved with the development of the Markdown Test Suite. If you are a first time contributor to an open source project, you can still add value to this project. You may identify grammar issues, write prose, examples or documentation for the project. You may flag some errors and open new issues.

Read all bits of this document and that will guide you on how to participate.

## Discussion

### Mailing List

The Markdown Test Suite has been started a little bit after the start of the [Markdown Community Group](http://www.w3.org/community/markdown/). You may want to discuss about Markdown and this project on the [group mailing-list](http://lists.w3.org/Archives/Public/public-markdown/).

## How to Report an Issue

Don't be afraid to add details to your issue. The more context you give, the better for people participating to the project. Make a short summary, add a description with the context and give links to places which will help to understand.

## Editing Markdown Specification

There is much needed work on the [Markdown Specification](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html). It doesn't require strong competences in coding. Be systematic in the markup and follow the way it is already organized. Each time you added a new atomic section, create a commit for this specific part.

## Test Suite Guidelines

When proposing new tests, make sure they do not already exist in the current test suite. You will notice that there is a separate section dedicated to the specific extensions that some markdown generators have created. Keep them separate. We want to keep the core clean and close to the original specification of Markdown.

If you are not sure, create an issue.

### Markdown Extensions

Markdown extension tests are accepted. Use the following rules:

- place all extension tests under the test/extensions/ENGINE directory with filename equal to the feature name
- for each ENGINE and add a README.markdown under the engine directory with a link to its specification

where ENGINE is either of:

- a command line utility. E.g. pandoc, kramdown.
- a programming API. E.g. Redcarpet::Markdown.new().
- a programmatically accessible web service. E.g.: GFM via the GitHub API.
- a non programmatically accessible web service. E.g.: Stack Overflow flavored markdown.

To avoid test duplication for common features, use the following rules:

- if file tests/extensions/ENGINE/FEATURE.md is empty or not present, use tests/extensions/FEATURE.md instead
- if file tests/extensions/ENGINE/FEATURE.out not present, use tests/extensions/FEATURE.out instead
- for a given ENGINE, only features which have either a .md or a .out are implemented by that engine.
- in case of different outputs for a single feature input, keep directly under extensions/ only the output case that happens across the most engines

**version**

Only the latest stable version of each ENGINE is considered.

**options**

The IO behavior tested is for engine defaults, without any options (command line options, extra JSON parameters, etc.) passed to the engine.

**external state**

Tests that use external state not present in the markdown input shall not be included in this test suite.

For example, what GFM @user user tags render to also depends on the state of GitHub's databases (only render to a link if user exists), not only on the input markdown.

#### Examples

GFM and the "fenced code block" use the following file structure:

    tests/extensions/gfm/README.markdown
    tests/extensions/gfm/fenced-code-block.md
    tests/extensions/gfm/fenced-code-block.out

where README.markdown contains:

    https://help.github.com/articles/github-flavored-markdown

To avoid duplication with other engines, if the input / output (normalized to DOM) is the same across multiple engines use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

If the input is the same, and outputs are DOM different, but represent the same idea (e.g. both represent computer code) use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/gfm/fenced-code-block.out
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

#### New Extensions

Tests are modular, and if you want to test a new engine for your project, that should be easy to do.

If you feel that the new engine is reasonably popular, please send a pull request adding it.

## Commits and Pull Requests

* Keep your commits clean and commented
* Do not mix in one commit different things. Keep modifications related.
* Do not mix everything in one giant pull request. Create separate pull requests for different topic. That will help to have a more meaningful debate about the pull requests and will help to review the code.
* If it relates to a specific issue, add the number of the issue in the commit message.

Thanks for Contributing
as*te*risks*single asterisks*_single underscores_HTML entities are written using ampersand notation: &copy;These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

This is an H1
=============# This is an H1 # # This is an H1# this is an h1 with two trailing spaces  
A new paragraph.# This is an H1This is an H2
-------------## This is an H2 #### This is an H2### This is an H3 ###### This is an H3#### This is an H4 ######## This is an H4##### This is an H5 ########## This is an H5###### This is an H6  ############ This is an H6- - ----***___-------![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 for everyone"![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 logo for everyone")![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png)We love <code> and & for everything We love code for everything We love code for everything The MIT License (MIT)

Copyright (c) 2013 Karl Dubost

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
A first sentence  
and a line break.A first sentence     
and a line break.This is an automatic link <http://www.w3.org/>[W3C](http://www.w3.org/ "Discover w3c")[W3C](http://www.w3.org/)[World Wide Web Consortium][w3c]

[w3c]: <http://www.w3.org/>[World Wide Web Consortium][]

[World Wide Web Consortium]: http://www.w3.org/[w3c][]

[w3c]: http://www.w3.org/[World Wide Web Consortium] [w3c]

[w3c]: http://www.w3.org/[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/
   "Discover W3C"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ (Discover w3c)[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ 'Discover w3c'[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ "Discover w3c"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/*   a list containing a blockquote

    > this the blockquote in the list* a

        b
*   a list containing a block of code

	    10 PRINT HELLO INFINITE
	    20 GOTO 10*   This is a list item with two paragraphs. Lorem ipsum dolor
	sit amet, consectetuer adipiscing elit. Aliquam hendrerit
	mi posuere lectus.

	Vestibulum enim wisi, viverra nec, fringilla in, laoreet
	vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
	sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.*   This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.1\. ordered list escape1. 1

    - inner par list

2. 2
1. list item 1
8. list item 2
1. list item 31. list item 1
2. list item 2
3. list item 3This is a paragraph
on multiple lines
with hard return.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line. This is a paragraph with a trailing and leading space. This is a paragraph with 1 trailing tab.	  This is a paragraph with 2 leading spaces.   This is a paragraph with 3 leading spaces. This is a paragraph with 1 leading space.This is a paragraph with a trailing space. # Colophon - October 1st, 2014

This project was initiated to provide a test suite for Markdown markup, and eventually create a specification from this test results. A part of of the community has started a new endeavor which seems to get traction as [CommonMark](https://github.com/jgm/stmd). **We are then closing this project** and encourage you to contribute to CommonMark. 

The most interesting part of this project would not have been possible without the dedication of [Ciro Santilli](https://github.com/cirosantilli) @cirosantilli. So big applause and thank you to him.


The rest is kept around for archives and references.

# Markdown Test Suite

Inspired by questions on [W3C Markdown Community Group](http://www.w3.org/community/markdown).

Pull Requests are welcome. See the [CONTRIBUTING Guidelines](https://github.com/karlcow/markdown-testsuite/blob/master/CONTRIBUTING.md)

## Design goals

- Comprehensive.
- Small modularized tests.
- Easy to run tests using any programming language. In particular, data representations must have an implementation on all major languages.
- Develop a consensus based markdown specification at [markdown-spec.html](markdown-spec.html). Visualize it [here](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html).

## Test Scripts

Markdown Test Suite already includes tests for many important markdown engines.

To see what the scripts do run:

    ./cat-all.py -h
    ./run-tests.py -h

To configure the scripts do:

	cp config_local.py.example config_local.py

and edit config_local.py. It is already gitignored.

A Vagrantfile is provided with a provision script that installs all installable engines.

Sample output from run-tests.py:

    blackfriday   |......FFF..............FF...F....................................F....................................|   0.93s  102    7   6%
	gfm           |FF.....F.....F...FFFF..F....F........................FFFF...FF...............FF...F.......F...........| 262.88s  102   20  19%
    hoedown       |..............................F.................................................F.....................|   0.36s  102    2   1%
	kramdown      |......FFF.....FF.......FF.......FF.FFFFFFFFFFFFF.......................F..............................|  30.69s  102   23  22%
    lunamark      |FFFFFF.F.FFFFFFFFFFFF.F.....FFFF..FF............FFFFF..FFFFFFFFFF..............F...FFFFFFFFFFF........|   1.58s  103   53  51%
    markdown_pl   |.....................FFFF...............................F...............F.............................|   2.56s  102    6   5%
    markdown2     |......................................................................................................|   5.39s  103    0   0%
    marked        |..............F.................FFFFFFFFFFFFFFFF......................F.F.............................|   6.22s  102   19  18%
    maruku        |......FFF......F.......F.FFF...............................................FF.........................|  37.02s  102   10   9%
    md2html       |.........................FFF...F............................................FF........................|   7.42s  102    6   5%
    multimarkdown |......FFF....FF...F............FFF.FFFFFFFFFFFFF.....FFFF.........F...................................|   0.58s  102   27  26%
    pandoc        |FF...........F.F.FFFF..FFFFF....FF.FFFFFFFFFFFFF.....FFFF.....FF............FFF.FFF..................F|   1.11s  102   41  40%
    peg_markdown  |.................................................................F....................................|   0.46s  102    1   0%
    rdiscount     |.......F.........................................................F....................................|  25.19s  102    3   2%
    redcarpet     |......................................................................................................|  21.49s  102    0   0%
    showdown      |.......................................................................F..............................|   6.85s  102    1   0%

	Extensions:

    blackfriday   |F..|  0.04s    3    1  33%
	gfm           |F.|   2.37s    2    1  50%
    hoedown       |.|    0.00s    1    0   0%
    lunamark      |F.F|  0.05s    3    2  66%
    kramdown      |..|   0.62s    2    0   0%
    markdown_pl   ||     0.00s    0    0   0%
    markdown2     |F.|   0.14s    2    1  50%
    marked        |F.|   0.13s    2    1  50%
    maruku        |F..|  1.06s    3    1  33%
    md2html       |F.|   0.14s    2    0   0%
    multimarkdown |F.|   0.01s    2    1  50%
    pandoc        |F.|   0.02s    2    1  50%
    peg_markdown  |...|  0.02s    3    0   0%
    rdiscount     |F..|   0.74s    3    1  33%
    redcarpet     |..|   0.42s    2    0   0%
    showdown      |F..|  0.20s    3    1  33%

Where F indicates a failing test.

## Other Noticeable Test Suites

We haven't been the first test suite effort. Some projects have maintained their own test suite for a long time. Hopefully we can reach a state where people agree on the terms of what should be a good test suite for all developers.

- [Original test suite](http://daringfireball.net/projects/downloads/MarkdownTest_1.0.zip)
- [PHP markdown test suite:](https://github.com/michelf/mdtest/tree/master/Markdown.mdtest)
- [Markdown-js test suite](https://github.com/evilstreak/markdown-js/tree/master/test/features)
- [Python markdown 2 test suite](https://github.com/trentm/python-markdown2/tree/master/test/tm-cases)
- [multimarkdown test suite](https://github.com/fletcher/MMD-Test-Suite)
- [John MacFarlane's Standard Markdown spec](https://github.com/jgm/stmd)

In addition we should note the [wonderful work](http://johnmacfarlane.net/babelmark2/) made by John Mac Farlane. The Web service output the differences in between the different markdown implementations. It helps a lot when searching on the most common output.
as**te**risks**double asterisks**__double underscores__* list item 1
* list item 2
* list item 3
- list item 1
- list item 2
- list item 3 * list item 1
 * list item 2
 * list item 3  * list item 1
  * list item 2
  * list item 3   * list item 1
   * list item 2
   * list item 3+ list item 1
+ list item 2
+ list item 3* list item in paragraph

* another list item in paragraph*   This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a list.
*   and yet another long long long long long long long long long long long long long long long long long long long long long long line.*   This is a list item
    with the content on
    multiline and indented.
*   And this another list item
    with the same principle.€Some text about HTML, SGML and HTML4.

Let's talk about the U.S.A., (É.U. or É.-U. d'A. in French).

*[HTML4]: Hyper Text Markup Language version 4
*[HTML]: Hyper Text Markup Language
*[SGML]: Standard Generalized Markup Language
*[U.S.A.]: United States of America
*[É.U.] : États-Unis d'Amérique
*[É.-U. d'A.] : États-Unis d'Amérique

And here we have a CD, some CDs, and some other CD's.

*[CD]: Compact Disk

Let's transfert documents through TCP/IP, using TCP packets.

*[IP]: Internet Protocol
*[TCP]: Transmission Control Protocol

 ---

Bienvenue sur [CMS](http://www.bidulecms.com "Bidule CMS").

*[CMS]: Content Management System

 ---

ATCCE

*[ATCCE]: Abbreviation "Testing" Correct 'Character' < Escapes >* one
* two

1. three
2. four

* one
* two
1. three
2. fourAT&T has an ampersand in their name.

AT&amp;T is another way to write it.

This & that.

4 < 5.

6 > 5.

Here's a [link] [1] with an ampersand in the URL.

Here's a link with an amersand in the link text: [AT&T] [2].

Here's an inline [link](/script?foo=1&bar=2).

Here's an inline [link](</script?foo=1&bar=2>).


[1]: http://example.com/?foo=1&bar=2
[2]: http://att.com/  "AT&T"Link: <http://example.com/>.

With an ampersand: <http://example.com/?foo=1&bar=2>

* In a list?
* <http://example.com/>
* It should.

> Blockquoted: <http://example.com/>

Auto-links should not occur here: <http://example.com/>

	or here: <http://example.com/>These should all get escaped:

Backslash: \\

Backtick: \

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-



These should not, because they occur within a code block:

	Backslash: \\

	Backtick: \

	Asterisk: \*

	Underscore: \_

	Left brace: \{

	Right brace: \}

	Left bracket: \[

	Right bracket: \]

	Left paren: \(

	Right paren: \)

	Greater-than: \>

	Hash: \#

	Period: \.

	Bang: \!

	Plus: \+

	Minus: \-


Nor should these, which occur in code spans:

Backslash: \\

Backtick:   \  

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-


These should get escaped, even though they're matching pairs for
other Markdown constructs:

\*asterisks\*

\_underscores\_

\backticks\

This is a code span with a literal backslash-backtick sequence:   \  

This is a tag with unescaped backticks <span attr='ticks'>bar</span>.

This is a tag with backslashes <span attr='\\backslashes\\'>bar</span>.
  .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>
 

As above: checking for bad interractions with the HTML block parser:

  html
<div>
 

Some *markdown* formatting.

  html
</div>
 

Some *markdown*

 
<div>
    <html>
 

 
function test();
 

<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">
 
<html>
    <title>
 
</div>

Two code blocks with no blank line between them:

 
<div>
 
 
<div>
 

Testing *confusion* with code spans at the HTML block parser:

 
<div></div>
 

Testing mixing with title code blocks

 
<p>

<p>
 

<p>
 
<p>

 
<Fenced>
 

Code block starting and ending with empty lines:
 


<Fenced>


 

Indented code block containing fenced code block sample:

	 
	<Fenced>
	 

Fenced code block with indented code block sample:

 
Some text

	Indented code block sample code
 

Fenced code block with long markers:

 
Fenced
 

Fenced code block with fenced code block markers of different length in it:

 
In code block
 
Still in code block
 
Still in code block
 

Fenced code block with Markdown header and horizontal rule:

 
#test
---
 

Fenced code block with link definitions, footnote definition and
abbreviation definitions:

 
[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language
 

* In a list item with smalish indent:

   
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
   

With HTML content.

 
<b>bold</b>
 

Bug with block level elements in this case:
 
  <div>
  </div>
 

Indented code block of a fenced code block:

     
	haha!
	 

With class:

 html
<b>bold</b>
 

  html
<b>bold</b>
 

 .html
<b>bold</b>
 

  .html
<b>bold</b>
 

With extra attribute block:

 {.html}
<b>bold</b>
 

  {.html #codeid}
<b>bold</b>
 

  .html{.bold}
<div>
 
  
  .html {#codeid}
</div>
 > Example:
> 
>     sub status {
>         print "working";
>     }
> 
> Or:
> 
>     sub status {
>         return "working";
>     }

*	List Item:

		code block

		with a blank line

	within a list item.

*       code block
        as first element of a list item

*	List Item:
	
		code block with whitespace on preceding line
    Codeblock on second line
    <?php
    echo "hello!";
    ?>

foo bar

    <?php
    echo "hello!";

lorem ipsum

    echo "hello!";
    ?>
    
lorem ipsum	code block on the first line
	
Regular text.

    code block indented by spaces

Regular text.

	the lines in this block  
	all contain trailing spaces  

Regular Text.

	code block on the last line<test a=" content of attribute ">

Fix for backticks within HTML tag: <span attr='ticks'>like this</span>

Here's how you put   backticks   in a code span.A simple definition list:

Term 1
:   Definition 1

Term 2
:   Definition 2

With multiple terms:

Term 1
Term 2
:   Definition 1

Term 3
Term 4
:   Definition 2

With multiple definitions:

Term 1
:   Definition 1
:   Definition 2

Term 2
:   Definition 3
:   Definition 4

With multiple lines per definition:

Term 1
:   Definition 1 line 1 ...
Definition 1 line 2
:   Definition 2 line 1 ...
Definition 2 line 2

Term 2
:   Definition 3 line 2 ...
    Definition 3 line 2
:   Definition 4 line 2 ...
    Definition 4 line 2

With paragraphs:

Term 1

:   Definition 1 (paragraph)

Term 2

:   Definition 2 (paragraph)

With multiple paragraphs:

Term 1

:   Definition 1 paragraph 1 line 1 ...
	Definition 1 paragraph 1 line 2

    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)

    Definition 1 paragraph 2 line 1 ...
Definition 1 paragraph 2 line 2 (lazy)

* * *

A mix:

Term 1
Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)
    
    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

:   Definition 2 paragraph 1 line 1 ...
Definition 2 paragraph 1 line 2 (lazy)

Term 3
:   Definition 3 (no paragraph)
:   Definition 4 (no paragraph)
:   Definition 5 line 1 ...
    Definition 5 line 2 (no paragraph)

:   Definition 6 paragraph 1 line 1 ...
Definition 6 paragraph 1 line 2
:   Definition 7 (no paragraph)
:   Definition 8 paragraph 1 line 1 (forced paragraph) ...
    Definition 8 paragraph 1 line 2
    
    Definition 8 paragraph 2 line 1
    
Term 4
:   Definition 9 paragraph 1 line 1 (forced paragraph) ...
    Definition 9 paragraph 1 line 2
    
    Definition 9 paragraph 2 line 1
:   Definition 10 (no paragraph)

* * *

Special cases:

Term

:       code block
        as first element of a definition<michel.fortin@michelf.ca>

International domain names: <help@tūdaliņ.lv>


## Some weird valid email addresses

<abc.123@example.com>

<1234567890@example.com>

<_______@example.com>

<abc+mailbox/department=shipping@example.com>

<!#$%&'*+-/=?^_.{|}@example.com> (all of these characters are allowed)

<"abc@def"@example.com> (anything goes inside quotation marks)

<"Fred Bloggs"@example.com>

<jsmith@[192.0.2.1]>

<"A"@example.com>Combined emphasis:

1.  ***test test***
2.  ___test test___
3.  *test **test***
4.  **test *test***
5.  ***test* test**
6.  ***test** test*
7.  ***test* test**
8.  **test *test***
9.  *test **test***
10. _test __test___
11. __test _test___
12. ___test_ test__
13. ___test__ test_
14. ___test_ test__
15. __test _test___
16. _test __test___
17. *test __test__*
18. **test _test_**
19. **_test_ test**
20. *__test__ test*
21. **_test_ test**
22. **test _test_**
23. *test __test__*
24. _test **test**_
25. __test *test*__
26. __*test* test__
27. _**test** test_
28. __*test* test__
29. __test *test*__
30. _test **test**_


Incorrect nesting:

1.  *test  **test*  test**
2.  _test  __test_  test__
3.  **test  *test** test*
4.  __test  _test__ test_
5.  *test   *test*  test*
6.  _test   _test_  test_
7.  **test **test** test**
8.  __test __test__ test__
9. _**some text_**
10. *__some text*__
11. **_some text**_
12. *__some text*__

No emphasis:

1.  test*  test  *test
2.  test** test **test
3.  test_  test  _test
4.  test__ test __test



Middle-word emphasis (asterisks):

1.  *a*b
2.   a*b*
3.   a*b*c
4. **a**b
5.   a**b**
6.   a**b**c


Middle-word emphasis (underscore):

1.  _a_b
2.   a_b_
3.   a_b_c
4. __a__b
5.   a__b__
6.   a__b__c

my_precious_file.txt


## Tricky Cases

E**. **Test** TestTestTest

E**. **Test** Test Test Test


## Overlong emphasis

Name: ____________  
Organization: ____  
Region/Country: __

_____Cut here_____

____Cut here____

# Regression

_**Note**_: This _is emphasis_.
With asterisks

 * List item
 *
 * List item

With numbers

1. List item
2.
3. List item

With hyphens

- List item
-
- List item

With asterisks

 * List item
 * List item
 *

With numbers

1. List item
2. List item
3.

With hyphens

- List item
- List item
-
This is the first paragraph.[^first]

[^first]:  This is the first note.

* List item one.[^second]
* List item two.[^third]

[^third]: This is the third note, defined out of order.
[^second]: This is the second note.
[^fourth]: This is the fourth note.

# Header[^fourth]

Some paragraph with a footnote[^1], and another[^2].

[^1]: Content for fifth footnote.
[^2]: Content for sixth footnote spaning on 
    three lines, with some span-level markup like
    _emphasis_, a [link][].

[link]: http://michelf.ca/

Another paragraph with a named footnote[^fn-name].

[^fn-name]:
    Footnote beginning on the line next to the marker.

This paragraph should not have a footnote marker since 
the footnote is undefined.[^3]

This paragraph has a second footnote marker to footnote number one.[^1]

This paragraph links to a footnote with plenty of 
block-level content.[^block]

[^block]:
	Paragraph.
	
	*   List item
	
	> Blockquote
	
	    Code block

This paragraph host the footnote reference within a 
footnote test[^reference].

[^reference]:
	This footnote has a footnote of its own.[^nested]

[^nested]:
	This footnote should appear even though it is referenced
	from another footnote. But [^reference] should be litteral
	since the footnote with that name has already been used.

 - - -

Testing unusual footnote name[^1$^!"'].

[^1$^!"']: Haha!

 - - -
 
Footnotes mixed with images[^image-mixed]
![1800 Travel][img6]
![1830 Travel][img7]

[img6]: images/MGR-1800-travel.jpeg "Travel Speeds in 1800"
[^image-mixed]: Footnote Content
[img7]: images/MGR-1830-travel.jpeg "Travel Speeds in 1830"
In Markdown 1.0.0 and earlier. Version
8. This line turns into a list item.
Because a hard-wrapped line in the
middle of a paragraph looked like a
list item.

Here's one with a bullet.
* criminey.
Header  {#id1}
======

Header  { #id2}
------

### Header  {#id3 }
#### Header ##  { #id4 }

 - - -

Header  {.cl}
======

Header  { .cl}
------

### Header  {.cl }
#### Header ##  { .cl }

 - - -

Header  {.cl.class}
======

Header  { .cl .class}
------

### Header  {.cl .class }
#### Header ##  { .cl.class }

 - - -

Header  {#id5.cl.class}
======

Header  { #id6 .cl .class}
------

### Header  {.cl.class#id7 }
#### Header ##  { .cl.class#id8 }
Header
======

Header
------

### Header

 - - -

Header
======
Paragraph

Header
------
Paragraph

### Header
Paragraph

 - - -

Paragraph
Header
======
Paragraph

Paragraph
Header
------
Paragraph

Paragraph
### Header
ParagraphDashes:

---

 ---
 
  ---

   ---

	---

- - -

 - - -
 
  - - -

   - - -

	- - -


Asterisks:

***

 ***
 
  ***

   ***

	***

* * *

 * * *
 
  * * *

   * * *

	* * *


Underscores:

___

 ___
 
  ___

   ___

    ___

_ _ _

 _ _ _
 
  _ _ _

   _ _ _

    _ _ _
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")

Inline within a paragraph: [alt text](/url/).

![alt text](/url/  "title preceded by two spaces")

![alt text](/url/  "title has spaces afterward"  )

![alt text](</url/>)

![alt text](</url/> "with a title").

![Empty]()

![this is a stupid URL](http://example.com/(parens).jpg)


![alt text][foo]

  [foo]: /url/

![alt text][bar]

  [bar]: /url/ "Title here"Simple block on one line:

<div>foo</div>

And nested without indentation:

<div>
<div>
<div>
foo
</div>
<div style=">"/>
</div>
<div>bar</div>
</div>

And with attributes:

<div>
	<div id="foo">
	</div>
</div>

This was broken in 1.0.2b7:

<div class="inlinepage">
<div class="toggleableend">
foo
</div>
</div>
Here's a simple block:

<div>
	foo
</div>

This should be a code block, though:

	<div>
		foo
	</div>

As should this:

	<div>foo</div>

Now, nested:

<div>
	<div>
		<div>
			foo
		</div>
	</div>
</div>

This should just be an HTML comment:

<!-- Comment -->

Multiline:

<!--
Blah
Blah
-->

Code block:

	<!-- Comment -->

Just plain comment, with trailing spaces on the line:

<!-- foo -->   

Code:

	<hr />
	
Hr's:

<hr>

<hr/>

<hr />

<hr>   

<hr/>  

<hr /> 

<hr class="foo" id="bar" />

<hr class="foo" id="bar"/>

<hr class="foo" id="bar" >

<abbr title=" **Attribute Content Is Not A Code Span** ">ACINACS</abbr>

<abbr title="first backtick!">SB</abbr> 
<abbr title="second backtick!">SB</abbr>Paragraph one.

<!-- This is a simple comment -->

<!--
	This is another comment.
-->

Paragraph two.

<!-- one comment block -- -- with two comments -->

The end.
# Markdown inside code blocks

<div markdown="1">
foo
</div>

<div markdown='1'>
foo
</div>

<div markdown=1>
foo
</div>

<table>
<tr><td markdown="1">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="span">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="block">test _emphasis_ (block)</td></tr>
</table>

## More complicated

<table>
<tr><td markdown="1">
* this is _not_ a list item</td></tr>
<tr><td markdown="span">
* this is _not_ a list item</td></tr>
<tr><td markdown="block">
* this _is_ a list item
</td></tr>
</table>

## With indent

<div>
    <div markdown="1">
    This text is no code block: if it was, the 
    closing <div> would be too and the HTML block 
    would be invalid.

    Markdown content in HTML blocks is assumed to be 
    indented the same as the block opening tag.

    **This should be the third paragraph after the header.**
    </div>
</div>

## Code block with rogue </div>s in Markdown code span and block

<div>
    <div markdown="1">

    This is a code block however:

        </div>

    Funny isn't it? Here is a code span: </div>.

    </div>
</div>

<div>
  <div markdown="1">
    * List item, not a code block

Some text

      This is a code block.
  </div>
</div>

## No code block in markdown span mode

<p markdown="1">
    This is not a code block since Markdown parse paragraph 
    content as span. Code spans like </p> are allowed though.
</p>

<p markdown="1">_Hello_ _world_</p>

## Preserving attributes and tags on more than one line:

<p class="test" markdown="1" 
id="12">
Some _span_ content.
</p>


## Header confusion bug

<table class="canvas">
<tr>
<td id="main" markdown="1">Hello World!
============

Hello World!</td>
</tr>
</table>
Here is a block tag ins:

<ins>
<p>Some text</p>
</ins>

<ins>And here it is inside a paragraph.</ins>

And here it is <ins>in the middle of</ins> a paragraph.

<del>
<p>Some text</p>
</del>

<del>And here is ins as a paragraph.</del>

And here it is <del>in the middle of</del> a paragraph.
		    GNU GENERAL PUBLIC LICENSE
		       Version 2, June 1991

 Copyright (C) 1989, 1991 Free Software Foundation, Inc.,
 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

			    Preamble

  The licenses for most software are designed to take away your
freedom to share and change it.  By contrast, the GNU General Public
License is intended to guarantee your freedom to share and change free
software--to make sure the software is free for all its users.  This
General Public License applies to most of the Free Software
Foundation's software and to any other program whose authors commit to
using it.  (Some other Free Software Foundation software is covered by
the GNU Lesser General Public License instead.)  You can apply it to
your programs, too.

  When we speak of free software, we are referring to freedom, not
price.  Our General Public Licenses are designed to make sure that you
have the freedom to distribute copies of free software (and charge for
this service if you wish), that you receive source code or can get it
if you want it, that you can change the software or use pieces of it
in new free programs; and that you know you can do these things.

  To protect your rights, we need to make restrictions that forbid
anyone to deny you these rights or to ask you to surrender the rights.
These restrictions translate to certain responsibilities for you if you
distribute copies of the software, or if you modify it.

  For example, if you distribute copies of such a program, whether
gratis or for a fee, you must give the recipients all the rights that
you have.  You must make sure that they, too, receive or can get the
source code.  And you must show them these terms so they know their
rights.

  We protect your rights with two steps: (1) copyright the software, and
(2) offer you this license which gives you legal permission to copy,
distribute and/or modify the software.

  Also, for each author's protection and ours, we want to make certain
that everyone understands that there is no warranty for this free
software.  If the software is modified by someone else and passed on, we
want its recipients to know that what they have is not the original, so
that any problems introduced by others will not reflect on the original
authors' reputations.

  Finally, any free program is threatened constantly by software
patents.  We wish to avoid the danger that redistributors of a free
program will individually obtain patent licenses, in effect making the
program proprietary.  To prevent this, we have made it clear that any
patent must be licensed for everyone's free use or not licensed at all.

  The precise terms and conditions for copying, distribution and
modification follow.

		    GNU GENERAL PUBLIC LICENSE
   TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

  0. This License applies to any program or other work which contains
a notice placed by the copyright holder saying it may be distributed
under the terms of this General Public License.  The "Program", below,
refers to any such program or work, and a "work based on the Program"
means either the Program or any derivative work under copyright law:
that is to say, a work containing the Program or a portion of it,
either verbatim or with modifications and/or translated into another
language.  (Hereinafter, translation is included without limitation in
the term "modification".)  Each licensee is addressed as "you".

Activities other than copying, distribution and modification are not
covered by this License; they are outside its scope.  The act of
running the Program is not restricted, and the output from the Program
is covered only if its contents constitute a work based on the
Program (independent of having been made by running the Program).
Whether that is true depends on what the Program does.

  1. You may copy and distribute verbatim copies of the Program's
source code as you receive it, in any medium, provided that you
conspicuously and appropriately publish on each copy an appropriate
copyright notice and disclaimer of warranty; keep intact all the
notices that refer to this License and to the absence of any warranty;
and give any other recipients of the Program a copy of this License
along with the Program.

You may charge a fee for the physical act of transferring a copy, and
you may at your option offer warranty protection in exchange for a fee.

  2. You may modify your copy or copies of the Program or any portion
of it, thus forming a work based on the Program, and copy and
distribute such modifications or work under the terms of Section 1
above, provided that you also meet all of these conditions:

    a) You must cause the modified files to carry prominent notices
    stating that you changed the files and the date of any change.

    b) You must cause any work that you distribute or publish, that in
    whole or in part contains or is derived from the Program or any
    part thereof, to be licensed as a whole at no charge to all third
    parties under the terms of this License.

    c) If the modified program normally reads commands interactively
    when run, you must cause it, when started running for such
    interactive use in the most ordinary way, to print or display an
    announcement including an appropriate copyright notice and a
    notice that there is no warranty (or else, saying that you provide
    a warranty) and that users may redistribute the program under
    these conditions, and telling the user how to view a copy of this
    License.  (Exception: if the Program itself is interactive but
    does not normally print such an announcement, your work based on
    the Program is not required to print an announcement.)

These requirements apply to the modified work as a whole.  If
identifiable sections of that work are not derived from the Program,
and can be reasonably considered independent and separate works in
themselves, then this License, and its terms, do not apply to those
sections when you distribute them as separate works.  But when you
distribute the same sections as part of a whole which is a work based
on the Program, the distribution of the whole must be on the terms of
this License, whose permissions for other licensees extend to the
entire whole, and thus to each and every part regardless of who wrote it.

Thus, it is not the intent of this section to claim rights or contest
your rights to work written entirely by you; rather, the intent is to
exercise the right to control the distribution of derivative or
collective works based on the Program.

In addition, mere aggregation of another work not based on the Program
with the Program (or with a work based on the Program) on a volume of
a storage or distribution medium does not bring the other work under
the scope of this License.

  3. You may copy and distribute the Program (or a work based on it,
under Section 2) in object code or executable form under the terms of
Sections 1 and 2 above provided that you also do one of the following:

    a) Accompany it with the complete corresponding machine-readable
    source code, which must be distributed under the terms of Sections
    1 and 2 above on a medium customarily used for software interchange; or,

    b) Accompany it with a written offer, valid for at least three
    years, to give any third party, for a charge no more than your
    cost of physically performing source distribution, a complete
    machine-readable copy of the corresponding source code, to be
    distributed under the terms of Sections 1 and 2 above on a medium
    customarily used for software interchange; or,

    c) Accompany it with the information you received as to the offer
    to distribute corresponding source code.  (This alternative is
    allowed only for noncommercial distribution and only if you
    received the program in object code or executable form with such
    an offer, in accord with Subsection b above.)

The source code for a work means the preferred form of the work for
making modifications to it.  For an executable work, complete source
code means all the source code for all modules it contains, plus any
associated interface definition files, plus the scripts used to
control compilation and installation of the executable.  However, as a
special exception, the source code distributed need not include
anything that is normally distributed (in either source or binary
form) with the major components (compiler, kernel, and so on) of the
operating system on which the executable runs, unless that component
itself accompanies the executable.

If distribution of executable or object code is made by offering
access to copy from a designated place, then offering equivalent
access to copy the source code from the same place counts as
distribution of the source code, even though third parties are not
compelled to copy the source along with the object code.

  4. You may not copy, modify, sublicense, or distribute the Program
except as expressly provided under this License.  Any attempt
otherwise to copy, modify, sublicense or distribute the Program is
void, and will automatically terminate your rights under this License.
However, parties who have received copies, or rights, from you under
this License will not have their licenses terminated so long as such
parties remain in full compliance.

  5. You are not required to accept this License, since you have not
signed it.  However, nothing else grants you permission to modify or
distribute the Program or its derivative works.  These actions are
prohibited by law if you do not accept this License.  Therefore, by
modifying or distributing the Program (or any work based on the
Program), you indicate your acceptance of this License to do so, and
all its terms and conditions for copying, distributing or modifying
the Program or works based on it.

  6. Each time you redistribute the Program (or any work based on the
Program), the recipient automatically receives a license from the
original licensor to copy, distribute or modify the Program subject to
these terms and conditions.  You may not impose any further
restrictions on the recipients' exercise of the rights granted herein.
You are not responsible for enforcing compliance by third parties to
this License.

  7. If, as a consequence of a court judgment or allegation of patent
infringement or for any other reason (not limited to patent issues),
conditions are imposed on you (whether by court order, agreement or
otherwise) that contradict the conditions of this License, they do not
excuse you from the conditions of this License.  If you cannot
distribute so as to satisfy simultaneously your obligations under this
License and any other pertinent obligations, then as a consequence you
may not distribute the Program at all.  For example, if a patent
license would not permit royalty-free redistribution of the Program by
all those who receive copies directly or indirectly through you, then
the only way you could satisfy both it and this License would be to
refrain entirely from distribution of the Program.

If any portion of this section is held invalid or unenforceable under
any particular circumstance, the balance of the section is intended to
apply and the section as a whole is intended to apply in other
circumstances.

It is not the purpose of this section to induce you to infringe any
patents or other property right claims or to contest validity of any
such claims; this section has the sole purpose of protecting the
integrity of the free software distribution system, which is
implemented by public license practices.  Many people have made
generous contributions to the wide range of software distributed
through that system in reliance on consistent application of that
system; it is up to the author/donor to decide if he or she is willing
to distribute software through any other system and a licensee cannot
impose that choice.

This section is intended to make thoroughly clear what is believed to
be a consequence of the rest of this License.

  8. If the distribution and/or use of the Program is restricted in
certain countries either by patents or by copyrighted interfaces, the
original copyright holder who places the Program under this License
may add an explicit geographical distribution limitation excluding
those countries, so that distribution is permitted only in or among
countries not thus excluded.  In such case, this License incorporates
the limitation as if written in the body of this License.

  9. The Free Software Foundation may publish revised and/or new versions
of the General Public License from time to time.  Such new versions will
be similar in spirit to the present version, but may differ in detail to
address new problems or concerns.

Each version is given a distinguishing version number.  If the Program
specifies a version number of this License which applies to it and "any
later version", you have the option of following the terms and conditions
either of that version or of any later version published by the Free
Software Foundation.  If the Program does not specify a version number of
this License, you may choose any version ever published by the Free Software
Foundation.

  10. If you wish to incorporate parts of the Program into other free
programs whose distribution conditions are different, write to the author
to ask for permission.  For software which is copyrighted by the Free
Software Foundation, write to the Free Software Foundation; we sometimes
make exceptions for this.  Our decision will be guided by the two goals
of preserving the free status of all derivatives of our free software and
of promoting the sharing and reuse of software generally.

			    NO WARRANTY

  11. BECAUSE THE PROGRAM IS LICENSED FREE OF CHARGE, THERE IS NO WARRANTY
FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW.  EXCEPT WHEN
OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES
PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED
OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.  THE ENTIRE RISK AS
TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU.  SHOULD THE
PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING,
REPAIR OR CORRECTION.

  12. IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING
WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MAY MODIFY AND/OR
REDISTRIBUTE THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES,
INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING
OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED
TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY
YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER
PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES.

		     END OF TERMS AND CONDITIONS

	    How to Apply These Terms to Your New Programs

  If you develop a new program, and you want it to be of the greatest
possible use to the public, the best way to achieve this is to make it
free software which everyone can redistribute and change under these terms.

  To do so, attach the following notices to the program.  It is safest
to attach them to the start of each source file to most effectively
convey the exclusion of warranty; and each file should have at least
the "copyright" line and a pointer to where the full notice is found.

    <one line to give the program's name and a brief idea of what it does.>
    Copyright (C) <year>  <name of author>

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

Also add information on how to contact you by electronic and paper mail.

If the program is interactive, make it output a short notice like this
when it starts in an interactive mode:

    Gnomovision version 69, Copyright (C) year name of author
    Gnomovision comes with ABSOLUTELY NO WARRANTY; for details type show w'.
    This is free software, and you are welcome to redistribute it
    under certain conditions; type show c' for details.

The hypothetical commands show w' and show c' should show the appropriate
parts of the General Public License.  Of course, the commands you use may
be called something other than show w' and show c'; they could even be
mouse-clicks or menu items--whatever suits your program.

You should also get your employer (if you work as a programmer) or your
school, if any, to sign a "copyright disclaimer" for the program, if
necessary.  Here is a sample; alter the names:

  Yoyodyne, Inc., hereby disclaims all copyright interest in the program
  Gnomovision' (which makes passes at compilers) written by James Hacker.

  <signature of Ty Coon>, 1 April 1989
  Ty Coon, President of Vice

This General Public License does not permit incorporating your program into
proprietary programs.  If your program is a subroutine library, you may
consider it more useful to permit linking proprietary applications with the
library.  If this is what you want to do, use the GNU Lesser General
Public License instead of this License.
This is an [inline link](/url "title"){.class #inline-link}.

This is a [reference link][refid].

This is an ![inline image](/img "title"){.class #inline-img}.

This is a ![reference image][refid].

[refid]: /path/to/something (Title) { .class #ref data-key=val }

Just a [URL](/url/).

[URL and title](/url/ "title").

[URL and title](/url/  "title preceded by two spaces").

[URL and title](/url/	"title preceded by a tab").

[URL and title](/url/ "title has spaces afterward"  ).

[URL wrapped in angle brackets](</url/>).

[URL w/ angle brackets + title](</url/> "Here's the title").

[Empty]().

[With parens in the URL](http://en.wikipedia.org/wiki/WIMP_(computing))

(With outer parens and [parens in url](/foo(bar)))


[With parens in the URL](/foo(bar) "and a title")

(With outer parens and [parens in url](/foo(bar) "and a title"))
Foo [bar] [1].

Foo [bar][1].

Foo [bar]
[1].

[1]: /url/  "Title"


With [embedded [brackets]] [b].


Indented [once][].

Indented [twice][].

Indented [thrice][].

Indented [four][] times.

 [once]: /url

  [twice]: /url

   [thrice]: /url

    [four]: /url


[b]: /url/

* * *

[this] [this] should work

So should [this][this].

And [this] [].

And [this][].

And [this].

But not [that] [].

Nor [that][].

Nor [that].

[Something in brackets like [this][] should work]

[Same with [this].]

In this case, [this](/somethingelse/) points to something else.

Backslashing should suppress \[this] and [this\].

[this]: foo


* * *

Here's one where the [link
breaks] across lines.

Here's another where the [link 
breaks] across lines, but with a line-ending space.


[link breaks]: /url/
This is the [simple case].

[simple case]: /simple



This one has a [line
break].

This one has a [line 
break] with a line-ending space.

[line break]: /foo


[this] [that] and the [other]

[this]: /this
[that]: /that
[other]: /other
Foo [bar][].

Foo [bar](/url/ "Title with "quotes" inside").


  [bar]: /url/ "Title with "quotes" inside"

Markdown: Basics
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a class="selected" title="Markdown Basics">Basics</a></li>
    <li><a href="/projects/markdown/syntax" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


Getting the Gist of Markdown's Formatting Syntax
------------------------------------------------

This page offers a brief overview of what it's like to use Markdown.
The [syntax page] [s] provides complete, detailed documentation for
every feature, but Markdown should be very easy to pick up simply by
looking at a few examples of it in action. The examples on this page
are written in a before/after style, showing example syntax and the
HTML output produced by Markdown.

It's also helpful to simply try Markdown out; the [Dingus] [d] is a
web application that allows you type your own Markdown-formatted text
and translate it to XHTML.

**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL] [src].

  [s]: /projects/markdown/syntax  "Markdown Syntax"
  [d]: /projects/markdown/dingus  "Markdown Dingus"
  [src]: /projects/markdown/basics.text


## Paragraphs, Headers, Blockquotes ##

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

Markdown offers two styles of headers: *Setext* and *atx*.
Setext-style headers for <h1> and <h2> are created by
"underlining" with equal signs (=) and hyphens (-), respectively.
To create an atx-style header, you put 1-6 hash marks (#) at the
beginning of the line -- the number of hashes equals the resulting
HTML header level.

Blockquotes are indicated using email-style '>' angle brackets.

Markdown:

    A First Level Header
    ====================
    
    A Second Level Header
    ---------------------

    Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.

    The quick brown fox jumped over the lazy
    dog's back.
    
    ### Header 3

    > This is a blockquote.
    > 
    > This is the second paragraph in the blockquote.
    >
    > ## This is an H2 in a blockquote


Output:

    <h1>A First Level Header</h1>
    
    <h2>A Second Level Header</h2>
    
    <p>Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.</p>
    
    <p>The quick brown fox jumped over the lazy
    dog's back.</p>
    
    <h3>Header 3</h3>
    
    <blockquote>
        <p>This is a blockquote.</p>
        
        <p>This is the second paragraph in the blockquote.</p>
        
        <h2>This is an H2 in a blockquote</h2>
    </blockquote>



### Phrase Emphasis ###

Markdown uses asterisks and underscores to indicate spans of emphasis.

Markdown:

    Some of these words *are emphasized*.
    Some of these words _are emphasized also_.
    
    Use two asterisks for **strong emphasis**.
    Or, if you prefer, __use two underscores instead__.

Output:

    <p>Some of these words <em>are emphasized</em>.
    Some of these words <em>are emphasized also</em>.</p>
    
    <p>Use two asterisks for <strong>strong emphasis</strong>.
    Or, if you prefer, <strong>use two underscores instead</strong>.</p>
   


## Lists ##

Unordered (bulleted) lists use asterisks, pluses, and hyphens (*,
+, and -) as list markers. These three markers are
interchangable; this:

    *   Candy.
    *   Gum.
    *   Booze.

this:

    +   Candy.
    +   Gum.
    +   Booze.

and this:

    -   Candy.
    -   Gum.
    -   Booze.

all produce the same output:

    <ul>
    <li>Candy.</li>
    <li>Gum.</li>
    <li>Booze.</li>
    </ul>

Ordered (numbered) lists use regular numbers, followed by periods, as
list markers:

    1.  Red
    2.  Green
    3.  Blue

Output:

    <ol>
    <li>Red</li>
    <li>Green</li>
    <li>Blue</li>
    </ol>

If you put blank lines between items, you'll get <p> tags for the
list item text. You can create multi-paragraph list items by indenting
the paragraphs by 4 spaces or 1 tab:

    *   A list item.
    
        With multiple paragraphs.

    *   Another item in the list.

Output:

    <ul>
    <li><p>A list item.</p>
    <p>With multiple paragraphs.</p></li>
    <li><p>Another item in the list.</p></li>
    </ul>
    


### Links ###

Markdown supports two styles for creating links: *inline* and
*reference*. With both styles, you use square brackets to delimit the
text you want to turn into a link.

Inline-style links use parentheses immediately after the link text.
For example:

    This is an [example link](http://example.com/).

Output:

    <p>This is an <a href="http://example.com/">
    example link</a>.</p>

Optionally, you may include a title attribute in the parentheses:

    This is an [example link](http://example.com/ "With a Title").

Output:

    <p>This is an <a href="http://example.com/" title="With a Title">
    example link</a>.</p>

Reference-style links allow you to refer to your links by names, which
you define elsewhere in your document:

    I get 10 times more traffic from [Google][1] than from
    [Yahoo][2] or [MSN][3].

    [1]: http://google.com/        "Google"
    [2]: http://search.yahoo.com/  "Yahoo Search"
    [3]: http://search.msn.com/    "MSN Search"

Output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from <a href="http://search.yahoo.com/"
    title="Yahoo Search">Yahoo</a> or <a href="http://search.msn.com/"
    title="MSN Search">MSN</a>.</p>

The title attribute is optional. Link names may contain letters,
numbers and spaces, but are *not* case sensitive:

    I start my morning with a cup of coffee and
    [The New York Times][NY Times].

    [ny times]: http://www.nytimes.com/

Output:

    <p>I start my morning with a cup of coffee and
    <a href="http://www.nytimes.com/">The New York Times</a>.</p>


### Images ###

Image syntax is very much like link syntax.

Inline (titles are optional):

    ![alt text](/path/to/img.jpg "Title")

Reference-style:

    ![alt text][id]

    [id]: /path/to/img.jpg "Title"

Both of the above examples produce the same output:

    <img src="/path/to/img.jpg" alt="alt text" title="Title" />



### Code ###

In a regular paragraph, you can create code span by wrapping text in
backtick quotes. Any ampersands (&) and angle brackets (< or
>) will automatically be translated into HTML entities. This makes
it easy to use Markdown to write about HTML example code:

    I strongly recommend against using any <blink> tags.

    I wish SmartyPants used named entities like &mdash;
    instead of decimal-encoded entites like &#8212;.

Output:

    <p>I strongly recommend against using any
    <code>&lt;blink&gt;</code> tags.</p>
    
    <p>I wish SmartyPants used named entities like
    <code>&amp;mdash;</code> instead of decimal-encoded
    entites like <code>&amp;#8212;</code>.</p>


To specify an entire block of pre-formatted code, indent every line of
the block by 4 spaces or 1 tab. Just like with code spans, &, <,
and > characters will be escaped automatically.

Markdown:

    If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:

        <blockquote>
            <p>For example.</p>
        </blockquote>

Output:

    <p>If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:</p>
    
    <pre><code>&lt;blockquote&gt;
        &lt;p&gt;For example.&lt;/p&gt;
    &lt;/blockquote&gt;
    </code></pre>
Markdown: Syntax
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a href="/projects/markdown/basics" title="Markdown Basics">Basics</a></li>
    <li><a class="selected" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


*   [Overview](#overview)
    *   [Philosophy](#philosophy)
    *   [Inline HTML](#html)
    *   [Automatic Escaping for Special Characters](#autoescape)
*   [Block Elements](#block)
    *   [Paragraphs and Line Breaks](#p)
    *   [Headers](#header)
    *   [Blockquotes](#blockquote)
    *   [Lists](#list)
    *   [Code Blocks](#precode)
    *   [Horizontal Rules](#hr)
*   [Span Elements](#span)
    *   [Links](#link)
    *   [Emphasis](#em)
    *   [Code](#code)
    *   [Images](#img)
*   [Miscellaneous](#misc)
    *   [Backslash Escapes](#backslash)
    *   [Automatic Links](#autolink)


**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL][src].

  [src]: /projects/markdown/syntax.text

* * *

<h2 id="overview">Overview</h2>

<h3 id="philosophy">Philosophy</h3>

Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

Readability, however, is emphasized above all else. A Markdown-formatted
document should be publishable as-is, as plain text, without looking
like it's been marked up with tags or formatting instructions. While
Markdown's syntax has been influenced by several existing text-to-HTML
filters -- including [Setext] [1], [atx] [2], [Textile] [3], [reStructuredText] [4],
[Grutatext] [5], and [EtText] [6] -- the single biggest source of
inspiration for Markdown's syntax is the format of plain text email.

  [1]: http://docutils.sourceforge.net/mirror/setext.html
  [2]: http://www.aaronsw.com/2002/atx/
  [3]: http://textism.com/tools/textile/
  [4]: http://docutils.sourceforge.net/rst.html
  [5]: http://www.triptico.com/software/grutatxt.html
  [6]: http://ettext.taint.org/doc/

To this end, Markdown's syntax is comprised entirely of punctuation
characters, which punctuation characters have been carefully chosen so
as to look like what they mean. E.g., asterisks around a word actually
look like \*emphasis\*. Markdown lists look like, well, lists. Even
blockquotes look like quoted passages of text, assuming you've ever
used email.



<h3 id="html">Inline HTML</h3>

Markdown's syntax is intended for one purpose: to be used as a
format for *writing* for the web.

Markdown is not a replacement for HTML, or even close to it. Its
syntax is very small, corresponding only to a very small subset of
HTML tags. The idea is *not* to create a syntax that makes it easier
to insert HTML tags. In my opinion, HTML tags are already easy to
insert. The idea for Markdown is to make it easy to read, write, and
edit prose. HTML is a *publishing* format; Markdown is a *writing*
format. Thus, Markdown's formatting syntax only addresses issues that
can be conveyed in plain text.

For any markup that is not covered by Markdown's syntax, you simply
use HTML itself. There's no need to preface it or delimit it to
indicate that you're switching from Markdown to HTML; you just use
the tags.

The only restrictions are that block-level HTML elements -- e.g. <div>,
<table>, <pre>, <p>, etc. -- must be separated from surrounding
content by blank lines, and the start and end tags of the block should
not be indented with tabs or spaces. Markdown is smart enough not
to add extra (unwanted) <p> tags around HTML block-level tags.

For example, to add an HTML table to a Markdown article:

    This is a regular paragraph.

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    This is another regular paragraph.

Note that Markdown formatting syntax is not processed within block-level
HTML tags. E.g., you can't use Markdown-style *emphasis* inside an
HTML block.

Span-level HTML tags -- e.g. <span>, <cite>, or <del> -- can be
used anywhere in a Markdown paragraph, list item, or header. If you
want, you can even use HTML tags instead of Markdown formatting; e.g. if
you'd prefer to use HTML <a> or <img> tags instead of Markdown's
link or image syntax, go right ahead.

Unlike block-level HTML tags, Markdown syntax *is* processed within
span-level tags.


<h3 id="autoescape">Automatic Escaping for Special Characters</h3>

In HTML, there are two characters that demand special treatment: <
and &. Left angle brackets are used to start tags; ampersands are
used to denote HTML entities. If you want to use them as literal
characters, you must escape them as entities, e.g. &lt;, and
&amp;.

Ampersands in particular are bedeviling for web writers. If you want to
write about 'AT&T', you need to write 'AT&amp;T'. You even need to
escape ampersands within URLs. Thus, if you want to link to:

    http://images.google.com/images?num=30&q=larry+bird

you need to encode the URL as:

    http://images.google.com/images?num=30&amp;q=larry+bird

in your anchor tag href attribute. Needless to say, this is easy to
forget, and is probably the single most common source of HTML validation
errors in otherwise well-marked-up web sites.

Markdown allows you to use these characters naturally, taking care of
all the necessary escaping for you. If you use an ampersand as part of
an HTML entity, it remains unchanged; otherwise it will be translated
into &amp;.

So, if you want to include a copyright symbol in your article, you can write:

    &copy;

and Markdown will leave it alone. But if you write:

    AT&T

Markdown will translate it to:

    AT&amp;T

Similarly, because Markdown supports [inline HTML](#html), if you use
angle brackets as delimiters for HTML tags, Markdown will treat them as
such. But if you write:

    4 < 5

Markdown will translate it to:

    4 &lt; 5

However, inside Markdown code spans and blocks, angle brackets and
ampersands are *always* encoded automatically. This makes it easy to use
Markdown to write about HTML code. (As opposed to raw HTML, which is a
terrible format for writing about HTML syntax, because every single <
and & in your example code needs to be escaped.)


* * *


<h2 id="block">Block Elements</h2>


<h3 id="p">Paragraphs and Line Breaks</h3>

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing but spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

The implication of the "one or more consecutive lines of text" rule is
that Markdown supports "hard-wrapped" text paragraphs. This differs
significantly from most other text-to-HTML formatters (including Movable
Type's "Convert Line Breaks" option) which translate every line break
character in a paragraph into a <br /> tag.

When you *do* want to insert a <br /> break tag using Markdown, you
end a line with two or more spaces, then type return.

Yes, this takes a tad more effort to create a <br />, but a simplistic
"every line break is a <br />" rule wouldn't work for Markdown.
Markdown's email-style [blockquoting][bq] and multi-paragraph [list items][l]
work best -- and look better -- when you format them with hard breaks.

  [bq]: #blockquote
  [l]:  #list



<h3 id="header">Headers</h3>

Markdown supports two styles of headers, [Setext] [1] and [atx] [2].

Setext-style headers are "underlined" using equal signs (for first-level
headers) and dashes (for second-level headers). For example:

    This is an H1
    =============

    This is an H2
    -------------

Any number of underlining ='s or -'s will work.

Atx-style headers use 1-6 hash characters at the start of the line,
corresponding to header levels 1-6. For example:

    # This is an H1

    ## This is an H2

    ###### This is an H6

Optionally, you may "close" atx-style headers. This is purely
cosmetic -- you can use this if you think it looks better. The
closing hashes don't even need to match the number of hashes
used to open the header. (The number of opening hashes
determines the header level.) :

    # This is an H1 #

    ## This is an H2 ##

    ### This is an H3 ######


<h3 id="blockquote">Blockquotes</h3>

Markdown uses email-style > characters for blockquoting. If you're
familiar with quoting passages of text in an email message, then you
know how to create a blockquote in Markdown. It looks best if you hard
wrap the text and put a > before every line:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    > 
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

Markdown allows you to be lazy and only put the > before the first
line of a hard-wrapped paragraph:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

Blockquotes can be nested (i.e. a blockquote-in-a-blockquote) by
adding additional levels of >:

    > This is the first level of quoting.
    >
    > > This is nested blockquote.
    >
    > Back to the first level.

Blockquotes can contain other Markdown elements, including headers, lists,
and code blocks:

	> ## This is a header.
	> 
	> 1.   This is the first list item.
	> 2.   This is the second list item.
	> 
	> Here's some example code:
	> 
	>     return shell_exec("echo $input | $markdown_script");

Any decent text editor should make email-style quoting easy. For
example, with BBEdit, you can make a selection and choose Increase
Quote Level from the Text menu.


<h3 id="list">Lists</h3>

Markdown supports ordered (numbered) and unordered (bulleted) lists.

Unordered lists use asterisks, pluses, and hyphens -- interchangably
-- as list markers:

    *   Red
    *   Green
    *   Blue

is equivalent to:

    +   Red
    +   Green
    +   Blue

and:

    -   Red
    -   Green
    -   Blue

Ordered lists use numbers followed by periods:

    1.  Bird
    2.  McHale
    3.  Parish

It's important to note that the actual numbers you use to mark the
list have no effect on the HTML output Markdown produces. The HTML
Markdown produces from the above list is:

    <ol>
    <li>Bird</li>
    <li>McHale</li>
    <li>Parish</li>
    </ol>

If you instead wrote the list in Markdown like this:

    1.  Bird
    1.  McHale
    1.  Parish

or even:

    3. Bird
    1. McHale
    8. Parish

you'd get the exact same HTML output. The point is, if you want to,
you can use ordinal numbers in your ordered Markdown lists, so that
the numbers in your source match the numbers in your published HTML.
But if you want to be lazy, you don't have to.

If you do use lazy list numbering, however, you should still start the
list with the number 1. At some point in the future, Markdown may support
starting ordered lists at an arbitrary number.

List markers typically start at the left margin, but may be indented by
up to three spaces. List markers must be followed by one or more spaces
or a tab.

To make lists look nice, you can wrap items with hanging indents:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
        Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
        viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
        Suspendisse id sem consectetuer libero luctus adipiscing.

But if you want to be lazy, you don't have to:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.

If list items are separated by blank lines, Markdown will wrap the
items in <p> tags in the HTML output. For example, this input:

    *   Bird
    *   Magic

will turn into:

    <ul>
    <li>Bird</li>
    <li>Magic</li>
    </ul>

But this:

    *   Bird

    *   Magic

will turn into:

    <ul>
    <li><p>Bird</p></li>
    <li><p>Magic</p></li>
    </ul>

List items may consist of multiple paragraphs. Each subsequent
paragraph in a list item must be intended by either 4 spaces
or one tab:

    1.  This is a list item with two paragraphs. Lorem ipsum dolor
        sit amet, consectetuer adipiscing elit. Aliquam hendrerit
        mi posuere lectus.

        Vestibulum enim wisi, viverra nec, fringilla in, laoreet
        vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
        sit amet velit.

    2.  Suspendisse id sem consectetuer libero luctus adipiscing.

It looks nice if you indent every line of the subsequent
paragraphs, but here again, Markdown will allow you to be
lazy:

    *   This is a list item with two paragraphs.

        This is the second paragraph in the list item. You're
    only required to indent the first line. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit.

    *   Another item in the same list.

To put a blockquote within a list item, the blockquote's >
delimiters need to be indented:

    *   A list item with a blockquote:

        > This is a blockquote
        > inside a list item.

To put a code block within a list item, the code block needs
to be indented *twice* -- 8 spaces or two tabs:

    *   A list item with a code block:

            <code goes here>


It's worth noting that it's possible to trigger an ordered list by
accident, by writing something like this:

    1986. What a great season.

In other words, a *number-period-space* sequence at the beginning of a
line. To avoid this, you can backslash-escape the period:

    1986\. What a great season.



<h3 id="precode">Code Blocks</h3>

Pre-formatted code blocks are used for writing about programming or
markup source code. Rather than forming normal paragraphs, the lines
of a code block are interpreted literally. Markdown wraps a code block
in both <pre> and <code> tags.

To produce a code block in Markdown, simply indent every line of the
block by at least 4 spaces or 1 tab. For example, given this input:

    This is a normal paragraph:

        This is a code block.

Markdown will generate:

    <p>This is a normal paragraph:</p>

    <pre><code>This is a code block.
    </code></pre>

One level of indentation -- 4 spaces or 1 tab -- is removed from each
line of the code block. For example, this:

    Here is an example of AppleScript:

        tell application "Foo"
            beep
        end tell

will turn into:

    <p>Here is an example of AppleScript:</p>

    <pre><code>tell application "Foo"
        beep
    end tell
    </code></pre>

A code block continues until it reaches a line that is not indented
(or the end of the article).

Within a code block, ampersands (&) and angle brackets (< and >)
are automatically converted into HTML entities. This makes it very
easy to include example HTML source code using Markdown -- just paste
it and indent it, and Markdown will handle the hassle of encoding the
ampersands and angle brackets. For example, this:

        <div class="footer">
            &copy; 2004 Foo Corporation
        </div>

will turn into:

    <pre><code>&lt;div class="footer"&gt;
        &amp;copy; 2004 Foo Corporation
    &lt;/div&gt;
    </code></pre>

Regular Markdown syntax is not processed within code blocks. E.g.,
asterisks are just literal asterisks within a code block. This means
it's also easy to use Markdown to write about Markdown's own syntax.



<h3 id="hr">Horizontal Rules</h3>

You can produce a horizontal rule tag (<hr />) by placing three or
more hyphens, asterisks, or underscores on a line by themselves. If you
wish, you may use spaces between the hyphens or asterisks. Each of the
following lines will produce a horizontal rule:

    * * *

    ***

    *****
	
    - - -

    ---------------------------------------

	_ _ _


* * *

<h2 id="span">Span Elements</h2>

<h3 id="link">Links</h3>

Markdown supports two style of links: *inline* and *reference*.

In both styles, the link text is delimited by [square brackets].

To create an inline link, use a set of regular parentheses immediately
after the link text's closing square bracket. Inside the parentheses,
put the URL where you want the link to point, along with an *optional*
title for the link, surrounded in quotes. For example:

    This is [an example](http://example.com/ "Title") inline link.

    [This link](http://example.net/) has no title attribute.

Will produce:

    <p>This is <a href="http://example.com/" title="Title">
    an example</a> inline link.</p>

    <p><a href="http://example.net/">This link</a> has no
    title attribute.</p>

If you're referring to a local resource on the same server, you can
use relative paths:

    See my [About](/about/) page for details.

Reference-style links use a second set of square brackets, inside
which you place a label of your choosing to identify the link:

    This is [an example][id] reference-style link.

You can optionally use a space to separate the sets of brackets:

    This is [an example] [id] reference-style link.

Then, anywhere in the document, you define your link label like this,
on a line by itself:

    [id]: http://example.com/  "Optional Title Here"

That is:

*   Square brackets containing the link identifier (optionally
    indented from the left margin using up to three spaces);
*   followed by a colon;
*   followed by one or more spaces (or tabs);
*   followed by the URL for the link;
*   optionally followed by a title attribute for the link, enclosed
    in double or single quotes.

The link URL may, optionally, be surrounded by angle brackets:

    [id]: <http://example.com/>  "Optional Title Here"

You can put the title attribute on the next line and use extra spaces
or tabs for padding, which tends to look better with longer URLs:

    [id]: http://example.com/longish/path/to/resource/here
        "Optional Title Here"

Link definitions are only used for creating links during Markdown
processing, and are stripped from your document in the HTML output.

Link definition names may constist of letters, numbers, spaces, and punctuation -- but they are *not* case sensitive. E.g. these two links:

	[link text][a]
	[link text][A]

are equivalent.

The *implicit link name* shortcut allows you to omit the name of the
link, in which case the link text itself is used as the name.
Just use an empty set of square brackets -- e.g., to link the word
"Google" to the google.com web site, you could simply write:

	[Google][]

And then define the link:

	[Google]: http://google.com/

Because link names may contain spaces, this shortcut even works for
multiple words in the link text:

	Visit [Daring Fireball][] for more information.

And then define the link:
	
	[Daring Fireball]: http://daringfireball.net/

Link definitions can be placed anywhere in your Markdown document. I
tend to put them immediately after each paragraph in which they're
used, but if you want, you can put them all at the end of your
document, sort of like footnotes.

Here's an example of reference links in action:

    I get 10 times more traffic from [Google] [1] than from
    [Yahoo] [2] or [MSN] [3].

      [1]: http://google.com/        "Google"
      [2]: http://search.yahoo.com/  "Yahoo Search"
      [3]: http://search.msn.com/    "MSN Search"

Using the implicit link name shortcut, you could instead write:

    I get 10 times more traffic from [Google][] than from
    [Yahoo][] or [MSN][].

      [google]: http://google.com/        "Google"
      [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
      [msn]:    http://search.msn.com/    "MSN Search"

Both of the above examples will produce the following HTML output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from
    <a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a>
    or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p>

For comparison, here is the same paragraph written using
Markdown's inline link style:

    I get 10 times more traffic from [Google](http://google.com/ "Google")
    than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or
    [MSN](http://search.msn.com/ "MSN Search").

The point of reference-style links is not that they're easier to
write. The point is that with reference-style links, your document
source is vastly more readable. Compare the above examples: using
reference-style links, the paragraph itself is only 81 characters
long; with inline-style links, it's 176 characters; and as raw HTML,
it's 234 characters. In the raw HTML, there's more markup than there
is text.

With Markdown's reference-style links, a source document much more
closely resembles the final output, as rendered in a browser. By
allowing you to move the markup-related metadata out of the paragraph,
you can add links without interrupting the narrative flow of your
prose.


<h3 id="em">Emphasis</h3>

Markdown treats asterisks (*) and underscores (_) as indicators of
emphasis. Text wrapped with one * or _ will be wrapped with an
HTML <em> tag; double *'s or _'s will be wrapped with an HTML
<strong> tag. E.g., this input:

    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__

will produce:

    <em>single asterisks</em>

    <em>single underscores</em>

    <strong>double asterisks</strong>

    <strong>double underscores</strong>

You can use whichever style you prefer; the lone restriction is that
the same character must be used to open and close an emphasis span.

Emphasis can be used in the middle of a word:

    un*fucking*believable

But if you surround an * or _ with spaces, it'll be treated as a
literal asterisk or underscore.

To produce a literal asterisk or underscore at a position where it
would otherwise be used as an emphasis delimiter, you can backslash
escape it:

    \*this text is surrounded by literal asterisks\*



<h3 id="code">Code</h3>

To indicate a span of code, wrap it with backtick quotes (  ).
Unlike a pre-formatted code block, a code span indicates code within a
normal paragraph. For example:

    Use the printf() function.

will produce:

    <p>Use the <code>printf()</code> function.</p>

To include a literal backtick character within a code span, you can use
multiple backticks as the opening and closing delimiters:

     There is a literal backtick () here.

which will produce this:

    <p><code>There is a literal backtick () here.</code></p>

The backtick delimiters surrounding a code span may include spaces --
one after the opening, one before the closing. This allows you to place
literal backtick characters at the beginning or end of a code span:

	A single backtick in a code span:     
	
	A backtick-delimited string in a code span:   foo  

will produce:

	<p>A single backtick in a code span: <code></code></p>
	
	<p>A backtick-delimited string in a code span: <code>foo</code></p>

With a code span, ampersands and angle brackets are encoded as HTML
entities automatically, which makes it easy to include example HTML
tags. Markdown will turn this:

    Please don't use any <blink> tags.

into:

    <p>Please don't use any <code>&lt;blink&gt;</code> tags.</p>

You can write this:

    &#8212; is the decimal-encoded equivalent of &mdash;.

to produce:

    <p><code>&amp;#8212;</code> is the decimal-encoded
    equivalent of <code>&amp;mdash;</code>.</p>



<h3 id="img">Images</h3>

Admittedly, it's fairly difficult to devise a "natural" syntax for
placing images into a plain text document format.

Markdown uses an image syntax that is intended to resemble the syntax
for links, allowing for two styles: *inline* and *reference*.

Inline image syntax looks like this:

    ![Alt text](/path/to/img.jpg)

    ![Alt text](/path/to/img.jpg "Optional title")

That is:

*   An exclamation mark: !;
*   followed by a set of square brackets, containing the alt
    attribute text for the image;
*   followed by a set of parentheses, containing the URL or path to
    the image, and an optional title attribute enclosed in double
    or single quotes.

Reference-style image syntax looks like this:

    ![Alt text][id]

Where "id" is the name of a defined image reference. Image references
are defined using syntax identical to link references:

    [id]: url/to/image  "Optional title attribute"

As of this writing, Markdown has no syntax for specifying the
dimensions of an image; if this is important to you, you can simply
use regular HTML <img> tags.


* * *


<h2 id="misc">Miscellaneous</h2>

<h3 id="autolink">Automatic Links</h3>

Markdown supports a shortcut style for creating "automatic" links for URLs and email addresses: simply surround the URL or email address with angle brackets. What this means is that if you want to show the actual text of a URL or email address, and also have it be a clickable link, you can do this:

    <http://example.com/>
    
Markdown will turn this into:

    <a href="http://example.com/">http://example.com/</a>

Automatic links for email addresses work similarly, except that
Markdown will also perform a bit of randomized decimal and hex
entity-encoding to help obscure your address from address-harvesting
spambots. For example, Markdown will turn this:

    <address@example.com>

into something like this:

    <a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
    &#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
    &#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
    &#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>

which will render in a browser as a clickable link to "address@example.com".

(This sort of entity-encoding trick will indeed fool many, if not
most, address-harvesting bots, but it definitely won't fool all of
them. It's better than nothing, but an address published in this way
will probably eventually start receiving spam.)



<h3 id="backslash">Backslash Escapes</h3>

Markdown allows you to use backslash escapes to generate literal
characters which would otherwise have special meaning in Markdown's
formatting syntax. For example, if you wanted to surround a word with
literal asterisks (instead of an HTML <em> tag), you can backslashes
before the asterisks, like this:

    \*literal asterisks\*

Markdown provides backslash escapes for the following characters:

    \   backslash
       backtick
    *   asterisk
    _   underscore
    {}  curly braces
    []  square brackets
    ()  parentheses
    #   hash mark
	+	plus sign
	-	minus sign (hyphen)
    .   dot
    !   exclamation mark

# Character Escapes

The MD5 value for + is "26b17225b626fb9238849fd60eabdf60".

# HTML Blocks

<p>test</p>

The MD5 value for <p>test</p> is:

6205333b793f34273d75379350b36826* test
+ test
- test

1. test
2. test

* test
+ test
- test

1. test
2. test
> foo
>
> > bar
>
> foo
Valid nesting:

**[Link](url)**

[**Link**](url)

**[**Link**](url)**

Invalid nesting:

[[Link](url)](url)## Unordered

Asterisks tight:

*	asterisk 1
*	asterisk 2
*	asterisk 3


Asterisks loose:

*	asterisk 1

*	asterisk 2

*	asterisk 3

* * *

Pluses tight:

+	Plus 1
+	Plus 2
+	Plus 3


Pluses loose:

+	Plus 1

+	Plus 2

+	Plus 3

* * *


Minuses tight:

-	Minus 1
-	Minus 2
-	Minus 3


Minuses loose:

-	Minus 1

-	Minus 2

-	Minus 3


## Ordered

Tight:

1.	First
2.	Second
3.	Third

and:

1. One
2. Two
3. Three


Loose using tabs:

1.	First

2.	Second

3.	Third

and using spaces:

1. One

2. Two

3. Three

Multiple paragraphs:

1.	Item 1, graf one.

	Item 2. graf two. The quick brown fox jumped over the lazy dog's
	back.
	
2.	Item 2.

3.	Item 3.



## Nested

*	Tab
	*	Tab
		*	Tab

Here's another:

1. First
2. Second:
	* Fee
	* Fie
	* Foe
3. Third

Same thing but with paragraphs:

1. First

2. Second:
	* Fee
	* Fie
	* Foe

3. Third


This was an error in Markdown 1.0.1:

*	this

	*	sub

	that
[Inline link 1 with parens](/url\(test\) "title").

[Inline link 2 with parens](</url\(test\)> "title").

[Inline link 3 with non-escaped parens](/url(test) "title").

[Inline link 4 with non-escaped parens](</url(test)> "title").

[Reference link 1 with parens][1].

[Reference link 2 with parens][2].

  [1]: /url(test) "title"
  [2]: </url(test)> "title"
This tests for a bug where quotes escaped by PHP when using 
preg_replace with the /e modifier must be correctly unescaped
(hence the _UnslashQuotes function found only in PHP Markdown).



Headers below should appear exactly as they are typed (no backslash
added or removed).

Header "quoted\" again \\""
===========================

Header "quoted\" again \\""
---------------------------

### Header "quoted\" again \\"" ###



Test with tabs for _Detab:

	Code	'block'	with	some	"tabs"	and	"quotes"
[Test](/"style="color:red)
[Test](/'style='color:red)

![](/"style="border-color:red;border-size:1px;border-style:solid)
![](/'style='border-color:red;border-size:1px;border-style:solid)
***This is strong and em.***

So is ***this*** word.

___This is strong and em.___

So is ___this___ word.
# Simple tables

Header 1  | Header 2
--------- | ---------
Cell 1    | Cell 2
Cell 3    | Cell 4

With leading pipes:

| Header 1  | Header 2
| --------- | ---------
| Cell 1    | Cell 2
| Cell 3    | Cell 4

With tailing pipes:

Header 1  | Header 2  |
--------- | --------- |
Cell 1    | Cell 2    |
Cell 3    | Cell 4    |

With leading and tailing pipes:

| Header 1  | Header 2  |
| --------- | --------- |
| Cell 1    | Cell 2    |
| Cell 3    | Cell 4    |

* * *

# One-column one-row table

With leading pipes:

| Header
| -------
| Cell

With tailing pipes:

Header  |
------- |
Cell    |

With leading and tailing pipes:

| Header  |
| ------- |
| Cell    |

* * *

Table alignement:

| Default   | Right     |  Center   |     Left  |
| --------- |:--------- |:---------:| ---------:|
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

Table alignement (alternate spacing):

| Default   | Right     |  Center   |     Left  |
| --------- | :-------- | :-------: | --------: |
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

* * * 

# Empty cells

| Header 1  | Header 2  |
| --------- | --------- |
| A         | B         |
| C         |           |

Header 1  | Header 2
--------- | ---------
A         | B
          | D

* * *

# Missing tailing pipe

Header 1  | Header 2  
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- 
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      

* * *

# Too many pipes in rows

| Header 1  | Header 2  |
| --------- 
| Cell      | Cell      | Extra cell? |
| Cell      | Cell      | Extra cell? |

+	this is a list item
	indented with tabs

+   this is a list item
    indented with spaces

Code:

	this code block is indented by one tab

And:

		this code block is indented by two tabs

And:

	+	this is an example list item
		indented with tabs
	
	+   this is an example list item
	    indented with spaces
> A list within a blockquote:
> 
> *	asterisk 1
> *	asterisk 2
> *	asterisk 3
Paragraph and no space:
* ciao

Paragraph and 1 space:
 * ciao

Paragraph and 3 spaces:
  * ciao

Paragraph and 4 spaces:
   * ciao

Paragraph before header:
#Header

Paragraph before blockquote:
>Some quote.
 .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>


As above: checking for bad interractions with the HTML block parser:

 html
<div>


Some *markdown* formatting.

 html
</div>


Some *markdown*


<div>
    <html>



function test();


<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">

<html>
    <title>

</div>

Two code blocks with no blank line between them:


<div>


<div>


Testing *confusion* with markers in the middle:


<div></div>


Testing mixing with title code blocks


<p>
 
<p>

 
<p>

<p>
 

<Fenced>


Code block starting and ending with empty lines:



<Fenced>




Indented code block containing fenced code block sample:

	
	<Fenced>
	

Fenced code block with indented code block sample:


Some text

	Indented code block sample code


Fenced code block with long markers:


Fenced


Fenced code block with fenced code block markers of different length in it:


In code block

Still in code block

Still in code block


Fenced code block with Markdown header and horizontal rule:


#test
---


Fenced code block with link definitions, footnote definition and 
abbreviation definitions:


[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language


* In a list item with smalish indent:

  
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
  
  
With HTML content.
  

<b>bold</b>


Bug with block level elements in this case:

  <div>
  </div>


Indented code block of a fenced code block:

    
	haha!
	

With class:
  
html
<b>bold</b>

  
 html
<b>bold</b>

  
.html
<b>bold</b>

  
 .html
<b>bold</b>


With extra attribute block:

{.html}
<b>bold</b>

  
 {.html #codeid}
<b>bold</b>


 .html{.bold}
<div>

  
 .html {#codeid}
</div>
First line. <br/>
Second line.

This is a first paragraph,
on multiple lines.
     
This is a second paragraph.
There are spaces in between the two.This is a first paragraph,
on multiple lines.

This is a second paragraph
which has multiple lines too.A first paragraph.



A second paragraph after 3 CR (carriage return).This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
     
A few spaces and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
	
1 tab to separate them and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.

A new long long long long long long long long long long long long long long long long paragraph on 1 line.An ampersand & in the text flow is escaped as an html entity.There is an [ampersand](http://validator.w3.org/check?uri=http://www.w3.org/&verbose=1) in the URI.This is \*an asterisk which should stay as is.This is * an asterisk which should stay as is.\\   backslash
\   backtick
\*   asterisk
\_   underscore
\{\}  curly braces
\[\]  square brackets
\(\)  parentheses
\#   hash mark
\+   plus sign
\-   minus sign (hyphen)
\.   dot
\!   exclamation mark> # heading level 1
> 
> paragraph>A blockquote with a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.

>and a second very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.>This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a blockquote.> A blockquote
> on multiple lines
> like this.>A blockquote 
>on multiple lines 
>like this. >A blockquote
>on multiple lines
>like this.
>
>But it has
>two paragraphs.>A blockquote
>on multiple lines
>like this> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.
> This is the first level of quoting.
>
> > This is nested blockquote.> This is the first level of quoting.
> > This is nested blockquote.
> Back to the first level.
> This is the first level of quoting.
> > This is nested blockquote.
	10 PRINT HELLO INFINITE
	20 GOTO 10    10 PRINT < > &
    20 GOTO 10    10 PRINT HELLO INFINITE
    20 GOTO 10# Contributing to Mardown Test Suite

1. [Getting Involved](#getting-involved)
2. [Discussion](#discussion)
3. [How To Report an Issue](#how-to-report-an-issue)
4. [Editing Markdown Specification](#editing-markdown-specification)
5. [Test Suite Guidelines](#test-suite-guidelines)
6. [Pull Request Guidelines](#pull-request-guidelines)

## Getting Involved

There are a number of ways to get involved with the development of the Markdown Test Suite. If you are a first time contributor to an open source project, you can still add value to this project. You may identify grammar issues, write prose, examples or documentation for the project. You may flag some errors and open new issues.

Read all bits of this document and that will guide you on how to participate.

## Discussion

### Mailing List

The Markdown Test Suite has been started a little bit after the start of the [Markdown Community Group](http://www.w3.org/community/markdown/). You may want to discuss about Markdown and this project on the [group mailing-list](http://lists.w3.org/Archives/Public/public-markdown/).

## How to Report an Issue

Don't be afraid to add details to your issue. The more context you give, the better for people participating to the project. Make a short summary, add a description with the context and give links to places which will help to understand.

## Editing Markdown Specification

There is much needed work on the [Markdown Specification](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html). It doesn't require strong competences in coding. Be systematic in the markup and follow the way it is already organized. Each time you added a new atomic section, create a commit for this specific part.

## Test Suite Guidelines

When proposing new tests, make sure they do not already exist in the current test suite. You will notice that there is a separate section dedicated to the specific extensions that some markdown generators have created. Keep them separate. We want to keep the core clean and close to the original specification of Markdown.

If you are not sure, create an issue.

### Markdown Extensions

Markdown extension tests are accepted. Use the following rules:

- place all extension tests under the test/extensions/ENGINE directory with filename equal to the feature name
- for each ENGINE and add a README.markdown under the engine directory with a link to its specification

where ENGINE is either of:

- a command line utility. E.g. pandoc, kramdown.
- a programming API. E.g. Redcarpet::Markdown.new().
- a programmatically accessible web service. E.g.: GFM via the GitHub API.
- a non programmatically accessible web service. E.g.: Stack Overflow flavored markdown.

To avoid test duplication for common features, use the following rules:

- if file tests/extensions/ENGINE/FEATURE.md is empty or not present, use tests/extensions/FEATURE.md instead
- if file tests/extensions/ENGINE/FEATURE.out not present, use tests/extensions/FEATURE.out instead
- for a given ENGINE, only features which have either a .md or a .out are implemented by that engine.
- in case of different outputs for a single feature input, keep directly under extensions/ only the output case that happens across the most engines

**version**

Only the latest stable version of each ENGINE is considered.

**options**

The IO behavior tested is for engine defaults, without any options (command line options, extra JSON parameters, etc.) passed to the engine.

**external state**

Tests that use external state not present in the markdown input shall not be included in this test suite.

For example, what GFM @user user tags render to also depends on the state of GitHub's databases (only render to a link if user exists), not only on the input markdown.

#### Examples

GFM and the "fenced code block" use the following file structure:

    tests/extensions/gfm/README.markdown
    tests/extensions/gfm/fenced-code-block.md
    tests/extensions/gfm/fenced-code-block.out

where README.markdown contains:

    https://help.github.com/articles/github-flavored-markdown

To avoid duplication with other engines, if the input / output (normalized to DOM) is the same across multiple engines use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

If the input is the same, and outputs are DOM different, but represent the same idea (e.g. both represent computer code) use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/gfm/fenced-code-block.out
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

#### New Extensions

Tests are modular, and if you want to test a new engine for your project, that should be easy to do.

If you feel that the new engine is reasonably popular, please send a pull request adding it.

## Commits and Pull Requests

* Keep your commits clean and commented
* Do not mix in one commit different things. Keep modifications related.
* Do not mix everything in one giant pull request. Create separate pull requests for different topic. That will help to have a more meaningful debate about the pull requests and will help to review the code.
* If it relates to a specific issue, add the number of the issue in the commit message.

Thanks for Contributing
as*te*risks*single asterisks*_single underscores_HTML entities are written using ampersand notation: &copy;These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

This is an H1
=============# This is an H1 # # This is an H1# this is an h1 with two trailing spaces  
A new paragraph.# This is an H1This is an H2
-------------## This is an H2 #### This is an H2### This is an H3 ###### This is an H3#### This is an H4 ######## This is an H4##### This is an H5 ########## This is an H5###### This is an H6  ############ This is an H6- - ----***___-------![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 for everyone"![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 logo for everyone")![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png)We love <code> and & for everything We love code for everything We love code for everything The MIT License (MIT)

Copyright (c) 2013 Karl Dubost

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
A first sentence  
and a line break.A first sentence     
and a line break.This is an automatic link <http://www.w3.org/>[W3C](http://www.w3.org/ "Discover w3c")[W3C](http://www.w3.org/)[World Wide Web Consortium][w3c]

[w3c]: <http://www.w3.org/>[World Wide Web Consortium][]

[World Wide Web Consortium]: http://www.w3.org/[w3c][]

[w3c]: http://www.w3.org/[World Wide Web Consortium] [w3c]

[w3c]: http://www.w3.org/[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/
   "Discover W3C"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ (Discover w3c)[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ 'Discover w3c'[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ "Discover w3c"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/*   a list containing a blockquote

    > this the blockquote in the list* a

        b
*   a list containing a block of code

	    10 PRINT HELLO INFINITE
	    20 GOTO 10*   This is a list item with two paragraphs. Lorem ipsum dolor
	sit amet, consectetuer adipiscing elit. Aliquam hendrerit
	mi posuere lectus.

	Vestibulum enim wisi, viverra nec, fringilla in, laoreet
	vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
	sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.*   This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.1\. ordered list escape1. 1

    - inner par list

2. 2
1. list item 1
8. list item 2
1. list item 31. list item 1
2. list item 2
3. list item 3This is a paragraph
on multiple lines
with hard return.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line. This is a paragraph with a trailing and leading space. This is a paragraph with 1 trailing tab.	  This is a paragraph with 2 leading spaces.   This is a paragraph with 3 leading spaces. This is a paragraph with 1 leading space.This is a paragraph with a trailing space. # Colophon - October 1st, 2014

This project was initiated to provide a test suite for Markdown markup, and eventually create a specification from this test results. A part of of the community has started a new endeavor which seems to get traction as [CommonMark](https://github.com/jgm/stmd). **We are then closing this project** and encourage you to contribute to CommonMark. 

The most interesting part of this project would not have been possible without the dedication of [Ciro Santilli](https://github.com/cirosantilli) @cirosantilli. So big applause and thank you to him.


The rest is kept around for archives and references.

# Markdown Test Suite

Inspired by questions on [W3C Markdown Community Group](http://www.w3.org/community/markdown).

Pull Requests are welcome. See the [CONTRIBUTING Guidelines](https://github.com/karlcow/markdown-testsuite/blob/master/CONTRIBUTING.md)

## Design goals

- Comprehensive.
- Small modularized tests.
- Easy to run tests using any programming language. In particular, data representations must have an implementation on all major languages.
- Develop a consensus based markdown specification at [markdown-spec.html](markdown-spec.html). Visualize it [here](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html).

## Test Scripts

Markdown Test Suite already includes tests for many important markdown engines.

To see what the scripts do run:

    ./cat-all.py -h
    ./run-tests.py -h

To configure the scripts do:

	cp config_local.py.example config_local.py

and edit config_local.py. It is already gitignored.

A Vagrantfile is provided with a provision script that installs all installable engines.

Sample output from run-tests.py:

    blackfriday   |......FFF..............FF...F....................................F....................................|   0.93s  102    7   6%
	gfm           |FF.....F.....F...FFFF..F....F........................FFFF...FF...............FF...F.......F...........| 262.88s  102   20  19%
    hoedown       |..............................F.................................................F.....................|   0.36s  102    2   1%
	kramdown      |......FFF.....FF.......FF.......FF.FFFFFFFFFFFFF.......................F..............................|  30.69s  102   23  22%
    lunamark      |FFFFFF.F.FFFFFFFFFFFF.F.....FFFF..FF............FFFFF..FFFFFFFFFF..............F...FFFFFFFFFFF........|   1.58s  103   53  51%
    markdown_pl   |.....................FFFF...............................F...............F.............................|   2.56s  102    6   5%
    markdown2     |......................................................................................................|   5.39s  103    0   0%
    marked        |..............F.................FFFFFFFFFFFFFFFF......................F.F.............................|   6.22s  102   19  18%
    maruku        |......FFF......F.......F.FFF...............................................FF.........................|  37.02s  102   10   9%
    md2html       |.........................FFF...F............................................FF........................|   7.42s  102    6   5%
    multimarkdown |......FFF....FF...F............FFF.FFFFFFFFFFFFF.....FFFF.........F...................................|   0.58s  102   27  26%
    pandoc        |FF...........F.F.FFFF..FFFFF....FF.FFFFFFFFFFFFF.....FFFF.....FF............FFF.FFF..................F|   1.11s  102   41  40%
    peg_markdown  |.................................................................F....................................|   0.46s  102    1   0%
    rdiscount     |.......F.........................................................F....................................|  25.19s  102    3   2%
    redcarpet     |......................................................................................................|  21.49s  102    0   0%
    showdown      |.......................................................................F..............................|   6.85s  102    1   0%

	Extensions:

    blackfriday   |F..|  0.04s    3    1  33%
	gfm           |F.|   2.37s    2    1  50%
    hoedown       |.|    0.00s    1    0   0%
    lunamark      |F.F|  0.05s    3    2  66%
    kramdown      |..|   0.62s    2    0   0%
    markdown_pl   ||     0.00s    0    0   0%
    markdown2     |F.|   0.14s    2    1  50%
    marked        |F.|   0.13s    2    1  50%
    maruku        |F..|  1.06s    3    1  33%
    md2html       |F.|   0.14s    2    0   0%
    multimarkdown |F.|   0.01s    2    1  50%
    pandoc        |F.|   0.02s    2    1  50%
    peg_markdown  |...|  0.02s    3    0   0%
    rdiscount     |F..|   0.74s    3    1  33%
    redcarpet     |..|   0.42s    2    0   0%
    showdown      |F..|  0.20s    3    1  33%

Where F indicates a failing test.

## Other Noticeable Test Suites

We haven't been the first test suite effort. Some projects have maintained their own test suite for a long time. Hopefully we can reach a state where people agree on the terms of what should be a good test suite for all developers.

- [Original test suite](http://daringfireball.net/projects/downloads/MarkdownTest_1.0.zip)
- [PHP markdown test suite:](https://github.com/michelf/mdtest/tree/master/Markdown.mdtest)
- [Markdown-js test suite](https://github.com/evilstreak/markdown-js/tree/master/test/features)
- [Python markdown 2 test suite](https://github.com/trentm/python-markdown2/tree/master/test/tm-cases)
- [multimarkdown test suite](https://github.com/fletcher/MMD-Test-Suite)
- [John MacFarlane's Standard Markdown spec](https://github.com/jgm/stmd)

In addition we should note the [wonderful work](http://johnmacfarlane.net/babelmark2/) made by John Mac Farlane. The Web service output the differences in between the different markdown implementations. It helps a lot when searching on the most common output.
as**te**risks**double asterisks**__double underscores__* list item 1
* list item 2
* list item 3
- list item 1
- list item 2
- list item 3 * list item 1
 * list item 2
 * list item 3  * list item 1
  * list item 2
  * list item 3   * list item 1
   * list item 2
   * list item 3+ list item 1
+ list item 2
+ list item 3* list item in paragraph

* another list item in paragraph*   This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a list.
*   and yet another long long long long long long long long long long long long long long long long long long long long long long line.*   This is a list item
    with the content on
    multiline and indented.
*   And this another list item
    with the same principle.€Some text about HTML, SGML and HTML4.

Let's talk about the U.S.A., (É.U. or É.-U. d'A. in French).

*[HTML4]: Hyper Text Markup Language version 4
*[HTML]: Hyper Text Markup Language
*[SGML]: Standard Generalized Markup Language
*[U.S.A.]: United States of America
*[É.U.] : États-Unis d'Amérique
*[É.-U. d'A.] : États-Unis d'Amérique

And here we have a CD, some CDs, and some other CD's.

*[CD]: Compact Disk

Let's transfert documents through TCP/IP, using TCP packets.

*[IP]: Internet Protocol
*[TCP]: Transmission Control Protocol

 ---

Bienvenue sur [CMS](http://www.bidulecms.com "Bidule CMS").

*[CMS]: Content Management System

 ---

ATCCE

*[ATCCE]: Abbreviation "Testing" Correct 'Character' < Escapes >* one
* two

1. three
2. four

* one
* two
1. three
2. fourAT&T has an ampersand in their name.

AT&amp;T is another way to write it.

This & that.

4 < 5.

6 > 5.

Here's a [link] [1] with an ampersand in the URL.

Here's a link with an amersand in the link text: [AT&T] [2].

Here's an inline [link](/script?foo=1&bar=2).

Here's an inline [link](</script?foo=1&bar=2>).


[1]: http://example.com/?foo=1&bar=2
[2]: http://att.com/  "AT&T"Link: <http://example.com/>.

With an ampersand: <http://example.com/?foo=1&bar=2>

* In a list?
* <http://example.com/>
* It should.

> Blockquoted: <http://example.com/>

Auto-links should not occur here: <http://example.com/>

	or here: <http://example.com/>These should all get escaped:

Backslash: \\

Backtick: \

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-



These should not, because they occur within a code block:

	Backslash: \\

	Backtick: \

	Asterisk: \*

	Underscore: \_

	Left brace: \{

	Right brace: \}

	Left bracket: \[

	Right bracket: \]

	Left paren: \(

	Right paren: \)

	Greater-than: \>

	Hash: \#

	Period: \.

	Bang: \!

	Plus: \+

	Minus: \-


Nor should these, which occur in code spans:

Backslash: \\

Backtick:   \  

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-


These should get escaped, even though they're matching pairs for
other Markdown constructs:

\*asterisks\*

\_underscores\_

\backticks\

This is a code span with a literal backslash-backtick sequence:   \  

This is a tag with unescaped backticks <span attr='ticks'>bar</span>.

This is a tag with backslashes <span attr='\\backslashes\\'>bar</span>.
  .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>
 

As above: checking for bad interractions with the HTML block parser:

  html
<div>
 

Some *markdown* formatting.

  html
</div>
 

Some *markdown*

 
<div>
    <html>
 

 
function test();
 

<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">
 
<html>
    <title>
 
</div>

Two code blocks with no blank line between them:

 
<div>
 
 
<div>
 

Testing *confusion* with code spans at the HTML block parser:

 
<div></div>
 

Testing mixing with title code blocks

 
<p>

<p>
 

<p>
 
<p>

 
<Fenced>
 

Code block starting and ending with empty lines:
 


<Fenced>


 

Indented code block containing fenced code block sample:

	 
	<Fenced>
	 

Fenced code block with indented code block sample:

 
Some text

	Indented code block sample code
 

Fenced code block with long markers:

 
Fenced
 

Fenced code block with fenced code block markers of different length in it:

 
In code block
 
Still in code block
 
Still in code block
 

Fenced code block with Markdown header and horizontal rule:

 
#test
---
 

Fenced code block with link definitions, footnote definition and
abbreviation definitions:

 
[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language
 

* In a list item with smalish indent:

   
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
   

With HTML content.

 
<b>bold</b>
 

Bug with block level elements in this case:
 
  <div>
  </div>
 

Indented code block of a fenced code block:

     
	haha!
	 

With class:

 html
<b>bold</b>
 

  html
<b>bold</b>
 

 .html
<b>bold</b>
 

  .html
<b>bold</b>
 

With extra attribute block:

 {.html}
<b>bold</b>
 

  {.html #codeid}
<b>bold</b>
 

  .html{.bold}
<div>
 
  
  .html {#codeid}
</div>
 > Example:
> 
>     sub status {
>         print "working";
>     }
> 
> Or:
> 
>     sub status {
>         return "working";
>     }

*	List Item:

		code block

		with a blank line

	within a list item.

*       code block
        as first element of a list item

*	List Item:
	
		code block with whitespace on preceding line
    Codeblock on second line
    <?php
    echo "hello!";
    ?>

foo bar

    <?php
    echo "hello!";

lorem ipsum

    echo "hello!";
    ?>
    
lorem ipsum	code block on the first line
	
Regular text.

    code block indented by spaces

Regular text.

	the lines in this block  
	all contain trailing spaces  

Regular Text.

	code block on the last line<test a=" content of attribute ">

Fix for backticks within HTML tag: <span attr='ticks'>like this</span>

Here's how you put   backticks   in a code span.A simple definition list:

Term 1
:   Definition 1

Term 2
:   Definition 2

With multiple terms:

Term 1
Term 2
:   Definition 1

Term 3
Term 4
:   Definition 2

With multiple definitions:

Term 1
:   Definition 1
:   Definition 2

Term 2
:   Definition 3
:   Definition 4

With multiple lines per definition:

Term 1
:   Definition 1 line 1 ...
Definition 1 line 2
:   Definition 2 line 1 ...
Definition 2 line 2

Term 2
:   Definition 3 line 2 ...
    Definition 3 line 2
:   Definition 4 line 2 ...
    Definition 4 line 2

With paragraphs:

Term 1

:   Definition 1 (paragraph)

Term 2

:   Definition 2 (paragraph)

With multiple paragraphs:

Term 1

:   Definition 1 paragraph 1 line 1 ...
	Definition 1 paragraph 1 line 2

    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)

    Definition 1 paragraph 2 line 1 ...
Definition 1 paragraph 2 line 2 (lazy)

* * *

A mix:

Term 1
Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)
    
    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

:   Definition 2 paragraph 1 line 1 ...
Definition 2 paragraph 1 line 2 (lazy)

Term 3
:   Definition 3 (no paragraph)
:   Definition 4 (no paragraph)
:   Definition 5 line 1 ...
    Definition 5 line 2 (no paragraph)

:   Definition 6 paragraph 1 line 1 ...
Definition 6 paragraph 1 line 2
:   Definition 7 (no paragraph)
:   Definition 8 paragraph 1 line 1 (forced paragraph) ...
    Definition 8 paragraph 1 line 2
    
    Definition 8 paragraph 2 line 1
    
Term 4
:   Definition 9 paragraph 1 line 1 (forced paragraph) ...
    Definition 9 paragraph 1 line 2
    
    Definition 9 paragraph 2 line 1
:   Definition 10 (no paragraph)

* * *

Special cases:

Term

:       code block
        as first element of a definition<michel.fortin@michelf.ca>

International domain names: <help@tūdaliņ.lv>


## Some weird valid email addresses

<abc.123@example.com>

<1234567890@example.com>

<_______@example.com>

<abc+mailbox/department=shipping@example.com>

<!#$%&'*+-/=?^_.{|}@example.com> (all of these characters are allowed)

<"abc@def"@example.com> (anything goes inside quotation marks)

<"Fred Bloggs"@example.com>

<jsmith@[192.0.2.1]>

<"A"@example.com>Combined emphasis:

1.  ***test test***
2.  ___test test___
3.  *test **test***
4.  **test *test***
5.  ***test* test**
6.  ***test** test*
7.  ***test* test**
8.  **test *test***
9.  *test **test***
10. _test __test___
11. __test _test___
12. ___test_ test__
13. ___test__ test_
14. ___test_ test__
15. __test _test___
16. _test __test___
17. *test __test__*
18. **test _test_**
19. **_test_ test**
20. *__test__ test*
21. **_test_ test**
22. **test _test_**
23. *test __test__*
24. _test **test**_
25. __test *test*__
26. __*test* test__
27. _**test** test_
28. __*test* test__
29. __test *test*__
30. _test **test**_


Incorrect nesting:

1.  *test  **test*  test**
2.  _test  __test_  test__
3.  **test  *test** test*
4.  __test  _test__ test_
5.  *test   *test*  test*
6.  _test   _test_  test_
7.  **test **test** test**
8.  __test __test__ test__
9. _**some text_**
10. *__some text*__
11. **_some text**_
12. *__some text*__

No emphasis:

1.  test*  test  *test
2.  test** test **test
3.  test_  test  _test
4.  test__ test __test



Middle-word emphasis (asterisks):

1.  *a*b
2.   a*b*
3.   a*b*c
4. **a**b
5.   a**b**
6.   a**b**c


Middle-word emphasis (underscore):

1.  _a_b
2.   a_b_
3.   a_b_c
4. __a__b
5.   a__b__
6.   a__b__c

my_precious_file.txt


## Tricky Cases

E**. **Test** TestTestTest

E**. **Test** Test Test Test


## Overlong emphasis

Name: ____________  
Organization: ____  
Region/Country: __

_____Cut here_____

____Cut here____

# Regression

_**Note**_: This _is emphasis_.
With asterisks

 * List item
 *
 * List item

With numbers

1. List item
2.
3. List item

With hyphens

- List item
-
- List item

With asterisks

 * List item
 * List item
 *

With numbers

1. List item
2. List item
3.

With hyphens

- List item
- List item
-
This is the first paragraph.[^first]

[^first]:  This is the first note.

* List item one.[^second]
* List item two.[^third]

[^third]: This is the third note, defined out of order.
[^second]: This is the second note.
[^fourth]: This is the fourth note.

# Header[^fourth]

Some paragraph with a footnote[^1], and another[^2].

[^1]: Content for fifth footnote.
[^2]: Content for sixth footnote spaning on 
    three lines, with some span-level markup like
    _emphasis_, a [link][].

[link]: http://michelf.ca/

Another paragraph with a named footnote[^fn-name].

[^fn-name]:
    Footnote beginning on the line next to the marker.

This paragraph should not have a footnote marker since 
the footnote is undefined.[^3]

This paragraph has a second footnote marker to footnote number one.[^1]

This paragraph links to a footnote with plenty of 
block-level content.[^block]

[^block]:
	Paragraph.
	
	*   List item
	
	> Blockquote
	
	    Code block

This paragraph host the footnote reference within a 
footnote test[^reference].

[^reference]:
	This footnote has a footnote of its own.[^nested]

[^nested]:
	This footnote should appear even though it is referenced
	from another footnote. But [^reference] should be litteral
	since the footnote with that name has already been used.

 - - -

Testing unusual footnote name[^1$^!"'].

[^1$^!"']: Haha!

 - - -
 
Footnotes mixed with images[^image-mixed]
![1800 Travel][img6]
![1830 Travel][img7]

[img6]: images/MGR-1800-travel.jpeg "Travel Speeds in 1800"
[^image-mixed]: Footnote Content
[img7]: images/MGR-1830-travel.jpeg "Travel Speeds in 1830"
In Markdown 1.0.0 and earlier. Version
8. This line turns into a list item.
Because a hard-wrapped line in the
middle of a paragraph looked like a
list item.

Here's one with a bullet.
* criminey.
Header  {#id1}
======

Header  { #id2}
------

### Header  {#id3 }
#### Header ##  { #id4 }

 - - -

Header  {.cl}
======

Header  { .cl}
------

### Header  {.cl }
#### Header ##  { .cl }

 - - -

Header  {.cl.class}
======

Header  { .cl .class}
------

### Header  {.cl .class }
#### Header ##  { .cl.class }

 - - -

Header  {#id5.cl.class}
======

Header  { #id6 .cl .class}
------

### Header  {.cl.class#id7 }
#### Header ##  { .cl.class#id8 }
Header
======

Header
------

### Header

 - - -

Header
======
Paragraph

Header
------
Paragraph

### Header
Paragraph

 - - -

Paragraph
Header
======
Paragraph

Paragraph
Header
------
Paragraph

Paragraph
### Header
ParagraphDashes:

---

 ---
 
  ---

   ---

	---

- - -

 - - -
 
  - - -

   - - -

	- - -


Asterisks:

***

 ***
 
  ***

   ***

	***

* * *

 * * *
 
  * * *

   * * *

	* * *


Underscores:

___

 ___
 
  ___

   ___

    ___

_ _ _

 _ _ _
 
  _ _ _

   _ _ _

    _ _ _
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")

Inline within a paragraph: [alt text](/url/).

![alt text](/url/  "title preceded by two spaces")

![alt text](/url/  "title has spaces afterward"  )

![alt text](</url/>)

![alt text](</url/> "with a title").

![Empty]()

![this is a stupid URL](http://example.com/(parens).jpg)


![alt text][foo]

  [foo]: /url/

![alt text][bar]

  [bar]: /url/ "Title here"Simple block on one line:

<div>foo</div>

And nested without indentation:

<div>
<div>
<div>
foo
</div>
<div style=">"/>
</div>
<div>bar</div>
</div>

And with attributes:

<div>
	<div id="foo">
	</div>
</div>

This was broken in 1.0.2b7:

<div class="inlinepage">
<div class="toggleableend">
foo
</div>
</div>
Here's a simple block:

<div>
	foo
</div>

This should be a code block, though:

	<div>
		foo
	</div>

As should this:

	<div>foo</div>

Now, nested:

<div>
	<div>
		<div>
			foo
		</div>
	</div>
</div>

This should just be an HTML comment:

<!-- Comment -->

Multiline:

<!--
Blah
Blah
-->

Code block:

	<!-- Comment -->

Just plain comment, with trailing spaces on the line:

<!-- foo -->   

Code:

	<hr />
	
Hr's:

<hr>

<hr/>

<hr />

<hr>   

<hr/>  

<hr /> 

<hr class="foo" id="bar" />

<hr class="foo" id="bar"/>

<hr class="foo" id="bar" >

<abbr title=" **Attribute Content Is Not A Code Span** ">ACINACS</abbr>

<abbr title="first backtick!">SB</abbr> 
<abbr title="second backtick!">SB</abbr>Paragraph one.

<!-- This is a simple comment -->

<!--
	This is another comment.
-->

Paragraph two.

<!-- one comment block -- -- with two comments -->

The end.
# Markdown inside code blocks

<div markdown="1">
foo
</div>

<div markdown='1'>
foo
</div>

<div markdown=1>
foo
</div>

<table>
<tr><td markdown="1">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="span">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="block">test _emphasis_ (block)</td></tr>
</table>

## More complicated

<table>
<tr><td markdown="1">
* this is _not_ a list item</td></tr>
<tr><td markdown="span">
* this is _not_ a list item</td></tr>
<tr><td markdown="block">
* this _is_ a list item
</td></tr>
</table>

## With indent

<div>
    <div markdown="1">
    This text is no code block: if it was, the 
    closing <div> would be too and the HTML block 
    would be invalid.

    Markdown content in HTML blocks is assumed to be 
    indented the same as the block opening tag.

    **This should be the third paragraph after the header.**
    </div>
</div>

## Code block with rogue </div>s in Markdown code span and block

<div>
    <div markdown="1">

    This is a code block however:

        </div>

    Funny isn't it? Here is a code span: </div>.

    </div>
</div>

<div>
  <div markdown="1">
    * List item, not a code block

Some text

      This is a code block.
  </div>
</div>

## No code block in markdown span mode

<p markdown="1">
    This is not a code block since Markdown parse paragraph 
    content as span. Code spans like </p> are allowed though.
</p>

<p markdown="1">_Hello_ _world_</p>

## Preserving attributes and tags on more than one line:

<p class="test" markdown="1" 
id="12">
Some _span_ content.
</p>


## Header confusion bug

<table class="canvas">
<tr>
<td id="main" markdown="1">Hello World!
============

Hello World!</td>
</tr>
</table>
Here is a block tag ins:

<ins>
<p>Some text</p>
</ins>

<ins>And here it is inside a paragraph.</ins>

And here it is <ins>in the middle of</ins> a paragraph.

<del>
<p>Some text</p>
</del>

<del>And here is ins as a paragraph.</del>

And here it is <del>in the middle of</del> a paragraph.
		    GNU GENERAL PUBLIC LICENSE
		       Version 2, June 1991

 Copyright (C) 1989, 1991 Free Software Foundation, Inc.,
 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

			    Preamble

  The licenses for most software are designed to take away your
freedom to share and change it.  By contrast, the GNU General Public
License is intended to guarantee your freedom to share and change free
software--to make sure the software is free for all its users.  This
General Public License applies to most of the Free Software
Foundation's software and to any other program whose authors commit to
using it.  (Some other Free Software Foundation software is covered by
the GNU Lesser General Public License instead.)  You can apply it to
your programs, too.

  When we speak of free software, we are referring to freedom, not
price.  Our General Public Licenses are designed to make sure that you
have the freedom to distribute copies of free software (and charge for
this service if you wish), that you receive source code or can get it
if you want it, that you can change the software or use pieces of it
in new free programs; and that you know you can do these things.

  To protect your rights, we need to make restrictions that forbid
anyone to deny you these rights or to ask you to surrender the rights.
These restrictions translate to certain responsibilities for you if you
distribute copies of the software, or if you modify it.

  For example, if you distribute copies of such a program, whether
gratis or for a fee, you must give the recipients all the rights that
you have.  You must make sure that they, too, receive or can get the
source code.  And you must show them these terms so they know their
rights.

  We protect your rights with two steps: (1) copyright the software, and
(2) offer you this license which gives you legal permission to copy,
distribute and/or modify the software.

  Also, for each author's protection and ours, we want to make certain
that everyone understands that there is no warranty for this free
software.  If the software is modified by someone else and passed on, we
want its recipients to know that what they have is not the original, so
that any problems introduced by others will not reflect on the original
authors' reputations.

  Finally, any free program is threatened constantly by software
patents.  We wish to avoid the danger that redistributors of a free
program will individually obtain patent licenses, in effect making the
program proprietary.  To prevent this, we have made it clear that any
patent must be licensed for everyone's free use or not licensed at all.

  The precise terms and conditions for copying, distribution and
modification follow.

		    GNU GENERAL PUBLIC LICENSE
   TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

  0. This License applies to any program or other work which contains
a notice placed by the copyright holder saying it may be distributed
under the terms of this General Public License.  The "Program", below,
refers to any such program or work, and a "work based on the Program"
means either the Program or any derivative work under copyright law:
that is to say, a work containing the Program or a portion of it,
either verbatim or with modifications and/or translated into another
language.  (Hereinafter, translation is included without limitation in
the term "modification".)  Each licensee is addressed as "you".

Activities other than copying, distribution and modification are not
covered by this License; they are outside its scope.  The act of
running the Program is not restricted, and the output from the Program
is covered only if its contents constitute a work based on the
Program (independent of having been made by running the Program).
Whether that is true depends on what the Program does.

  1. You may copy and distribute verbatim copies of the Program's
source code as you receive it, in any medium, provided that you
conspicuously and appropriately publish on each copy an appropriate
copyright notice and disclaimer of warranty; keep intact all the
notices that refer to this License and to the absence of any warranty;
and give any other recipients of the Program a copy of this License
along with the Program.

You may charge a fee for the physical act of transferring a copy, and
you may at your option offer warranty protection in exchange for a fee.

  2. You may modify your copy or copies of the Program or any portion
of it, thus forming a work based on the Program, and copy and
distribute such modifications or work under the terms of Section 1
above, provided that you also meet all of these conditions:

    a) You must cause the modified files to carry prominent notices
    stating that you changed the files and the date of any change.

    b) You must cause any work that you distribute or publish, that in
    whole or in part contains or is derived from the Program or any
    part thereof, to be licensed as a whole at no charge to all third
    parties under the terms of this License.

    c) If the modified program normally reads commands interactively
    when run, you must cause it, when started running for such
    interactive use in the most ordinary way, to print or display an
    announcement including an appropriate copyright notice and a
    notice that there is no warranty (or else, saying that you provide
    a warranty) and that users may redistribute the program under
    these conditions, and telling the user how to view a copy of this
    License.  (Exception: if the Program itself is interactive but
    does not normally print such an announcement, your work based on
    the Program is not required to print an announcement.)

These requirements apply to the modified work as a whole.  If
identifiable sections of that work are not derived from the Program,
and can be reasonably considered independent and separate works in
themselves, then this License, and its terms, do not apply to those
sections when you distribute them as separate works.  But when you
distribute the same sections as part of a whole which is a work based
on the Program, the distribution of the whole must be on the terms of
this License, whose permissions for other licensees extend to the
entire whole, and thus to each and every part regardless of who wrote it.

Thus, it is not the intent of this section to claim rights or contest
your rights to work written entirely by you; rather, the intent is to
exercise the right to control the distribution of derivative or
collective works based on the Program.

In addition, mere aggregation of another work not based on the Program
with the Program (or with a work based on the Program) on a volume of
a storage or distribution medium does not bring the other work under
the scope of this License.

  3. You may copy and distribute the Program (or a work based on it,
under Section 2) in object code or executable form under the terms of
Sections 1 and 2 above provided that you also do one of the following:

    a) Accompany it with the complete corresponding machine-readable
    source code, which must be distributed under the terms of Sections
    1 and 2 above on a medium customarily used for software interchange; or,

    b) Accompany it with a written offer, valid for at least three
    years, to give any third party, for a charge no more than your
    cost of physically performing source distribution, a complete
    machine-readable copy of the corresponding source code, to be
    distributed under the terms of Sections 1 and 2 above on a medium
    customarily used for software interchange; or,

    c) Accompany it with the information you received as to the offer
    to distribute corresponding source code.  (This alternative is
    allowed only for noncommercial distribution and only if you
    received the program in object code or executable form with such
    an offer, in accord with Subsection b above.)

The source code for a work means the preferred form of the work for
making modifications to it.  For an executable work, complete source
code means all the source code for all modules it contains, plus any
associated interface definition files, plus the scripts used to
control compilation and installation of the executable.  However, as a
special exception, the source code distributed need not include
anything that is normally distributed (in either source or binary
form) with the major components (compiler, kernel, and so on) of the
operating system on which the executable runs, unless that component
itself accompanies the executable.

If distribution of executable or object code is made by offering
access to copy from a designated place, then offering equivalent
access to copy the source code from the same place counts as
distribution of the source code, even though third parties are not
compelled to copy the source along with the object code.

  4. You may not copy, modify, sublicense, or distribute the Program
except as expressly provided under this License.  Any attempt
otherwise to copy, modify, sublicense or distribute the Program is
void, and will automatically terminate your rights under this License.
However, parties who have received copies, or rights, from you under
this License will not have their licenses terminated so long as such
parties remain in full compliance.

  5. You are not required to accept this License, since you have not
signed it.  However, nothing else grants you permission to modify or
distribute the Program or its derivative works.  These actions are
prohibited by law if you do not accept this License.  Therefore, by
modifying or distributing the Program (or any work based on the
Program), you indicate your acceptance of this License to do so, and
all its terms and conditions for copying, distributing or modifying
the Program or works based on it.

  6. Each time you redistribute the Program (or any work based on the
Program), the recipient automatically receives a license from the
original licensor to copy, distribute or modify the Program subject to
these terms and conditions.  You may not impose any further
restrictions on the recipients' exercise of the rights granted herein.
You are not responsible for enforcing compliance by third parties to
this License.

  7. If, as a consequence of a court judgment or allegation of patent
infringement or for any other reason (not limited to patent issues),
conditions are imposed on you (whether by court order, agreement or
otherwise) that contradict the conditions of this License, they do not
excuse you from the conditions of this License.  If you cannot
distribute so as to satisfy simultaneously your obligations under this
License and any other pertinent obligations, then as a consequence you
may not distribute the Program at all.  For example, if a patent
license would not permit royalty-free redistribution of the Program by
all those who receive copies directly or indirectly through you, then
the only way you could satisfy both it and this License would be to
refrain entirely from distribution of the Program.

If any portion of this section is held invalid or unenforceable under
any particular circumstance, the balance of the section is intended to
apply and the section as a whole is intended to apply in other
circumstances.

It is not the purpose of this section to induce you to infringe any
patents or other property right claims or to contest validity of any
such claims; this section has the sole purpose of protecting the
integrity of the free software distribution system, which is
implemented by public license practices.  Many people have made
generous contributions to the wide range of software distributed
through that system in reliance on consistent application of that
system; it is up to the author/donor to decide if he or she is willing
to distribute software through any other system and a licensee cannot
impose that choice.

This section is intended to make thoroughly clear what is believed to
be a consequence of the rest of this License.

  8. If the distribution and/or use of the Program is restricted in
certain countries either by patents or by copyrighted interfaces, the
original copyright holder who places the Program under this License
may add an explicit geographical distribution limitation excluding
those countries, so that distribution is permitted only in or among
countries not thus excluded.  In such case, this License incorporates
the limitation as if written in the body of this License.

  9. The Free Software Foundation may publish revised and/or new versions
of the General Public License from time to time.  Such new versions will
be similar in spirit to the present version, but may differ in detail to
address new problems or concerns.

Each version is given a distinguishing version number.  If the Program
specifies a version number of this License which applies to it and "any
later version", you have the option of following the terms and conditions
either of that version or of any later version published by the Free
Software Foundation.  If the Program does not specify a version number of
this License, you may choose any version ever published by the Free Software
Foundation.

  10. If you wish to incorporate parts of the Program into other free
programs whose distribution conditions are different, write to the author
to ask for permission.  For software which is copyrighted by the Free
Software Foundation, write to the Free Software Foundation; we sometimes
make exceptions for this.  Our decision will be guided by the two goals
of preserving the free status of all derivatives of our free software and
of promoting the sharing and reuse of software generally.

			    NO WARRANTY

  11. BECAUSE THE PROGRAM IS LICENSED FREE OF CHARGE, THERE IS NO WARRANTY
FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW.  EXCEPT WHEN
OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES
PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED
OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.  THE ENTIRE RISK AS
TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU.  SHOULD THE
PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING,
REPAIR OR CORRECTION.

  12. IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING
WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MAY MODIFY AND/OR
REDISTRIBUTE THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES,
INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING
OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED
TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY
YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER
PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES.

		     END OF TERMS AND CONDITIONS

	    How to Apply These Terms to Your New Programs

  If you develop a new program, and you want it to be of the greatest
possible use to the public, the best way to achieve this is to make it
free software which everyone can redistribute and change under these terms.

  To do so, attach the following notices to the program.  It is safest
to attach them to the start of each source file to most effectively
convey the exclusion of warranty; and each file should have at least
the "copyright" line and a pointer to where the full notice is found.

    <one line to give the program's name and a brief idea of what it does.>
    Copyright (C) <year>  <name of author>

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

Also add information on how to contact you by electronic and paper mail.

If the program is interactive, make it output a short notice like this
when it starts in an interactive mode:

    Gnomovision version 69, Copyright (C) year name of author
    Gnomovision comes with ABSOLUTELY NO WARRANTY; for details type show w'.
    This is free software, and you are welcome to redistribute it
    under certain conditions; type show c' for details.

The hypothetical commands show w' and show c' should show the appropriate
parts of the General Public License.  Of course, the commands you use may
be called something other than show w' and show c'; they could even be
mouse-clicks or menu items--whatever suits your program.

You should also get your employer (if you work as a programmer) or your
school, if any, to sign a "copyright disclaimer" for the program, if
necessary.  Here is a sample; alter the names:

  Yoyodyne, Inc., hereby disclaims all copyright interest in the program
  Gnomovision' (which makes passes at compilers) written by James Hacker.

  <signature of Ty Coon>, 1 April 1989
  Ty Coon, President of Vice

This General Public License does not permit incorporating your program into
proprietary programs.  If your program is a subroutine library, you may
consider it more useful to permit linking proprietary applications with the
library.  If this is what you want to do, use the GNU Lesser General
Public License instead of this License.
This is an [inline link](/url "title"){.class #inline-link}.

This is a [reference link][refid].

This is an ![inline image](/img "title"){.class #inline-img}.

This is a ![reference image][refid].

[refid]: /path/to/something (Title) { .class #ref data-key=val }

Just a [URL](/url/).

[URL and title](/url/ "title").

[URL and title](/url/  "title preceded by two spaces").

[URL and title](/url/	"title preceded by a tab").

[URL and title](/url/ "title has spaces afterward"  ).

[URL wrapped in angle brackets](</url/>).

[URL w/ angle brackets + title](</url/> "Here's the title").

[Empty]().

[With parens in the URL](http://en.wikipedia.org/wiki/WIMP_(computing))

(With outer parens and [parens in url](/foo(bar)))


[With parens in the URL](/foo(bar) "and a title")

(With outer parens and [parens in url](/foo(bar) "and a title"))
Foo [bar] [1].

Foo [bar][1].

Foo [bar]
[1].

[1]: /url/  "Title"


With [embedded [brackets]] [b].


Indented [once][].

Indented [twice][].

Indented [thrice][].

Indented [four][] times.

 [once]: /url

  [twice]: /url

   [thrice]: /url

    [four]: /url


[b]: /url/

* * *

[this] [this] should work

So should [this][this].

And [this] [].

And [this][].

And [this].

But not [that] [].

Nor [that][].

Nor [that].

[Something in brackets like [this][] should work]

[Same with [this].]

In this case, [this](/somethingelse/) points to something else.

Backslashing should suppress \[this] and [this\].

[this]: foo


* * *

Here's one where the [link
breaks] across lines.

Here's another where the [link 
breaks] across lines, but with a line-ending space.


[link breaks]: /url/
This is the [simple case].

[simple case]: /simple



This one has a [line
break].

This one has a [line 
break] with a line-ending space.

[line break]: /foo


[this] [that] and the [other]

[this]: /this
[that]: /that
[other]: /other
Foo [bar][].

Foo [bar](/url/ "Title with "quotes" inside").


  [bar]: /url/ "Title with "quotes" inside"

Markdown: Basics
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a class="selected" title="Markdown Basics">Basics</a></li>
    <li><a href="/projects/markdown/syntax" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


Getting the Gist of Markdown's Formatting Syntax
------------------------------------------------

This page offers a brief overview of what it's like to use Markdown.
The [syntax page] [s] provides complete, detailed documentation for
every feature, but Markdown should be very easy to pick up simply by
looking at a few examples of it in action. The examples on this page
are written in a before/after style, showing example syntax and the
HTML output produced by Markdown.

It's also helpful to simply try Markdown out; the [Dingus] [d] is a
web application that allows you type your own Markdown-formatted text
and translate it to XHTML.

**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL] [src].

  [s]: /projects/markdown/syntax  "Markdown Syntax"
  [d]: /projects/markdown/dingus  "Markdown Dingus"
  [src]: /projects/markdown/basics.text


## Paragraphs, Headers, Blockquotes ##

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

Markdown offers two styles of headers: *Setext* and *atx*.
Setext-style headers for <h1> and <h2> are created by
"underlining" with equal signs (=) and hyphens (-), respectively.
To create an atx-style header, you put 1-6 hash marks (#) at the
beginning of the line -- the number of hashes equals the resulting
HTML header level.

Blockquotes are indicated using email-style '>' angle brackets.

Markdown:

    A First Level Header
    ====================
    
    A Second Level Header
    ---------------------

    Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.

    The quick brown fox jumped over the lazy
    dog's back.
    
    ### Header 3

    > This is a blockquote.
    > 
    > This is the second paragraph in the blockquote.
    >
    > ## This is an H2 in a blockquote


Output:

    <h1>A First Level Header</h1>
    
    <h2>A Second Level Header</h2>
    
    <p>Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.</p>
    
    <p>The quick brown fox jumped over the lazy
    dog's back.</p>
    
    <h3>Header 3</h3>
    
    <blockquote>
        <p>This is a blockquote.</p>
        
        <p>This is the second paragraph in the blockquote.</p>
        
        <h2>This is an H2 in a blockquote</h2>
    </blockquote>



### Phrase Emphasis ###

Markdown uses asterisks and underscores to indicate spans of emphasis.

Markdown:

    Some of these words *are emphasized*.
    Some of these words _are emphasized also_.
    
    Use two asterisks for **strong emphasis**.
    Or, if you prefer, __use two underscores instead__.

Output:

    <p>Some of these words <em>are emphasized</em>.
    Some of these words <em>are emphasized also</em>.</p>
    
    <p>Use two asterisks for <strong>strong emphasis</strong>.
    Or, if you prefer, <strong>use two underscores instead</strong>.</p>
   


## Lists ##

Unordered (bulleted) lists use asterisks, pluses, and hyphens (*,
+, and -) as list markers. These three markers are
interchangable; this:

    *   Candy.
    *   Gum.
    *   Booze.

this:

    +   Candy.
    +   Gum.
    +   Booze.

and this:

    -   Candy.
    -   Gum.
    -   Booze.

all produce the same output:

    <ul>
    <li>Candy.</li>
    <li>Gum.</li>
    <li>Booze.</li>
    </ul>

Ordered (numbered) lists use regular numbers, followed by periods, as
list markers:

    1.  Red
    2.  Green
    3.  Blue

Output:

    <ol>
    <li>Red</li>
    <li>Green</li>
    <li>Blue</li>
    </ol>

If you put blank lines between items, you'll get <p> tags for the
list item text. You can create multi-paragraph list items by indenting
the paragraphs by 4 spaces or 1 tab:

    *   A list item.
    
        With multiple paragraphs.

    *   Another item in the list.

Output:

    <ul>
    <li><p>A list item.</p>
    <p>With multiple paragraphs.</p></li>
    <li><p>Another item in the list.</p></li>
    </ul>
    


### Links ###

Markdown supports two styles for creating links: *inline* and
*reference*. With both styles, you use square brackets to delimit the
text you want to turn into a link.

Inline-style links use parentheses immediately after the link text.
For example:

    This is an [example link](http://example.com/).

Output:

    <p>This is an <a href="http://example.com/">
    example link</a>.</p>

Optionally, you may include a title attribute in the parentheses:

    This is an [example link](http://example.com/ "With a Title").

Output:

    <p>This is an <a href="http://example.com/" title="With a Title">
    example link</a>.</p>

Reference-style links allow you to refer to your links by names, which
you define elsewhere in your document:

    I get 10 times more traffic from [Google][1] than from
    [Yahoo][2] or [MSN][3].

    [1]: http://google.com/        "Google"
    [2]: http://search.yahoo.com/  "Yahoo Search"
    [3]: http://search.msn.com/    "MSN Search"

Output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from <a href="http://search.yahoo.com/"
    title="Yahoo Search">Yahoo</a> or <a href="http://search.msn.com/"
    title="MSN Search">MSN</a>.</p>

The title attribute is optional. Link names may contain letters,
numbers and spaces, but are *not* case sensitive:

    I start my morning with a cup of coffee and
    [The New York Times][NY Times].

    [ny times]: http://www.nytimes.com/

Output:

    <p>I start my morning with a cup of coffee and
    <a href="http://www.nytimes.com/">The New York Times</a>.</p>


### Images ###

Image syntax is very much like link syntax.

Inline (titles are optional):

    ![alt text](/path/to/img.jpg "Title")

Reference-style:

    ![alt text][id]

    [id]: /path/to/img.jpg "Title"

Both of the above examples produce the same output:

    <img src="/path/to/img.jpg" alt="alt text" title="Title" />



### Code ###

In a regular paragraph, you can create code span by wrapping text in
backtick quotes. Any ampersands (&) and angle brackets (< or
>) will automatically be translated into HTML entities. This makes
it easy to use Markdown to write about HTML example code:

    I strongly recommend against using any <blink> tags.

    I wish SmartyPants used named entities like &mdash;
    instead of decimal-encoded entites like &#8212;.

Output:

    <p>I strongly recommend against using any
    <code>&lt;blink&gt;</code> tags.</p>
    
    <p>I wish SmartyPants used named entities like
    <code>&amp;mdash;</code> instead of decimal-encoded
    entites like <code>&amp;#8212;</code>.</p>


To specify an entire block of pre-formatted code, indent every line of
the block by 4 spaces or 1 tab. Just like with code spans, &, <,
and > characters will be escaped automatically.

Markdown:

    If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:

        <blockquote>
            <p>For example.</p>
        </blockquote>

Output:

    <p>If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:</p>
    
    <pre><code>&lt;blockquote&gt;
        &lt;p&gt;For example.&lt;/p&gt;
    &lt;/blockquote&gt;
    </code></pre>
Markdown: Syntax
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a href="/projects/markdown/basics" title="Markdown Basics">Basics</a></li>
    <li><a class="selected" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


*   [Overview](#overview)
    *   [Philosophy](#philosophy)
    *   [Inline HTML](#html)
    *   [Automatic Escaping for Special Characters](#autoescape)
*   [Block Elements](#block)
    *   [Paragraphs and Line Breaks](#p)
    *   [Headers](#header)
    *   [Blockquotes](#blockquote)
    *   [Lists](#list)
    *   [Code Blocks](#precode)
    *   [Horizontal Rules](#hr)
*   [Span Elements](#span)
    *   [Links](#link)
    *   [Emphasis](#em)
    *   [Code](#code)
    *   [Images](#img)
*   [Miscellaneous](#misc)
    *   [Backslash Escapes](#backslash)
    *   [Automatic Links](#autolink)


**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL][src].

  [src]: /projects/markdown/syntax.text

* * *

<h2 id="overview">Overview</h2>

<h3 id="philosophy">Philosophy</h3>

Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

Readability, however, is emphasized above all else. A Markdown-formatted
document should be publishable as-is, as plain text, without looking
like it's been marked up with tags or formatting instructions. While
Markdown's syntax has been influenced by several existing text-to-HTML
filters -- including [Setext] [1], [atx] [2], [Textile] [3], [reStructuredText] [4],
[Grutatext] [5], and [EtText] [6] -- the single biggest source of
inspiration for Markdown's syntax is the format of plain text email.

  [1]: http://docutils.sourceforge.net/mirror/setext.html
  [2]: http://www.aaronsw.com/2002/atx/
  [3]: http://textism.com/tools/textile/
  [4]: http://docutils.sourceforge.net/rst.html
  [5]: http://www.triptico.com/software/grutatxt.html
  [6]: http://ettext.taint.org/doc/

To this end, Markdown's syntax is comprised entirely of punctuation
characters, which punctuation characters have been carefully chosen so
as to look like what they mean. E.g., asterisks around a word actually
look like \*emphasis\*. Markdown lists look like, well, lists. Even
blockquotes look like quoted passages of text, assuming you've ever
used email.



<h3 id="html">Inline HTML</h3>

Markdown's syntax is intended for one purpose: to be used as a
format for *writing* for the web.

Markdown is not a replacement for HTML, or even close to it. Its
syntax is very small, corresponding only to a very small subset of
HTML tags. The idea is *not* to create a syntax that makes it easier
to insert HTML tags. In my opinion, HTML tags are already easy to
insert. The idea for Markdown is to make it easy to read, write, and
edit prose. HTML is a *publishing* format; Markdown is a *writing*
format. Thus, Markdown's formatting syntax only addresses issues that
can be conveyed in plain text.

For any markup that is not covered by Markdown's syntax, you simply
use HTML itself. There's no need to preface it or delimit it to
indicate that you're switching from Markdown to HTML; you just use
the tags.

The only restrictions are that block-level HTML elements -- e.g. <div>,
<table>, <pre>, <p>, etc. -- must be separated from surrounding
content by blank lines, and the start and end tags of the block should
not be indented with tabs or spaces. Markdown is smart enough not
to add extra (unwanted) <p> tags around HTML block-level tags.

For example, to add an HTML table to a Markdown article:

    This is a regular paragraph.

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    This is another regular paragraph.

Note that Markdown formatting syntax is not processed within block-level
HTML tags. E.g., you can't use Markdown-style *emphasis* inside an
HTML block.

Span-level HTML tags -- e.g. <span>, <cite>, or <del> -- can be
used anywhere in a Markdown paragraph, list item, or header. If you
want, you can even use HTML tags instead of Markdown formatting; e.g. if
you'd prefer to use HTML <a> or <img> tags instead of Markdown's
link or image syntax, go right ahead.

Unlike block-level HTML tags, Markdown syntax *is* processed within
span-level tags.


<h3 id="autoescape">Automatic Escaping for Special Characters</h3>

In HTML, there are two characters that demand special treatment: <
and &. Left angle brackets are used to start tags; ampersands are
used to denote HTML entities. If you want to use them as literal
characters, you must escape them as entities, e.g. &lt;, and
&amp;.

Ampersands in particular are bedeviling for web writers. If you want to
write about 'AT&T', you need to write 'AT&amp;T'. You even need to
escape ampersands within URLs. Thus, if you want to link to:

    http://images.google.com/images?num=30&q=larry+bird

you need to encode the URL as:

    http://images.google.com/images?num=30&amp;q=larry+bird

in your anchor tag href attribute. Needless to say, this is easy to
forget, and is probably the single most common source of HTML validation
errors in otherwise well-marked-up web sites.

Markdown allows you to use these characters naturally, taking care of
all the necessary escaping for you. If you use an ampersand as part of
an HTML entity, it remains unchanged; otherwise it will be translated
into &amp;.

So, if you want to include a copyright symbol in your article, you can write:

    &copy;

and Markdown will leave it alone. But if you write:

    AT&T

Markdown will translate it to:

    AT&amp;T

Similarly, because Markdown supports [inline HTML](#html), if you use
angle brackets as delimiters for HTML tags, Markdown will treat them as
such. But if you write:

    4 < 5

Markdown will translate it to:

    4 &lt; 5

However, inside Markdown code spans and blocks, angle brackets and
ampersands are *always* encoded automatically. This makes it easy to use
Markdown to write about HTML code. (As opposed to raw HTML, which is a
terrible format for writing about HTML syntax, because every single <
and & in your example code needs to be escaped.)


* * *


<h2 id="block">Block Elements</h2>


<h3 id="p">Paragraphs and Line Breaks</h3>

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing but spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

The implication of the "one or more consecutive lines of text" rule is
that Markdown supports "hard-wrapped" text paragraphs. This differs
significantly from most other text-to-HTML formatters (including Movable
Type's "Convert Line Breaks" option) which translate every line break
character in a paragraph into a <br /> tag.

When you *do* want to insert a <br /> break tag using Markdown, you
end a line with two or more spaces, then type return.

Yes, this takes a tad more effort to create a <br />, but a simplistic
"every line break is a <br />" rule wouldn't work for Markdown.
Markdown's email-style [blockquoting][bq] and multi-paragraph [list items][l]
work best -- and look better -- when you format them with hard breaks.

  [bq]: #blockquote
  [l]:  #list



<h3 id="header">Headers</h3>

Markdown supports two styles of headers, [Setext] [1] and [atx] [2].

Setext-style headers are "underlined" using equal signs (for first-level
headers) and dashes (for second-level headers). For example:

    This is an H1
    =============

    This is an H2
    -------------

Any number of underlining ='s or -'s will work.

Atx-style headers use 1-6 hash characters at the start of the line,
corresponding to header levels 1-6. For example:

    # This is an H1

    ## This is an H2

    ###### This is an H6

Optionally, you may "close" atx-style headers. This is purely
cosmetic -- you can use this if you think it looks better. The
closing hashes don't even need to match the number of hashes
used to open the header. (The number of opening hashes
determines the header level.) :

    # This is an H1 #

    ## This is an H2 ##

    ### This is an H3 ######


<h3 id="blockquote">Blockquotes</h3>

Markdown uses email-style > characters for blockquoting. If you're
familiar with quoting passages of text in an email message, then you
know how to create a blockquote in Markdown. It looks best if you hard
wrap the text and put a > before every line:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    > 
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

Markdown allows you to be lazy and only put the > before the first
line of a hard-wrapped paragraph:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

Blockquotes can be nested (i.e. a blockquote-in-a-blockquote) by
adding additional levels of >:

    > This is the first level of quoting.
    >
    > > This is nested blockquote.
    >
    > Back to the first level.

Blockquotes can contain other Markdown elements, including headers, lists,
and code blocks:

	> ## This is a header.
	> 
	> 1.   This is the first list item.
	> 2.   This is the second list item.
	> 
	> Here's some example code:
	> 
	>     return shell_exec("echo $input | $markdown_script");

Any decent text editor should make email-style quoting easy. For
example, with BBEdit, you can make a selection and choose Increase
Quote Level from the Text menu.


<h3 id="list">Lists</h3>

Markdown supports ordered (numbered) and unordered (bulleted) lists.

Unordered lists use asterisks, pluses, and hyphens -- interchangably
-- as list markers:

    *   Red
    *   Green
    *   Blue

is equivalent to:

    +   Red
    +   Green
    +   Blue

and:

    -   Red
    -   Green
    -   Blue

Ordered lists use numbers followed by periods:

    1.  Bird
    2.  McHale
    3.  Parish

It's important to note that the actual numbers you use to mark the
list have no effect on the HTML output Markdown produces. The HTML
Markdown produces from the above list is:

    <ol>
    <li>Bird</li>
    <li>McHale</li>
    <li>Parish</li>
    </ol>

If you instead wrote the list in Markdown like this:

    1.  Bird
    1.  McHale
    1.  Parish

or even:

    3. Bird
    1. McHale
    8. Parish

you'd get the exact same HTML output. The point is, if you want to,
you can use ordinal numbers in your ordered Markdown lists, so that
the numbers in your source match the numbers in your published HTML.
But if you want to be lazy, you don't have to.

If you do use lazy list numbering, however, you should still start the
list with the number 1. At some point in the future, Markdown may support
starting ordered lists at an arbitrary number.

List markers typically start at the left margin, but may be indented by
up to three spaces. List markers must be followed by one or more spaces
or a tab.

To make lists look nice, you can wrap items with hanging indents:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
        Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
        viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
        Suspendisse id sem consectetuer libero luctus adipiscing.

But if you want to be lazy, you don't have to:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.

If list items are separated by blank lines, Markdown will wrap the
items in <p> tags in the HTML output. For example, this input:

    *   Bird
    *   Magic

will turn into:

    <ul>
    <li>Bird</li>
    <li>Magic</li>
    </ul>

But this:

    *   Bird

    *   Magic

will turn into:

    <ul>
    <li><p>Bird</p></li>
    <li><p>Magic</p></li>
    </ul>

List items may consist of multiple paragraphs. Each subsequent
paragraph in a list item must be intended by either 4 spaces
or one tab:

    1.  This is a list item with two paragraphs. Lorem ipsum dolor
        sit amet, consectetuer adipiscing elit. Aliquam hendrerit
        mi posuere lectus.

        Vestibulum enim wisi, viverra nec, fringilla in, laoreet
        vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
        sit amet velit.

    2.  Suspendisse id sem consectetuer libero luctus adipiscing.

It looks nice if you indent every line of the subsequent
paragraphs, but here again, Markdown will allow you to be
lazy:

    *   This is a list item with two paragraphs.

        This is the second paragraph in the list item. You're
    only required to indent the first line. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit.

    *   Another item in the same list.

To put a blockquote within a list item, the blockquote's >
delimiters need to be indented:

    *   A list item with a blockquote:

        > This is a blockquote
        > inside a list item.

To put a code block within a list item, the code block needs
to be indented *twice* -- 8 spaces or two tabs:

    *   A list item with a code block:

            <code goes here>


It's worth noting that it's possible to trigger an ordered list by
accident, by writing something like this:

    1986. What a great season.

In other words, a *number-period-space* sequence at the beginning of a
line. To avoid this, you can backslash-escape the period:

    1986\. What a great season.



<h3 id="precode">Code Blocks</h3>

Pre-formatted code blocks are used for writing about programming or
markup source code. Rather than forming normal paragraphs, the lines
of a code block are interpreted literally. Markdown wraps a code block
in both <pre> and <code> tags.

To produce a code block in Markdown, simply indent every line of the
block by at least 4 spaces or 1 tab. For example, given this input:

    This is a normal paragraph:

        This is a code block.

Markdown will generate:

    <p>This is a normal paragraph:</p>

    <pre><code>This is a code block.
    </code></pre>

One level of indentation -- 4 spaces or 1 tab -- is removed from each
line of the code block. For example, this:

    Here is an example of AppleScript:

        tell application "Foo"
            beep
        end tell

will turn into:

    <p>Here is an example of AppleScript:</p>

    <pre><code>tell application "Foo"
        beep
    end tell
    </code></pre>

A code block continues until it reaches a line that is not indented
(or the end of the article).

Within a code block, ampersands (&) and angle brackets (< and >)
are automatically converted into HTML entities. This makes it very
easy to include example HTML source code using Markdown -- just paste
it and indent it, and Markdown will handle the hassle of encoding the
ampersands and angle brackets. For example, this:

        <div class="footer">
            &copy; 2004 Foo Corporation
        </div>

will turn into:

    <pre><code>&lt;div class="footer"&gt;
        &amp;copy; 2004 Foo Corporation
    &lt;/div&gt;
    </code></pre>

Regular Markdown syntax is not processed within code blocks. E.g.,
asterisks are just literal asterisks within a code block. This means
it's also easy to use Markdown to write about Markdown's own syntax.



<h3 id="hr">Horizontal Rules</h3>

You can produce a horizontal rule tag (<hr />) by placing three or
more hyphens, asterisks, or underscores on a line by themselves. If you
wish, you may use spaces between the hyphens or asterisks. Each of the
following lines will produce a horizontal rule:

    * * *

    ***

    *****
	
    - - -

    ---------------------------------------

	_ _ _


* * *

<h2 id="span">Span Elements</h2>

<h3 id="link">Links</h3>

Markdown supports two style of links: *inline* and *reference*.

In both styles, the link text is delimited by [square brackets].

To create an inline link, use a set of regular parentheses immediately
after the link text's closing square bracket. Inside the parentheses,
put the URL where you want the link to point, along with an *optional*
title for the link, surrounded in quotes. For example:

    This is [an example](http://example.com/ "Title") inline link.

    [This link](http://example.net/) has no title attribute.

Will produce:

    <p>This is <a href="http://example.com/" title="Title">
    an example</a> inline link.</p>

    <p><a href="http://example.net/">This link</a> has no
    title attribute.</p>

If you're referring to a local resource on the same server, you can
use relative paths:

    See my [About](/about/) page for details.

Reference-style links use a second set of square brackets, inside
which you place a label of your choosing to identify the link:

    This is [an example][id] reference-style link.

You can optionally use a space to separate the sets of brackets:

    This is [an example] [id] reference-style link.

Then, anywhere in the document, you define your link label like this,
on a line by itself:

    [id]: http://example.com/  "Optional Title Here"

That is:

*   Square brackets containing the link identifier (optionally
    indented from the left margin using up to three spaces);
*   followed by a colon;
*   followed by one or more spaces (or tabs);
*   followed by the URL for the link;
*   optionally followed by a title attribute for the link, enclosed
    in double or single quotes.

The link URL may, optionally, be surrounded by angle brackets:

    [id]: <http://example.com/>  "Optional Title Here"

You can put the title attribute on the next line and use extra spaces
or tabs for padding, which tends to look better with longer URLs:

    [id]: http://example.com/longish/path/to/resource/here
        "Optional Title Here"

Link definitions are only used for creating links during Markdown
processing, and are stripped from your document in the HTML output.

Link definition names may constist of letters, numbers, spaces, and punctuation -- but they are *not* case sensitive. E.g. these two links:

	[link text][a]
	[link text][A]

are equivalent.

The *implicit link name* shortcut allows you to omit the name of the
link, in which case the link text itself is used as the name.
Just use an empty set of square brackets -- e.g., to link the word
"Google" to the google.com web site, you could simply write:

	[Google][]

And then define the link:

	[Google]: http://google.com/

Because link names may contain spaces, this shortcut even works for
multiple words in the link text:

	Visit [Daring Fireball][] for more information.

And then define the link:
	
	[Daring Fireball]: http://daringfireball.net/

Link definitions can be placed anywhere in your Markdown document. I
tend to put them immediately after each paragraph in which they're
used, but if you want, you can put them all at the end of your
document, sort of like footnotes.

Here's an example of reference links in action:

    I get 10 times more traffic from [Google] [1] than from
    [Yahoo] [2] or [MSN] [3].

      [1]: http://google.com/        "Google"
      [2]: http://search.yahoo.com/  "Yahoo Search"
      [3]: http://search.msn.com/    "MSN Search"

Using the implicit link name shortcut, you could instead write:

    I get 10 times more traffic from [Google][] than from
    [Yahoo][] or [MSN][].

      [google]: http://google.com/        "Google"
      [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
      [msn]:    http://search.msn.com/    "MSN Search"

Both of the above examples will produce the following HTML output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from
    <a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a>
    or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p>

For comparison, here is the same paragraph written using
Markdown's inline link style:

    I get 10 times more traffic from [Google](http://google.com/ "Google")
    than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or
    [MSN](http://search.msn.com/ "MSN Search").

The point of reference-style links is not that they're easier to
write. The point is that with reference-style links, your document
source is vastly more readable. Compare the above examples: using
reference-style links, the paragraph itself is only 81 characters
long; with inline-style links, it's 176 characters; and as raw HTML,
it's 234 characters. In the raw HTML, there's more markup than there
is text.

With Markdown's reference-style links, a source document much more
closely resembles the final output, as rendered in a browser. By
allowing you to move the markup-related metadata out of the paragraph,
you can add links without interrupting the narrative flow of your
prose.


<h3 id="em">Emphasis</h3>

Markdown treats asterisks (*) and underscores (_) as indicators of
emphasis. Text wrapped with one * or _ will be wrapped with an
HTML <em> tag; double *'s or _'s will be wrapped with an HTML
<strong> tag. E.g., this input:

    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__

will produce:

    <em>single asterisks</em>

    <em>single underscores</em>

    <strong>double asterisks</strong>

    <strong>double underscores</strong>

You can use whichever style you prefer; the lone restriction is that
the same character must be used to open and close an emphasis span.

Emphasis can be used in the middle of a word:

    un*fucking*believable

But if you surround an * or _ with spaces, it'll be treated as a
literal asterisk or underscore.

To produce a literal asterisk or underscore at a position where it
would otherwise be used as an emphasis delimiter, you can backslash
escape it:

    \*this text is surrounded by literal asterisks\*



<h3 id="code">Code</h3>

To indicate a span of code, wrap it with backtick quotes (  ).
Unlike a pre-formatted code block, a code span indicates code within a
normal paragraph. For example:

    Use the printf() function.

will produce:

    <p>Use the <code>printf()</code> function.</p>

To include a literal backtick character within a code span, you can use
multiple backticks as the opening and closing delimiters:

     There is a literal backtick () here.

which will produce this:

    <p><code>There is a literal backtick () here.</code></p>

The backtick delimiters surrounding a code span may include spaces --
one after the opening, one before the closing. This allows you to place
literal backtick characters at the beginning or end of a code span:

	A single backtick in a code span:     
	
	A backtick-delimited string in a code span:   foo  

will produce:

	<p>A single backtick in a code span: <code></code></p>
	
	<p>A backtick-delimited string in a code span: <code>foo</code></p>

With a code span, ampersands and angle brackets are encoded as HTML
entities automatically, which makes it easy to include example HTML
tags. Markdown will turn this:

    Please don't use any <blink> tags.

into:

    <p>Please don't use any <code>&lt;blink&gt;</code> tags.</p>

You can write this:

    &#8212; is the decimal-encoded equivalent of &mdash;.

to produce:

    <p><code>&amp;#8212;</code> is the decimal-encoded
    equivalent of <code>&amp;mdash;</code>.</p>



<h3 id="img">Images</h3>

Admittedly, it's fairly difficult to devise a "natural" syntax for
placing images into a plain text document format.

Markdown uses an image syntax that is intended to resemble the syntax
for links, allowing for two styles: *inline* and *reference*.

Inline image syntax looks like this:

    ![Alt text](/path/to/img.jpg)

    ![Alt text](/path/to/img.jpg "Optional title")

That is:

*   An exclamation mark: !;
*   followed by a set of square brackets, containing the alt
    attribute text for the image;
*   followed by a set of parentheses, containing the URL or path to
    the image, and an optional title attribute enclosed in double
    or single quotes.

Reference-style image syntax looks like this:

    ![Alt text][id]

Where "id" is the name of a defined image reference. Image references
are defined using syntax identical to link references:

    [id]: url/to/image  "Optional title attribute"

As of this writing, Markdown has no syntax for specifying the
dimensions of an image; if this is important to you, you can simply
use regular HTML <img> tags.


* * *


<h2 id="misc">Miscellaneous</h2>

<h3 id="autolink">Automatic Links</h3>

Markdown supports a shortcut style for creating "automatic" links for URLs and email addresses: simply surround the URL or email address with angle brackets. What this means is that if you want to show the actual text of a URL or email address, and also have it be a clickable link, you can do this:

    <http://example.com/>
    
Markdown will turn this into:

    <a href="http://example.com/">http://example.com/</a>

Automatic links for email addresses work similarly, except that
Markdown will also perform a bit of randomized decimal and hex
entity-encoding to help obscure your address from address-harvesting
spambots. For example, Markdown will turn this:

    <address@example.com>

into something like this:

    <a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
    &#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
    &#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
    &#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>

which will render in a browser as a clickable link to "address@example.com".

(This sort of entity-encoding trick will indeed fool many, if not
most, address-harvesting bots, but it definitely won't fool all of
them. It's better than nothing, but an address published in this way
will probably eventually start receiving spam.)



<h3 id="backslash">Backslash Escapes</h3>

Markdown allows you to use backslash escapes to generate literal
characters which would otherwise have special meaning in Markdown's
formatting syntax. For example, if you wanted to surround a word with
literal asterisks (instead of an HTML <em> tag), you can backslashes
before the asterisks, like this:

    \*literal asterisks\*

Markdown provides backslash escapes for the following characters:

    \   backslash
       backtick
    *   asterisk
    _   underscore
    {}  curly braces
    []  square brackets
    ()  parentheses
    #   hash mark
	+	plus sign
	-	minus sign (hyphen)
    .   dot
    !   exclamation mark

# Character Escapes

The MD5 value for + is "26b17225b626fb9238849fd60eabdf60".

# HTML Blocks

<p>test</p>

The MD5 value for <p>test</p> is:

6205333b793f34273d75379350b36826* test
+ test
- test

1. test
2. test

* test
+ test
- test

1. test
2. test
> foo
>
> > bar
>
> foo
Valid nesting:

**[Link](url)**

[**Link**](url)

**[**Link**](url)**

Invalid nesting:

[[Link](url)](url)## Unordered

Asterisks tight:

*	asterisk 1
*	asterisk 2
*	asterisk 3


Asterisks loose:

*	asterisk 1

*	asterisk 2

*	asterisk 3

* * *

Pluses tight:

+	Plus 1
+	Plus 2
+	Plus 3


Pluses loose:

+	Plus 1

+	Plus 2

+	Plus 3

* * *


Minuses tight:

-	Minus 1
-	Minus 2
-	Minus 3


Minuses loose:

-	Minus 1

-	Minus 2

-	Minus 3


## Ordered

Tight:

1.	First
2.	Second
3.	Third

and:

1. One
2. Two
3. Three


Loose using tabs:

1.	First

2.	Second

3.	Third

and using spaces:

1. One

2. Two

3. Three

Multiple paragraphs:

1.	Item 1, graf one.

	Item 2. graf two. The quick brown fox jumped over the lazy dog's
	back.
	
2.	Item 2.

3.	Item 3.



## Nested

*	Tab
	*	Tab
		*	Tab

Here's another:

1. First
2. Second:
	* Fee
	* Fie
	* Foe
3. Third

Same thing but with paragraphs:

1. First

2. Second:
	* Fee
	* Fie
	* Foe

3. Third


This was an error in Markdown 1.0.1:

*	this

	*	sub

	that
[Inline link 1 with parens](/url\(test\) "title").

[Inline link 2 with parens](</url\(test\)> "title").

[Inline link 3 with non-escaped parens](/url(test) "title").

[Inline link 4 with non-escaped parens](</url(test)> "title").

[Reference link 1 with parens][1].

[Reference link 2 with parens][2].

  [1]: /url(test) "title"
  [2]: </url(test)> "title"
This tests for a bug where quotes escaped by PHP when using 
preg_replace with the /e modifier must be correctly unescaped
(hence the _UnslashQuotes function found only in PHP Markdown).



Headers below should appear exactly as they are typed (no backslash
added or removed).

Header "quoted\" again \\""
===========================

Header "quoted\" again \\""
---------------------------

### Header "quoted\" again \\"" ###



Test with tabs for _Detab:

	Code	'block'	with	some	"tabs"	and	"quotes"
[Test](/"style="color:red)
[Test](/'style='color:red)

![](/"style="border-color:red;border-size:1px;border-style:solid)
![](/'style='border-color:red;border-size:1px;border-style:solid)
***This is strong and em.***

So is ***this*** word.

___This is strong and em.___

So is ___this___ word.
# Simple tables

Header 1  | Header 2
--------- | ---------
Cell 1    | Cell 2
Cell 3    | Cell 4

With leading pipes:

| Header 1  | Header 2
| --------- | ---------
| Cell 1    | Cell 2
| Cell 3    | Cell 4

With tailing pipes:

Header 1  | Header 2  |
--------- | --------- |
Cell 1    | Cell 2    |
Cell 3    | Cell 4    |

With leading and tailing pipes:

| Header 1  | Header 2  |
| --------- | --------- |
| Cell 1    | Cell 2    |
| Cell 3    | Cell 4    |

* * *

# One-column one-row table

With leading pipes:

| Header
| -------
| Cell

With tailing pipes:

Header  |
------- |
Cell    |

With leading and tailing pipes:

| Header  |
| ------- |
| Cell    |

* * *

Table alignement:

| Default   | Right     |  Center   |     Left  |
| --------- |:--------- |:---------:| ---------:|
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

Table alignement (alternate spacing):

| Default   | Right     |  Center   |     Left  |
| --------- | :-------- | :-------: | --------: |
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

* * * 

# Empty cells

| Header 1  | Header 2  |
| --------- | --------- |
| A         | B         |
| C         |           |

Header 1  | Header 2
--------- | ---------
A         | B
          | D

* * *

# Missing tailing pipe

Header 1  | Header 2  
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- 
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      

* * *

# Too many pipes in rows

| Header 1  | Header 2  |
| --------- 
| Cell      | Cell      | Extra cell? |
| Cell      | Cell      | Extra cell? |

+	this is a list item
	indented with tabs

+   this is a list item
    indented with spaces

Code:

	this code block is indented by one tab

And:

		this code block is indented by two tabs

And:

	+	this is an example list item
		indented with tabs
	
	+   this is an example list item
	    indented with spaces
> A list within a blockquote:
> 
> *	asterisk 1
> *	asterisk 2
> *	asterisk 3
Paragraph and no space:
* ciao

Paragraph and 1 space:
 * ciao

Paragraph and 3 spaces:
  * ciao

Paragraph and 4 spaces:
   * ciao

Paragraph before header:
#Header

Paragraph before blockquote:
>Some quote.
 .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>


As above: checking for bad interractions with the HTML block parser:

 html
<div>


Some *markdown* formatting.

 html
</div>


Some *markdown*


<div>
    <html>



function test();


<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">

<html>
    <title>

</div>

Two code blocks with no blank line between them:


<div>


<div>


Testing *confusion* with markers in the middle:


<div></div>


Testing mixing with title code blocks


<p>
 
<p>

 
<p>

<p>
 

<Fenced>


Code block starting and ending with empty lines:



<Fenced>




Indented code block containing fenced code block sample:

	
	<Fenced>
	

Fenced code block with indented code block sample:


Some text

	Indented code block sample code


Fenced code block with long markers:


Fenced


Fenced code block with fenced code block markers of different length in it:


In code block

Still in code block

Still in code block


Fenced code block with Markdown header and horizontal rule:


#test
---


Fenced code block with link definitions, footnote definition and 
abbreviation definitions:


[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language


* In a list item with smalish indent:

  
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
  
  
With HTML content.
  

<b>bold</b>


Bug with block level elements in this case:

  <div>
  </div>


Indented code block of a fenced code block:

    
	haha!
	

With class:
  
html
<b>bold</b>

  
 html
<b>bold</b>

  
.html
<b>bold</b>

  
 .html
<b>bold</b>


With extra attribute block:

{.html}
<b>bold</b>

  
 {.html #codeid}
<b>bold</b>


 .html{.bold}
<div>

  
 .html {#codeid}
</div>
First line. <br/>
Second line.

This is a first paragraph,
on multiple lines.
     
This is a second paragraph.
There are spaces in between the two.This is a first paragraph,
on multiple lines.

This is a second paragraph
which has multiple lines too.A first paragraph.



A second paragraph after 3 CR (carriage return).This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
     
A few spaces and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
	
1 tab to separate them and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.

A new long long long long long long long long long long long long long long long long paragraph on 1 line.An ampersand & in the text flow is escaped as an html entity.There is an [ampersand](http://validator.w3.org/check?uri=http://www.w3.org/&verbose=1) in the URI.This is \*an asterisk which should stay as is.This is * an asterisk which should stay as is.\\   backslash
\   backtick
\*   asterisk
\_   underscore
\{\}  curly braces
\[\]  square brackets
\(\)  parentheses
\#   hash mark
\+   plus sign
\-   minus sign (hyphen)
\.   dot
\!   exclamation mark> # heading level 1
> 
> paragraph>A blockquote with a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.

>and a second very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.>This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a blockquote.> A blockquote
> on multiple lines
> like this.>A blockquote 
>on multiple lines 
>like this. >A blockquote
>on multiple lines
>like this.
>
>But it has
>two paragraphs.>A blockquote
>on multiple lines
>like this> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.
> This is the first level of quoting.
>
> > This is nested blockquote.> This is the first level of quoting.
> > This is nested blockquote.
> Back to the first level.
> This is the first level of quoting.
> > This is nested blockquote.
	10 PRINT HELLO INFINITE
	20 GOTO 10    10 PRINT < > &
    20 GOTO 10    10 PRINT HELLO INFINITE
    20 GOTO 10# Contributing to Mardown Test Suite

1. [Getting Involved](#getting-involved)
2. [Discussion](#discussion)
3. [How To Report an Issue](#how-to-report-an-issue)
4. [Editing Markdown Specification](#editing-markdown-specification)
5. [Test Suite Guidelines](#test-suite-guidelines)
6. [Pull Request Guidelines](#pull-request-guidelines)

## Getting Involved

There are a number of ways to get involved with the development of the Markdown Test Suite. If you are a first time contributor to an open source project, you can still add value to this project. You may identify grammar issues, write prose, examples or documentation for the project. You may flag some errors and open new issues.

Read all bits of this document and that will guide you on how to participate.

## Discussion

### Mailing List

The Markdown Test Suite has been started a little bit after the start of the [Markdown Community Group](http://www.w3.org/community/markdown/). You may want to discuss about Markdown and this project on the [group mailing-list](http://lists.w3.org/Archives/Public/public-markdown/).

## How to Report an Issue

Don't be afraid to add details to your issue. The more context you give, the better for people participating to the project. Make a short summary, add a description with the context and give links to places which will help to understand.

## Editing Markdown Specification

There is much needed work on the [Markdown Specification](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html). It doesn't require strong competences in coding. Be systematic in the markup and follow the way it is already organized. Each time you added a new atomic section, create a commit for this specific part.

## Test Suite Guidelines

When proposing new tests, make sure they do not already exist in the current test suite. You will notice that there is a separate section dedicated to the specific extensions that some markdown generators have created. Keep them separate. We want to keep the core clean and close to the original specification of Markdown.

If you are not sure, create an issue.

### Markdown Extensions

Markdown extension tests are accepted. Use the following rules:

- place all extension tests under the test/extensions/ENGINE directory with filename equal to the feature name
- for each ENGINE and add a README.markdown under the engine directory with a link to its specification

where ENGINE is either of:

- a command line utility. E.g. pandoc, kramdown.
- a programming API. E.g. Redcarpet::Markdown.new().
- a programmatically accessible web service. E.g.: GFM via the GitHub API.
- a non programmatically accessible web service. E.g.: Stack Overflow flavored markdown.

To avoid test duplication for common features, use the following rules:

- if file tests/extensions/ENGINE/FEATURE.md is empty or not present, use tests/extensions/FEATURE.md instead
- if file tests/extensions/ENGINE/FEATURE.out not present, use tests/extensions/FEATURE.out instead
- for a given ENGINE, only features which have either a .md or a .out are implemented by that engine.
- in case of different outputs for a single feature input, keep directly under extensions/ only the output case that happens across the most engines

**version**

Only the latest stable version of each ENGINE is considered.

**options**

The IO behavior tested is for engine defaults, without any options (command line options, extra JSON parameters, etc.) passed to the engine.

**external state**

Tests that use external state not present in the markdown input shall not be included in this test suite.

For example, what GFM @user user tags render to also depends on the state of GitHub's databases (only render to a link if user exists), not only on the input markdown.

#### Examples

GFM and the "fenced code block" use the following file structure:

    tests/extensions/gfm/README.markdown
    tests/extensions/gfm/fenced-code-block.md
    tests/extensions/gfm/fenced-code-block.out

where README.markdown contains:

    https://help.github.com/articles/github-flavored-markdown

To avoid duplication with other engines, if the input / output (normalized to DOM) is the same across multiple engines use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

If the input is the same, and outputs are DOM different, but represent the same idea (e.g. both represent computer code) use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/gfm/fenced-code-block.out
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

#### New Extensions

Tests are modular, and if you want to test a new engine for your project, that should be easy to do.

If you feel that the new engine is reasonably popular, please send a pull request adding it.

## Commits and Pull Requests

* Keep your commits clean and commented
* Do not mix in one commit different things. Keep modifications related.
* Do not mix everything in one giant pull request. Create separate pull requests for different topic. That will help to have a more meaningful debate about the pull requests and will help to review the code.
* If it relates to a specific issue, add the number of the issue in the commit message.

Thanks for Contributing
as*te*risks*single asterisks*_single underscores_HTML entities are written using ampersand notation: &copy;These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

This is an H1
=============# This is an H1 # # This is an H1# this is an h1 with two trailing spaces  
A new paragraph.# This is an H1This is an H2
-------------## This is an H2 #### This is an H2### This is an H3 ###### This is an H3#### This is an H4 ######## This is an H4##### This is an H5 ########## This is an H5###### This is an H6  ############ This is an H6- - ----***___-------![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 for everyone"![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 logo for everyone")![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png)We love <code> and & for everything We love code for everything We love code for everything The MIT License (MIT)

Copyright (c) 2013 Karl Dubost

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
A first sentence  
and a line break.A first sentence     
and a line break.This is an automatic link <http://www.w3.org/>[W3C](http://www.w3.org/ "Discover w3c")[W3C](http://www.w3.org/)[World Wide Web Consortium][w3c]

[w3c]: <http://www.w3.org/>[World Wide Web Consortium][]

[World Wide Web Consortium]: http://www.w3.org/[w3c][]

[w3c]: http://www.w3.org/[World Wide Web Consortium] [w3c]

[w3c]: http://www.w3.org/[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/
   "Discover W3C"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ (Discover w3c)[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ 'Discover w3c'[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ "Discover w3c"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/*   a list containing a blockquote

    > this the blockquote in the list* a

        b
*   a list containing a block of code

	    10 PRINT HELLO INFINITE
	    20 GOTO 10*   This is a list item with two paragraphs. Lorem ipsum dolor
	sit amet, consectetuer adipiscing elit. Aliquam hendrerit
	mi posuere lectus.

	Vestibulum enim wisi, viverra nec, fringilla in, laoreet
	vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
	sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.*   This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.1\. ordered list escape1. 1

    - inner par list

2. 2
1. list item 1
8. list item 2
1. list item 31. list item 1
2. list item 2
3. list item 3This is a paragraph
on multiple lines
with hard return.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line. This is a paragraph with a trailing and leading space. This is a paragraph with 1 trailing tab.	  This is a paragraph with 2 leading spaces.   This is a paragraph with 3 leading spaces. This is a paragraph with 1 leading space.This is a paragraph with a trailing space. # Colophon - October 1st, 2014

This project was initiated to provide a test suite for Markdown markup, and eventually create a specification from this test results. A part of of the community has started a new endeavor which seems to get traction as [CommonMark](https://github.com/jgm/stmd). **We are then closing this project** and encourage you to contribute to CommonMark. 

The most interesting part of this project would not have been possible without the dedication of [Ciro Santilli](https://github.com/cirosantilli) @cirosantilli. So big applause and thank you to him.


The rest is kept around for archives and references.

# Markdown Test Suite

Inspired by questions on [W3C Markdown Community Group](http://www.w3.org/community/markdown).

Pull Requests are welcome. See the [CONTRIBUTING Guidelines](https://github.com/karlcow/markdown-testsuite/blob/master/CONTRIBUTING.md)

## Design goals

- Comprehensive.
- Small modularized tests.
- Easy to run tests using any programming language. In particular, data representations must have an implementation on all major languages.
- Develop a consensus based markdown specification at [markdown-spec.html](markdown-spec.html). Visualize it [here](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html).

## Test Scripts

Markdown Test Suite already includes tests for many important markdown engines.

To see what the scripts do run:

    ./cat-all.py -h
    ./run-tests.py -h

To configure the scripts do:

	cp config_local.py.example config_local.py

and edit config_local.py. It is already gitignored.

A Vagrantfile is provided with a provision script that installs all installable engines.

Sample output from run-tests.py:

    blackfriday   |......FFF..............FF...F....................................F....................................|   0.93s  102    7   6%
	gfm           |FF.....F.....F...FFFF..F....F........................FFFF...FF...............FF...F.......F...........| 262.88s  102   20  19%
    hoedown       |..............................F.................................................F.....................|   0.36s  102    2   1%
	kramdown      |......FFF.....FF.......FF.......FF.FFFFFFFFFFFFF.......................F..............................|  30.69s  102   23  22%
    lunamark      |FFFFFF.F.FFFFFFFFFFFF.F.....FFFF..FF............FFFFF..FFFFFFFFFF..............F...FFFFFFFFFFF........|   1.58s  103   53  51%
    markdown_pl   |.....................FFFF...............................F...............F.............................|   2.56s  102    6   5%
    markdown2     |......................................................................................................|   5.39s  103    0   0%
    marked        |..............F.................FFFFFFFFFFFFFFFF......................F.F.............................|   6.22s  102   19  18%
    maruku        |......FFF......F.......F.FFF...............................................FF.........................|  37.02s  102   10   9%
    md2html       |.........................FFF...F............................................FF........................|   7.42s  102    6   5%
    multimarkdown |......FFF....FF...F............FFF.FFFFFFFFFFFFF.....FFFF.........F...................................|   0.58s  102   27  26%
    pandoc        |FF...........F.F.FFFF..FFFFF....FF.FFFFFFFFFFFFF.....FFFF.....FF............FFF.FFF..................F|   1.11s  102   41  40%
    peg_markdown  |.................................................................F....................................|   0.46s  102    1   0%
    rdiscount     |.......F.........................................................F....................................|  25.19s  102    3   2%
    redcarpet     |......................................................................................................|  21.49s  102    0   0%
    showdown      |.......................................................................F..............................|   6.85s  102    1   0%

	Extensions:

    blackfriday   |F..|  0.04s    3    1  33%
	gfm           |F.|   2.37s    2    1  50%
    hoedown       |.|    0.00s    1    0   0%
    lunamark      |F.F|  0.05s    3    2  66%
    kramdown      |..|   0.62s    2    0   0%
    markdown_pl   ||     0.00s    0    0   0%
    markdown2     |F.|   0.14s    2    1  50%
    marked        |F.|   0.13s    2    1  50%
    maruku        |F..|  1.06s    3    1  33%
    md2html       |F.|   0.14s    2    0   0%
    multimarkdown |F.|   0.01s    2    1  50%
    pandoc        |F.|   0.02s    2    1  50%
    peg_markdown  |...|  0.02s    3    0   0%
    rdiscount     |F..|   0.74s    3    1  33%
    redcarpet     |..|   0.42s    2    0   0%
    showdown      |F..|  0.20s    3    1  33%

Where F indicates a failing test.

## Other Noticeable Test Suites

We haven't been the first test suite effort. Some projects have maintained their own test suite for a long time. Hopefully we can reach a state where people agree on the terms of what should be a good test suite for all developers.

- [Original test suite](http://daringfireball.net/projects/downloads/MarkdownTest_1.0.zip)
- [PHP markdown test suite:](https://github.com/michelf/mdtest/tree/master/Markdown.mdtest)
- [Markdown-js test suite](https://github.com/evilstreak/markdown-js/tree/master/test/features)
- [Python markdown 2 test suite](https://github.com/trentm/python-markdown2/tree/master/test/tm-cases)
- [multimarkdown test suite](https://github.com/fletcher/MMD-Test-Suite)
- [John MacFarlane's Standard Markdown spec](https://github.com/jgm/stmd)

In addition we should note the [wonderful work](http://johnmacfarlane.net/babelmark2/) made by John Mac Farlane. The Web service output the differences in between the different markdown implementations. It helps a lot when searching on the most common output.
as**te**risks**double asterisks**__double underscores__* list item 1
* list item 2
* list item 3
- list item 1
- list item 2
- list item 3 * list item 1
 * list item 2
 * list item 3  * list item 1
  * list item 2
  * list item 3   * list item 1
   * list item 2
   * list item 3+ list item 1
+ list item 2
+ list item 3* list item in paragraph

* another list item in paragraph*   This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a list.
*   and yet another long long long long long long long long long long long long long long long long long long long long long long line.*   This is a list item
    with the content on
    multiline and indented.
*   And this another list item
    with the same principle.€Some text about HTML, SGML and HTML4.

Let's talk about the U.S.A., (É.U. or É.-U. d'A. in French).

*[HTML4]: Hyper Text Markup Language version 4
*[HTML]: Hyper Text Markup Language
*[SGML]: Standard Generalized Markup Language
*[U.S.A.]: United States of America
*[É.U.] : États-Unis d'Amérique
*[É.-U. d'A.] : États-Unis d'Amérique

And here we have a CD, some CDs, and some other CD's.

*[CD]: Compact Disk

Let's transfert documents through TCP/IP, using TCP packets.

*[IP]: Internet Protocol
*[TCP]: Transmission Control Protocol

 ---

Bienvenue sur [CMS](http://www.bidulecms.com "Bidule CMS").

*[CMS]: Content Management System

 ---

ATCCE

*[ATCCE]: Abbreviation "Testing" Correct 'Character' < Escapes >* one
* two

1. three
2. four

* one
* two
1. three
2. fourAT&T has an ampersand in their name.

AT&amp;T is another way to write it.

This & that.

4 < 5.

6 > 5.

Here's a [link] [1] with an ampersand in the URL.

Here's a link with an amersand in the link text: [AT&T] [2].

Here's an inline [link](/script?foo=1&bar=2).

Here's an inline [link](</script?foo=1&bar=2>).


[1]: http://example.com/?foo=1&bar=2
[2]: http://att.com/  "AT&T"Link: <http://example.com/>.

With an ampersand: <http://example.com/?foo=1&bar=2>

* In a list?
* <http://example.com/>
* It should.

> Blockquoted: <http://example.com/>

Auto-links should not occur here: <http://example.com/>

	or here: <http://example.com/>These should all get escaped:

Backslash: \\

Backtick: \

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-



These should not, because they occur within a code block:

	Backslash: \\

	Backtick: \

	Asterisk: \*

	Underscore: \_

	Left brace: \{

	Right brace: \}

	Left bracket: \[

	Right bracket: \]

	Left paren: \(

	Right paren: \)

	Greater-than: \>

	Hash: \#

	Period: \.

	Bang: \!

	Plus: \+

	Minus: \-


Nor should these, which occur in code spans:

Backslash: \\

Backtick:   \  

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-


These should get escaped, even though they're matching pairs for
other Markdown constructs:

\*asterisks\*

\_underscores\_

\backticks\

This is a code span with a literal backslash-backtick sequence:   \  

This is a tag with unescaped backticks <span attr='ticks'>bar</span>.

This is a tag with backslashes <span attr='\\backslashes\\'>bar</span>.
  .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>
 

As above: checking for bad interractions with the HTML block parser:

  html
<div>
 

Some *mar kdown* formatting.

  html
</div>
 

Some *markdown*

 
<div>
    <html>
 

 
function test();
 

<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">
 
<html>
    <title>
 
</div>

Two code blocks with no blank line between them:

 
<div>
 
 
<div>
 

Testing *confusion* with code spans at the HTML block parser:

 
<div></div>
 

Testing mixing with title code blocks

 
<p>

<p>
 

<p>
 
<p>

 
<Fenced>
 

Code block starting and ending with empty lines:
 


<Fenced>


 

Indented code block containing fenced code block sample:

	 
	<Fenced>
	 

Fenced code block with indented code block sample:

 
Some text

	Indented code block sample code
 

Fenced code block with long markers:

 
Fenced
 

Fenced code block with fenced code block markers of different length in it:

 
In code block
 
Still in code block
 
Still in code block
 

Fenced code block with Markdown header and horizontal rule:

 
#test
---
 

Fenced code block with link definitions, footnote definition and
abbreviation definitions:

 
[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language
 

* In a list item with smalish indent:

   
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
   

With HTML content.

 
<b>bold</b>
 

Bug with block level elements in this case:
 
  <div>
  </div>
 

Indented code block of a fenced code block:

     
	haha!
	 

With class:

 html
<b>bold</b>
 

  html
<b>bold</b>
 

 .html
<b>bold</b>
 

  .html
<b>bold</b>
 

With extra attribute block:

 {.html}
<b>bold</b>
 

  {.html #codeid}
<b>bold</b>
 

  .html{.bold}
<div>
 
  
  .html {#codeid}
</div>
 > Example:
> 
>     sub status {
>         print "working";
>     }
> 
> Or:
> 
>     sub status {
>         return "working";
>     }

*	List Item:

		code block

		with a blank line

	within a list item.

*       code block
        as first element of a list item

*	List Item:
	
		code block with whitespace on preceding line
    Codeblock on second line
    <?php
    echo "hello!";
    ?>

foo bar

    <?php
    echo "hello!";

lorem ipsum

    echo "hello!";
    ?>
    
lorem ipsum	code block on the first line
	
Regular text.

    code block indented by spaces

Regular text.

	the lines in this block  
	all contain trailing spaces  

Regular Text.

	code block on the last line<test a=" content of attribute ">

Fix for backticks within HTML tag: <span attr='ticks'>like this</span>

Here's how you put   backticks   in a code span.A simple definition list:

Term 1
:   Definition 1

Term 2
:   Definition 2

With multiple terms:

Term 1
Term 2
:   Definition 1

Term 3
Term 4
:   Definition 2

With multiple definitions:

Term 1
:   Definition 1
:   Definition 2

Term 2
:   Definition 3
:   Definition 4

With multiple lines per definition:

Term 1
:   Definition 1 line 1 ...
Definition 1 line 2
:   Definition 2 line 1 ...
Definition 2 line 2

Term 2
:   Definition 3 line 2 ...
    Definition 3 line 2
:   Definition 4 line 2 ...
    Definition 4 line 2

With paragraphs:

Term 1

:   Definition 1 (paragraph)

Term 2

:   Definition 2 (paragraph)

With multiple paragraphs:

Term 1

:   Definition 1 paragraph 1 line 1 ...
	Definition 1 paragraph 1 line 2

    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)

    Definition 1 paragraph 2 line 1 ...
Definition 1 paragraph 2 line 2 (lazy)

* * *

A mix:

Term 1
Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)
    
    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

:   Definition 2 paragraph 1 line 1 ...
Definition 2 paragraph 1 line 2 (lazy)

Term 3
:   Definition 3 (no paragraph)
:   Definition 4 (no paragraph)
:   Definition 5 line 1 ...
    Definition 5 line 2 (no paragraph)

:   Definition 6 paragraph 1 line 1 ...
Definition 6 paragraph 1 line 2
:   Definition 7 (no paragraph)
:   Definition 8 paragraph 1 line 1 (forced paragraph) ...
    Definition 8 paragraph 1 line 2
    
    Definition 8 paragraph 2 line 1
    
Term 4
:   Definition 9 paragraph 1 line 1 (forced paragraph) ...
    Definition 9 paragraph 1 line 2
    
    Definition 9 paragraph 2 line 1
:   Definition 10 (no paragraph)

* * *

Special cases:

Term

:       code block
        as first element of a definition<michel.fortin@michelf.ca>

International domain names: <help@tūdaliņ.lv>


## Some weird valid email addresses

<abc.123@example.com>

<1234567890@example.com>

<_______@example.com>

<abc+mailbox/department=shipping@example.com>

<!#$%&'*+-/=?^_.{|}@example.com> (all of these characters are allowed)

<"abc@def"@example.com> (anything goes inside quotation marks)

<"Fred Bloggs"@example.com>

<jsmith@[192.0.2.1]>

<"A"@example.com>Combined emphasis:

1.  ***test test***
2.  ___test test___
3.  *test **test***
4.  **test *test***
5.  ***test* test**
6.  ***test** test*
7.  ***test* test**
8.  **test *test***
9.  *test **test***
10. _test __test___
11. __test _test___
12. ___test_ test__
13. ___test__ test_
14. ___test_ test__
15. __test _test___
16. _test __test___
17. *test __test__*
18. **test _test_**
19. **_test_ test**
20. *__test__ test*
21. **_test_ test**
22. **test _test_**
23. *test __test__*
24. _test **test**_
25. __test *test*__
26. __*test* test__
27. _**test** test_
28. __*test* test__
29. __test *test*__
30. _test **test**_


Incorrect nesting:

1.  *test  **test*  test**
2.  _test  __test_  test__
3.  **test  *test** test*
4.  __test  _test__ test_
5.  *test   *test*  test*
6.  _test   _test_  test_
7.  **test **test** test**
8.  __test __test__ test__
9. _**some text_**
10. *__some text*__
11. **_some text**_
12. *__some text*__

No emphasis:

1.  test*  test  *test
2.  test** test **test
3.  test_  test  _test
4.  test__ test __test



Middle-word emphasis (asterisks):

1.  *a*b
2.   a*b*
3.   a*b*c
4. **a**b
5.   a**b**
6.   a**b**c


Middle-word emphasis (underscore):

1.  _a_b
2.   a_b_
3.   a_b_c
4. __a__b
5.   a__b__
6.   a__b__c

my_precious_file.txt


## Tricky Cases

E**. **Test** TestTestTest

E**. **Test** Test Test Test


## Overlong emphasis

Name: ____________  
Organization: ____  
Region/Country: __

_____Cut here_____

____Cut here____

# Regression

_**Note**_: This _is emphasis_.
With asterisks

 * List item
 *
 * List item

With numbers

1. List item
2.
3. List item

With hyphens

- List item
-
- List item

With asterisks

 * List item
 * List item
 *

With numbers

1. List item
2. List item
3.

With hyphens

- List item
- List item
-
This is the first paragraph.[^first]

[^first]:  This is the first note.

* List item one.[^second]
* List item two.[^third]

[^third]: This is the third note, defined out of order.
[^second]: This is the second note.
[^fourth]: This is the fourth note.

# Header[^fourth]

Some paragraph with a footnote[^1], and another[^2].

[^1]: Content for fifth footnote.
[^2]: Content for sixth footnote spaning on 
    three lines, with some span-level markup like
    _emphasis_, a [link][].

[link]: http://michelf.ca/

Another paragraph with a named footnote[^fn-name].

[^fn-name]:
    Footnote beginning on the line next to the marker.

This paragraph should not have a footnote marker since 
the footnote is undefined.[^3]

This paragraph has a second footnote marker to footnote number one.[^1]

This paragraph links to a footnote with plenty of 
block-level content.[^block]

[^block]:
	Paragraph.
	
	*   List item
	
	> Blockquote
	
	    Code block

This paragraph host the footnote reference within a 
footnote test[^reference].

[^reference]:
	This footnote has a footnote of its own.[^nested]

[^nested]:
	This footnote should appear even though it is referenced
	from another footnote. But [^reference] should be litteral
	since the footnote with that name has already been used.

 - - -

Testing unusual footnote name[^1$^!"'].

[^1$^!"']: Haha!

 - - -
 
Footnotes mixed with images[^image-mixed]
![1800 Travel][img6]
![1830 Travel][img7]

[img6]: images/MGR-1800-travel.jpeg "Travel Speeds in 1800"
[^image-mixed]: Footnote Content
[img7]: images/MGR-1830-travel.jpeg "Travel Speeds in 1830"
In Markdown 1.0.0 and earlier. Version
8. This line turns into a list item.
Because a hard-wrapped line in the
middle of a paragraph looked like a
list item.

Here's one with a bullet.
* criminey.
Header  {#id1}
======

Header  { #id2}
------

### Header  {#id3 }
#### Header ##  { #id4 }

 - - -

Header  {.cl}
======

Header  { .cl}
------

### Header  {.cl }
#### Header ##  { .cl }

 - - -

Header  {.cl.class}
======

Header  { .cl .class}
------

### Header  {.cl .class }
#### Header ##  { .cl.class }

 - - -

Header  {#id5.cl.class}
======

Header  { #id6 .cl .class}
------

### Header  {.cl.class#id7 }
#### Header ##  { .cl.class#id8 }
Header
======

Header
------

### Header

 - - -

Header
======
Paragraph

Header
------
Paragraph

### Header
Paragraph

 - - -

Paragraph
Header
======
Paragraph

Paragraph
Header
------
Paragraph

Paragraph
### Header
ParagraphDashes:

---

 ---
 
  ---

   ---

	---

- - -

 - - -
 
  - - -

   - - -

	- - -


Asterisks:

***

 ***
 
  ***

   ***

	***

* * *

 * * *
 
  * * *

   * * *

	* * *


Underscores:

___

 ___
 
  ___

   ___

    ___

_ _ _

 _ _ _
 
  _ _ _

   _ _ _

    _ _ _
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")

Inline within a paragraph: [alt text](/url/).

![alt text](/url/  "title preceded by two spaces")

![alt text](/url/  "title has spaces afterward"  )

![alt text](</url/>)

![alt text](</url/> "with a title").

![Empty]()

![this is a stupid URL](http://example.com/(parens).jpg)


![alt text][foo]

  [foo]: /url/

![alt text][bar]

  [bar]: /url/ "Title here"Simple block on one line:

<div>foo</div>

And nested without indentation:

<div>
<div>
<div>
foo
</div>
<div style=">"/>
</div>
<div>bar</div>
</div>

And with attributes:

<div>
	<div id="foo">
	</div>
</div>

This was broken in 1.0.2b7:

<div class="inlinepage">
<div class="toggleableend">
foo
</div>
</div>
Here's a simple block:

<div>
	foo
</div>

This should be a code block, though:

	<div>
		foo
	</div>

As should this:

	<div>foo</div>

Now, nested:

<div>
	<div>
		<div>
			foo
		</div>
	</div>
</div>

This should just be an HTML comment:

<!-- Comment -->

Multiline:

<!--
Blah
Blah
-->

Code block:

	<!-- Comment -->

Just plain comment, with trailing spaces on the line:

<!-- foo -->   

Code:

	<hr />
	
Hr's:

<hr>

<hr/>

<hr />

<hr>   

<hr/>  

<hr /> 

<hr class="foo" id="bar" />

<hr class="foo" id="bar"/>

<hr class="foo" id="bar" >

<abbr title=" **Attribute Content Is Not A Code Span** ">ACINACS</abbr>

<abbr title="first backtick!">SB</abbr> 
<abbr title="second backtick!">SB</abbr>Paragraph one.

<!-- This is a simple comment -->

<!--
	This is another comment.
-->

Paragraph two.

<!-- one comment block -- -- with two comments -->

The end.
# Markdown inside code blocks

<div markdown="1">
foo
</div>

<div markdown='1'>
foo
</div>

<div markdown=1>
foo
</div>

<table>
<tr><td markdown="1">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="span">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="block">test _emphasis_ (block)</td></tr>
</table>

## More complicated

<table>
<tr><td markdown="1">
* this is _not_ a list item</td></tr>
<tr><td markdown="span">
* this is _not_ a list item</td></tr>
<tr><td markdown="block">
* this _is_ a list item
</td></tr>
</table>

## With indent

<div>
    <div markdown="1">
    This text is no code block: if it was, the 
    closing <div> would be too and the HTML block 
    would be invalid.

    Markdown content in HTML blocks is assumed to be 
    indented the same as the block opening tag.

    **This should be the third paragraph after the header.**
    </div>
</div>

## Code block with rogue </div>s in Markdown code span and block

<div>
    <div markdown="1">

    This is a code block however:

        </div>

    Funny isn't it? Here is a code span: </div>.

    </div>
</div>

<div>
  <div markdown="1">
    * List item, not a code block

Some text

      This is a code block.
  </div>
</div>

## No code block in markdown span mode

<p markdown="1">
    This is not a code block since Markdown parse paragraph 
    content as span. Code spans like </p> are allowed though.
</p>

<p markdown="1">_Hello_ _world_</p>

## Preserving attributes and tags on more than one line:

<p class="test" markdown="1" 
id="12">
Some _span_ content.
</p>


## Header confusion bug

<table class="canvas">
<tr>
<td id="main" markdown="1">Hello World!
============

Hello World!</td>
</tr>
</table>
Here is a block tag ins:

<ins>
<p>Some text</p>
</ins>

<ins>And here it is inside a paragraph.</ins>

And here it is <ins>in the middle of</ins> a paragraph.

<del>
<p>Some text</p>
</del>

<del>And here is ins as a paragraph.</del>

And here it is <del>in the middle of</del> a paragraph.
		    GNU GENERAL PUBLIC LICENSE
		       Version 2, June 1991

 Copyright (C) 1989, 1991 Free Software Foundation, Inc.,
 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

			    Preamble

  The licenses for most software are designed to take away your
freedom to share and change it.  By contrast, the GNU General Public
License is intended to guarantee your freedom to share and change free
software--to make sure the software is free for all its users.  This
General Public License applies to most of the Free Software
Foundation's software and to any other program whose authors commit to
using it.  (Some other Free Software Foundation software is covered by
the GNU Lesser General Public License instead.)  You can apply it to
your programs, too.

  When we speak of free software, we are referring to freedom, not
price.  Our General Public Licenses are designed to make sure that you
have the freedom to distribute copies of free software (and charge for
this service if you wish), that you receive source code or can get it
if you want it, that you can change the software or use pieces of it
in new free programs; and that you know you can do these things.

  To protect your rights, we need to make restrictions that forbid
anyone to deny you these rights or to ask you to surrender the rights.
These restrictions translate to certain responsibilities for you if you
distribute copies of the software, or if you modify it.

  For example, if you distribute copies of such a program, whether
gratis or for a fee, you must give the recipients all the rights that
you have.  You must make sure that they, too, receive or can get the
source code.  And you must show them these terms so they know their
rights.

  We protect your rights with two steps: (1) copyright the software, and
(2) offer you this license which gives you legal permission to copy,
distribute and/or modify the software.

  Also, for each author's protection and ours, we want to make certain
that everyone understands that there is no warranty for this free
software.  If the software is modified by someone else and passed on, we
want its recipients to know that what they have is not the original, so
that any problems introduced by others will not reflect on the original
authors' reputations.

  Finally, any free program is threatened constantly by software
patents.  We wish to avoid the danger that redistributors of a free
program will individually obtain patent licenses, in effect making the
program proprietary.  To prevent this, we have made it clear that any
patent must be licensed for everyone's free use or not licensed at all.

  The precise terms and conditions for copying, distribution and
modification follow.

		    GNU GENERAL PUBLIC LICENSE
   TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

  0. This License applies to any program or other work which contains
a notice placed by the copyright holder saying it may be distributed
under the terms of this General Public License.  The "Program", below,
refers to any such program or work, and a "work based on the Program"
means either the Program or any derivative work under copyright law:
that is to say, a work containing the Program or a portion of it,
either verbatim or with modifications and/or translated into another
language.  (Hereinafter, translation is included without limitation in
the term "modification".)  Each licensee is addressed as "you".

Activities other than copying, distribution and modification are not
covered by this License; they are outside its scope.  The act of
running the Program is not restricted, and the output from the Program
is covered only if its contents constitute a work based on the
Program (independent of having been made by running the Program).
Whether that is true depends on what the Program does.

  1. You may copy and distribute verbatim copies of the Program's
source code as you receive it, in any medium, provided that you
conspicuously and appropriately publish on each copy an appropriate
copyright notice and disclaimer of warranty; keep intact all the
notices that refer to this License and to the absence of any warranty;
and give any other recipients of the Program a copy of this License
along with the Program.

You may charge a fee for the physical act of transferring a copy, and
you may at your option offer warranty protection in exchange for a fee.

  2. You may modify your copy or copies of the Program or any portion
of it, thus forming a work based on the Program, and copy and
distribute such modifications or work under the terms of Section 1
above, provided that you also meet all of these conditions:

    a) You must cause the modified files to carry prominent notices
    stating that you changed the files and the date of any change.

    b) You must cause any work that you distribute or publish, that in
    whole or in part contains or is derived from the Program or any
    part thereof, to be licensed as a whole at no charge to all third
    parties under the terms of this License.

    c) If the modified program normally reads commands interactively
    when run, you must cause it, when started running for such
    interactive use in the most ordinary way, to print or display an
    announcement including an appropriate copyright notice and a
    notice that there is no warranty (or else, saying that you provide
    a warranty) and that users may redistribute the program under
    these conditions, and telling the user how to view a copy of this
    License.  (Exception: if the Program itself is interactive but
    does not normally print such an announcement, your work based on
    the Program is not required to print an announcement.)

These requirements apply to the modified work as a whole.  If
identifiable sections of that work are not derived from the Program,
and can be reasonably considered independent and separate works in
themselves, then this License, and its terms, do not apply to those
sections when you distribute them as separate works.  But when you
distribute the same sections as part of a whole which is a work based
on the Program, the distribution of the whole must be on the terms of
this License, whose permissions for other licensees extend to the
entire whole, and thus to each and every part regardless of who wrote it.

Thus, it is not the intent of this section to claim rights or contest
your rights to work written entirely by you; rather, the intent is to
exercise the right to control the distribution of derivative or
collective works based on the Program.

In addition, mere aggregation of another work not based on the Program
with the Program (or with a work based on the Program) on a volume of
a storage or distribution medium does not bring the other work under
the scope of this License.

  3. You may copy and distribute the Program (or a work based on it,
under Section 2) in object code or executable form under the terms of
Sections 1 and 2 above provided that you also do one of the following:

    a) Accompany it with the complete corresponding machine-readable
    source code, which must be distributed under the terms of Sections
    1 and 2 above on a medium customarily used for software interchange; or,

    b) Accompany it with a written offer, valid for at least three
    years, to give any third party, for a charge no more than your
    cost of physically performing source distribution, a complete
    machine-readable copy of the corresponding source code, to be
    distributed under the terms of Sections 1 and 2 above on a medium
    customarily used for software interchange; or,

    c) Accompany it with the information you received as to the offer
    to distribute corresponding source code.  (This alternative is
    allowed only for noncommercial distribution and only if you
    received the program in object code or executable form with such
    an offer, in accord with Subsection b above.)

The source code for a work means the preferred form of the work for
making modifications to it.  For an executable work, complete source
code means all the source code for all modules it contains, plus any
associated interface definition files, plus the scripts used to
control compilation and installation of the executable.  However, as a
special exception, the source code distributed need not include
anything that is normally distributed (in either source or binary
form) with the major components (compiler, kernel, and so on) of the
operating system on which the executable runs, unless that component
itself accompanies the executable.

If distribution of executable or object code is made by offering
access to copy from a designated place, then offering equivalent
access to copy the source code from the same place counts as
distribution of the source code, even though third parties are not
compelled to copy the source along with the object code.

  4. You may not copy, modify, sublicense, or distribute the Program
except as expressly provided under this License.  Any attempt
otherwise to copy, modify, sublicense or distribute the Program is
void, and will automatically terminate your rights under this License.
However, parties who have received copies, or rights, from you under
this License will not have their licenses terminated so long as such
parties remain in full compliance.

  5. You are not required to accept this License, since you have not
signed it.  However, nothing else grants you permission to modify or
distribute the Program or its derivative works.  These actions are
prohibited by law if you do not accept this License.  Therefore, by
modifying or distributing the Program (or any work based on the
Program), you indicate your acceptance of this License to do so, and
all its terms and conditions for copying, distributing or modifying
the Program or works based on it.

  6. Each time you redistribute the Program (or any work based on the
Program), the recipient automatically receives a license from the
original licensor to copy, distribute or modify the Program subject to
these terms and conditions.  You may not impose any further
restrictions on the recipients' exercise of the rights granted herein.
You are not responsible for enforcing compliance by third parties to
this License.

  7. If, as a consequence of a court judgment or allegation of patent
infringement or for any other reason (not limited to patent issues),
conditions are imposed on you (whether by court order, agreement or
otherwise) that contradict the conditions of this License, they do not
excuse you from the conditions of this License.  If you cannot
distribute so as to satisfy simultaneously your obligations under this
License and any other pertinent obligations, then as a consequence you
may not distribute the Program at all.  For example, if a patent
license would not permit royalty-free redistribution of the Program by
all those who receive copies directly or indirectly through you, then
the only way you could satisfy both it and this License would be to
refrain entirely from distribution of the Program.

If any portion of this section is held invalid or unenforceable under
any particular circumstance, the balance of the section is intended to
apply and the section as a whole is intended to apply in other
circumstances.

It is not the purpose of this section to induce you to infringe any
patents or other property right claims or to contest validity of any
such claims; this section has the sole purpose of protecting the
integrity of the free software distribution system, which is
implemented by public license practices.  Many people have made
generous contributions to the wide range of software distributed
through that system in reliance on consistent application of that
system; it is up to the author/donor to decide if he or she is willing
to distribute software through any other system and a licensee cannot
impose that choice.

This section is intended to make thoroughly clear what is believed to
be a consequence of the rest of this License.

  8. If the distribution and/or use of the Program is restricted in
certain countries either by patents or by copyrighted interfaces, the
original copyright holder who places the Program under this License
may add an explicit geographical distribution limitation excluding
those countries, so that distribution is permitted only in or among
countries not thus excluded.  In such case, this License incorporates
the limitation as if written in the body of this License.

  9. The Free Software Foundation may publish revised and/or new versions
of the General Public License from time to time.  Such new versions will
be similar in spirit to the present version, but may differ in detail to
address new problems or concerns.

Each version is given a distinguishing version number.  If the Program
specifies a version number of this License which applies to it and "any
later version", you have the option of following the terms and conditions
either of that version or of any later version published by the Free
Software Foundation.  If the Program does not specify a version number of
this License, you may choose any version ever published by the Free Software
Foundation.

  10. If you wish to incorporate parts of the Program into other free
programs whose distribution conditions are different, write to the author
to ask for permission.  For software which is copyrighted by the Free
Software Foundation, write to the Free Software Foundation; we sometimes
make exceptions for this.  Our decision will be guided by the two goals
of preserving the free status of all derivatives of our free software and
of promoting the sharing and reuse of software generally.

			    NO WARRANTY

  11. BECAUSE THE PROGRAM IS LICENSED FREE OF CHARGE, THERE IS NO WARRANTY
FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW.  EXCEPT WHEN
OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES
PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED
OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.  THE ENTIRE RISK AS
TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU.  SHOULD THE
PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING,
REPAIR OR CORRECTION.

  12. IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING
WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MAY MODIFY AND/OR
REDISTRIBUTE THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES,
INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING
OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED
TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY
YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER
PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES.

		     END OF TERMS AND CONDITIONS

	    How to Apply These Terms to Your New Programs

  If you develop a new program, and you want it to be of the greatest
possible use to the public, the best way to achieve this is to make it
free software which everyone can redistribute and change under these terms.

  To do so, attach the following notices to the program.  It is safest
to attach them to the start of each source file to most effectively
convey the exclusion of warranty; and each file should have at least
the "copyright" line and a pointer to where the full notice is found.

    <one line to give the program's name and a brief idea of what it does.>
    Copyright (C) <year>  <name of author>

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

Also add information on how to contact you by electronic and paper mail.

If the program is interactive, make it output a short notice like this
when it starts in an interactive mode:

    Gnomovision version 69, Copyright (C) year name of author
    Gnomovision comes with ABSOLUTELY NO WARRANTY; for details type show w'.
    This is free software, and you are welcome to redistribute it
    under certain conditions; type show c' for details.

The hypothetical commands show w' and show c' should show the appropriate
parts of the General Public License.  Of course, the commands you use may
be called something other than show w' and show c'; they could even be
mouse-clicks or menu items--whatever suits your program.

You should also get your employer (if you work as a programmer) or your
school, if any, to sign a "copyright disclaimer" for the program, if
necessary.  Here is a sample; alter the names:

  Yoyodyne, Inc., hereby disclaims all copyright interest in the program
  Gnomovision' (which makes passes at compilers) written by James Hacker.

  <signature of Ty Coon>, 1 April 1989
  Ty Coon, President of Vice

This General Public License does not permit incorporating your program into
proprietary programs.  If your program is a subroutine library, you may
consider it more useful to permit linking proprietary applications with the
library.  If this is what you want to do, use the GNU Lesser General
Public License instead of this License.
This is an [inline link](/url "title"){.class #inline-link}.

This is a [reference link][refid].

This is an ![inline image](/img "title"){.class #inline-img}.

This is a ![reference image][refid].

[refid]: /path/to/something (Title) { .class #ref data-key=val }

Just a [URL](/url/).

[URL and title](/url/ "title").

[URL and title](/url/  "title preceded by two spaces").

[URL and title](/url/	"title preceded by a tab").

[URL and title](/url/ "title has spaces afterward"  ).

[URL wrapped in angle brackets](</url/>).

[URL w/ angle brackets + title](</url/> "Here's the title").

[Empty]().

[With parens in the URL](http://en.wikipedia.org/wiki/WIMP_(computing))

(With outer parens and [parens in url](/foo(bar)))


[With parens in the URL](/foo(bar) "and a title")

(With outer parens and [parens in url](/foo(bar) "and a title"))
Foo [bar] [1].

Foo [bar][1].

Foo [bar]
[1].

[1]: /url/  "Title"


With [embedded [brackets]] [b].


Indented [once][].

Indented [twice][].

Indented [thrice][].

Indented [four][] times.

 [once]: /url

  [twice]: /url

   [thrice]: /url

    [four]: /url


[b]: /url/

* * *

[this] [this] should work

So should [this][this].

And [this] [].

And [this][].

And [this].

But not [that] [].

Nor [that][].

Nor [that].

[Something in brackets like [this][] should work]

[Same with [this].]

In this case, [this](/somethingelse/) points to something else.

Backslashing should suppress \[this] and [this\].

[this]: foo


* * *

Here's one where the [link
breaks] across lines.

Here's another where the [link 
breaks] across lines, but with a line-ending space.


[link breaks]: /url/
This is the [simple case].

[simple case]: /simple



This one has a [line
break].

This one has a [line 
break] with a line-ending space.

[line break]: /foo


[this] [that] and the [other]

[this]: /this
[that]: /that
[other]: /other
Foo [bar][].

Foo [bar](/url/ "Title with "quotes" inside").


  [bar]: /url/ "Title with "quotes" inside"

Markdown: Basics
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a class="selected" title="Markdown Basics">Basics</a></li>
    <li><a href="/projects/markdown/syntax" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


Getting the Gist of Markdown's Formatting Syntax
------------------------------------------------

This page offers a brief overview of what it's like to use Markdown.
The [syntax page] [s] provides complete, detailed documentation for
every feature, but Markdown should be very easy to pick up simply by
looking at a few examples of it in action. The examples on this page
are written in a before/after style, showing example syntax and the
HTML output produced by Markdown.

It's also helpful to simply try Markdown out; the [Dingus] [d] is a
web application that allows you type your own Markdown-formatted text
and translate it to XHTML.

**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL] [src].

  [s]: /projects/markdown/syntax  "Markdown Syntax"
  [d]: /projects/markdown/dingus  "Markdown Dingus"
  [src]: /projects/markdown/basics.text


## Paragraphs, Headers, Blockquotes ##

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

Markdown offers two styles of headers: *Setext* and *atx*.
Setext-style headers for <h1> and <h2> are created by
"underlining" with equal signs (=) and hyphens (-), respectively.
To create an atx-style header, you put 1-6 hash marks (#) at the
beginning of the line -- the number of hashes equals the resulting
HTML header level.

Blockquotes are indicated using email-style '>' angle brackets.

Markdown:

    A First Level Header
    ====================
    
    A Second Level Header
    ---------------------

    Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.

    The quick brown fox jumped over the lazy
    dog's back.
    
    ### Header 3

    > This is a blockquote.
    > 
    > This is the second paragraph in the blockquote.
    >
    > ## This is an H2 in a blockquote


Output:

    <h1>A First Level Header</h1>
    
    <h2>A Second Level Header</h2>
    
    <p>Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.</p>
    
    <p>The quick brown fox jumped over the lazy
    dog's back.</p>
    
    <h3>Header 3</h3>
    
    <blockquote>
        <p>This is a blockquote.</p>
        
        <p>This is the second paragraph in the blockquote.</p>
        
        <h2>This is an H2 in a blockquote</h2>
    </blockquote>



### Phrase Emphasis ###

Markdown uses asterisks and underscores to indicate spans of emphasis.

Markdown:

    Some of these words *are emphasized*.
    Some of these words _are emphasized also_.
    
    Use two asterisks for **strong emphasis**.
    Or, if you prefer, __use two underscores instead__.

Output:

    <p>Some of these words <em>are emphasized</em>.
    Some of these words <em>are emphasized also</em>.</p>
    
    <p>Use two asterisks for <strong>strong emphasis</strong>.
    Or, if you prefer, <strong>use two underscores instead</strong>.</p>
   


## Lists ##

Unordered (bulleted) lists use asterisks, pluses, and hyphens (*,
+, and -) as list markers. These three markers are
interchangable; this:

    *   Candy.
    *   Gum.
    *   Booze.

this:

    +   Candy.
    +   Gum.
    +   Booze.

and this:

    -   Candy.
    -   Gum.
    -   Booze.

all produce the same output:

    <ul>
    <li>Candy.</li>
    <li>Gum.</li>
    <li>Booze.</li>
    </ul>

Ordered (numbered) lists use regular numbers, followed by periods, as
list markers:

    1.  Red
    2.  Green
    3.  Blue

Output:

    <ol>
    <li>Red</li>
    <li>Green</li>
    <li>Blue</li>
    </ol>

If you put blank lines between items, you'll get <p> tags for the
list item text. You can create multi-paragraph list items by indenting
the paragraphs by 4 spaces or 1 tab:

    *   A list item.
    
        With multiple paragraphs.

    *   Another item in the list.

Output:

    <ul>
    <li><p>A list item.</p>
    <p>With multiple paragraphs.</p></li>
    <li><p>Another item in the list.</p></li>
    </ul>
    


### Links ###

Markdown supports two styles for creating links: *inline* and
*reference*. With both styles, you use square brackets to delimit the
text you want to turn into a link.

Inline-style links use parentheses immediately after the link text.
For example:

    This is an [example link](http://example.com/).

Output:

    <p>This is an <a href="http://example.com/">
    example link</a>.</p>

Optionally, you may include a title attribute in the parentheses:

    This is an [example link](http://example.com/ "With a Title").

Output:

    <p>This is an <a href="http://example.com/" title="With a Title">
    example link</a>.</p>

Reference-style links allow you to refer to your links by names, which
you define elsewhere in your document:

    I get 10 times more traffic from [Google][1] than from
    [Yahoo][2] or [MSN][3].

    [1]: http://google.com/        "Google"
    [2]: http://search.yahoo.com/  "Yahoo Search"
    [3]: http://search.msn.com/    "MSN Search"

Output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from <a href="http://search.yahoo.com/"
    title="Yahoo Search">Yahoo</a> or <a href="http://search.msn.com/"
    title="MSN Search">MSN</a>.</p>

The title attribute is optional. Link names may contain letters,
numbers and spaces, but are *not* case sensitive:

    I start my morning with a cup of coffee and
    [The New York Times][NY Times].

    [ny times]: http://www.nytimes.com/

Output:

    <p>I start my morning with a cup of coffee and
    <a href="http://www.nytimes.com/">The New York Times</a>.</p>


### Images ###

Image syntax is very much like link syntax.

Inline (titles are optional):

    ![alt text](/path/to/img.jpg "Title")

Reference-style:

    ![alt text][id]

    [id]: /path/to/img.jpg "Title"

Both of the above examples produce the same output:

    <img src="/path/to/img.jpg" alt="alt text" title="Title" />



### Code ###

In a regular paragraph, you can create code span by wrapping text in
backtick quotes. Any ampersands (&) and angle brackets (< or
>) will automatically be translated into HTML entities. This makes
it easy to use Markdown to write about HTML example code:

    I strongly recommend against using any <blink> tags.

    I wish SmartyPants used named entities like &mdash;
    instead of decimal-encoded entites like &#8212;.

Output:

    <p>I strongly recommend against using any
    <code>&lt;blink&gt;</code> tags.</p>
    
    <p>I wish SmartyPants used named entities like
    <code>&amp;mdash;</code> instead of decimal-encoded
    entites like <code>&amp;#8212;</code>.</p>


To specify an entire block of pre-formatted code, indent every line of
the block by 4 spaces or 1 tab. Just like with code spans, &, <,
and > characters will be escaped automatically.

Markdown:

    If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:

        <blockquote>
            <p>For example.</p>
        </blockquote>

Output:

    <p>If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:</p>
    
    <pre><code>&lt;blockquote&gt;
        &lt;p&gt;For example.&lt;/p&gt;
    &lt;/blockquote&gt;
    </code></pre>
Markdown: Syntax
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a href="/projects/markdown/basics" title="Markdown Basics">Basics</a></li>
    <li><a class="selected" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


*   [Overview](#overview)
    *   [Philosophy](#philosophy)
    *   [Inline HTML](#html)
    *   [Automatic Escaping for Special Characters](#autoescape)
*   [Block Elements](#block)
    *   [Paragraphs and Line Breaks](#p)
    *   [Headers](#header)
    *   [Blockquotes](#blockquote)
    *   [Lists](#list)
    *   [Code Blocks](#precode)
    *   [Horizontal Rules](#hr)
*   [Span Elements](#span)
    *   [Links](#link)
    *   [Emphasis](#em)
    *   [Code](#code)
    *   [Images](#img)
*   [Miscellaneous](#misc)
    *   [Backslash Escapes](#backslash)
    *   [Automatic Links](#autolink)


**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL][src].

  [src]: /projects/markdown/syntax.text

* * *

<h2 id="overview">Overview</h2>

<h3 id="philosophy">Philosophy</h3>

Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

Readability, however, is emphasized above all else. A Markdown-formatted
document should be publishable as-is, as plain text, without looking
like it's been marked up with tags or formatting instructions. While
Markdown's syntax has been influenced by several existing text-to-HTML
filters -- including [Setext] [1], [atx] [2], [Textile] [3], [reStructuredText] [4],
[Grutatext] [5], and [EtText] [6] -- the single biggest source of
inspiration for Markdown's syntax is the format of plain text email.

  [1]: http://docutils.sourceforge.net/mirror/setext.html
  [2]: http://www.aaronsw.com/2002/atx/
  [3]: http://textism.com/tools/textile/
  [4]: http://docutils.sourceforge.net/rst.html
  [5]: http://www.triptico.com/software/grutatxt.html
  [6]: http://ettext.taint.org/doc/

To this end, Markdown's syntax is comprised entirely of punctuation
characters, which punctuation characters have been carefully chosen so
as to look like what they mean. E.g., asterisks around a word actually
look like \*emphasis\*. Markdown lists look like, well, lists. Even
blockquotes look like quoted passages of text, assuming you've ever
used email.



<h3 id="html">Inline HTML</h3>

Markdown's syntax is intended for one purpose: to be used as a
format for *writing* for the web.

Markdown is not a replacement for HTML, or even close to it. Its
syntax is very small, corresponding only to a very small subset of
HTML tags. The idea is *not* to create a syntax that makes it easier
to insert HTML tags. In my opinion, HTML tags are already easy to
insert. The idea for Markdown is to make it easy to read, write, and
edit prose. HTML is a *publishing* format; Markdown is a *writing*
format. Thus, Markdown's formatting syntax only addresses issues that
can be conveyed in plain text.

For any markup that is not covered by Markdown's syntax, you simply
use HTML itself. There's no need to preface it or delimit it to
indicate that you're switching from Markdown to HTML; you just use
the tags.

The only restrictions are that block-level HTML elements -- e.g. <div>,
<table>, <pre>, <p>, etc. -- must be separated from surrounding
content by blank lines, and the start and end tags of the block should
not be indented with tabs or spaces. Markdown is smart enough not
to add extra (unwanted) <p> tags around HTML block-level tags.

For example, to add an HTML table to a Markdown article:

    This is a regular paragraph.

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    This is another regular paragraph.

Note that Markdown formatting syntax is not processed within block-level
HTML tags. E.g., you can't use Markdown-style *emphasis* inside an
HTML block.

Span-level HTML tags -- e.g. <span>, <cite>, or <del> -- can be
used anywhere in a Markdown paragraph, list item, or header. If you
want, you can even use HTML tags instead of Markdown formatting; e.g. if
you'd prefer to use HTML <a> or <img> tags instead of Markdown's
link or image syntax, go right ahead.

Unlike block-level HTML tags, Markdown syntax *is* processed within
span-level tags.


<h3 id="autoescape">Automatic Escaping for Special Characters</h3>

In HTML, there are two characters that demand special treatment: <
and &. Left angle brackets are used to start tags; ampersands are
used to denote HTML entities. If you want to use them as literal
characters, you must escape them as entities, e.g. &lt;, and
&amp;.

Ampersands in particular are bedeviling for web writers. If you want to
write about 'AT&T', you need to write 'AT&amp;T'. You even need to
escape ampersands within URLs. Thus, if you want to link to:

    http://images.google.com/images?num=30&q=larry+bird

you need to encode the URL as:

    http://images.google.com/images?num=30&amp;q=larry+bird

in your anchor tag href attribute. Needless to say, this is easy to
forget, and is probably the single most common source of HTML validation
errors in otherwise well-marked-up web sites.

Markdown allows you to use these characters naturally, taking care of
all the necessary escaping for you. If you use an ampersand as part of
an HTML entity, it remains unchanged; otherwise it will be translated
into &amp;.

So, if you want to include a copyright symbol in your article, you can write:

    &copy;

and Markdown will leave it alone. But if you write:

    AT&T

Markdown will translate it to:

    AT&amp;T

Similarly, because Markdown supports [inline HTML](#html), if you use
angle brackets as delimiters for HTML tags, Markdown will treat them as
such. But if you write:

    4 < 5

Markdown will translate it to:

    4 &lt; 5

However, inside Markdown code spans and blocks, angle brackets and
ampersands are *always* encoded automatically. This makes it easy to use
Markdown to write about HTML code. (As opposed to raw HTML, which is a
terrible format for writing about HTML syntax, because every single <
and & in your example code needs to be escaped.)


* * *


<h2 id="block">Block Elements</h2>


<h3 id="p">Paragraphs and Line Breaks</h3>

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing but spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

The implication of the "one or more consecutive lines of text" rule is
that Markdown supports "hard-wrapped" text paragraphs. This differs
significantly from most other text-to-HTML formatters (including Movable
Type's "Convert Line Breaks" option) which translate every line break
character in a paragraph into a <br /> tag.

When you *do* want to insert a <br /> break tag using Markdown, you
end a line with two or more spaces, then type return.

Yes, this takes a tad more effort to create a <br />, but a simplistic
"every line break is a <br />" rule wouldn't work for Markdown.
Markdown's email-style [blockquoting][bq] and multi-paragraph [list items][l]
work best -- and look better -- when you format them with hard breaks.

  [bq]: #blockquote
  [l]:  #list



<h3 id="header">Headers</h3>

Markdown supports two styles of headers, [Setext] [1] and [atx] [2].

Setext-style headers are "underlined" using equal signs (for first-level
headers) and dashes (for second-level headers). For example:

    This is an H1
    =============

    This is an H2
    -------------

Any number of underlining ='s or -'s will work.

Atx-style headers use 1-6 hash characters at the start of the line,
corresponding to header levels 1-6. For example:

    # This is an H1

    ## This is an H2

    ###### This is an H6

Optionally, you may "close" atx-style headers. This is purely
cosmetic -- you can use this if you think it looks better. The
closing hashes don't even need to match the number of hashes
used to open the header. (The number of opening hashes
determines the header level.) :

    # This is an H1 #

    ## This is an H2 ##

    ### This is an H3 ######


<h3 id="blockquote">Blockquotes</h3>

Markdown uses email-style > characters for blockquoting. If you're
familiar with quoting passages of text in an email message, then you
know how to create a blockquote in Markdown. It looks best if you hard
wrap the text and put a > before every line:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    > 
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

Markdown allows you to be lazy and only put the > before the first
line of a hard-wrapped paragraph:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

Blockquotes can be nested (i.e. a blockquote-in-a-blockquote) by
adding additional levels of >:

    > This is the first level of quoting.
    >
    > > This is nested blockquote.
    >
    > Back to the first level.

Blockquotes can contain other Markdown elements, including headers, lists,
and code blocks:

	> ## This is a header.
	> 
	> 1.   This is the first list item.
	> 2.   This is the second list item.
	> 
	> Here's some example code:
	> 
	>     return shell_exec("echo $input | $markdown_script");

Any decent text editor should make email-style quoting easy. For
example, with BBEdit, you can make a selection and choose Increase
Quote Level from the Text menu.


<h3 id="list">Lists</h3>

Markdown supports ordered (numbered) and unordered (bulleted) lists.

Unordered lists use asterisks, pluses, and hyphens -- interchangably
-- as list markers:

    *   Red
    *   Green
    *   Blue

is equivalent to:

    +   Red
    +   Green
    +   Blue

and:

    -   Red
    -   Green
    -   Blue

Ordered lists use numbers followed by periods:

    1.  Bird
    2.  McHale
    3.  Parish

It's important to note that the actual numbers you use to mark the
list have no effect on the HTML output Markdown produces. The HTML
Markdown produces from the above list is:

    <ol>
    <li>Bird</li>
    <li>McHale</li>
    <li>Parish</li>
    </ol>

If you instead wrote the list in Markdown like this:

    1.  Bird
    1.  McHale
    1.  Parish

or even:

    3. Bird
    1. McHale
    8. Parish

you'd get the exact same HTML output. The point is, if you want to,
you can use ordinal numbers in your ordered Markdown lists, so that
the numbers in your source match the numbers in your published HTML.
But if you want to be lazy, you don't have to.

If you do use lazy list numbering, however, you should still start the
list with the number 1. At some point in the future, Markdown may support
starting ordered lists at an arbitrary number.

List markers typically start at the left margin, but may be indented by
up to three spaces. List markers must be followed by one or more spaces
or a tab.

To make lists look nice, you can wrap items with hanging indents:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
        Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
        viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
        Suspendisse id sem consectetuer libero luctus adipiscing.

But if you want to be lazy, you don't have to:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.

If list items are separated by blank lines, Markdown will wrap the
items in <p> tags in the HTML output. For example, this input:

    *   Bird
    *   Magic

will turn into:

    <ul>
    <li>Bird</li>
    <li>Magic</li>
    </ul>

But this:

    *   Bird

    *   Magic

will turn into:

    <ul>
    <li><p>Bird</p></li>
    <li><p>Magic</p></li>
    </ul>

List items may consist of multiple paragraphs. Each subsequent
paragraph in a list item must be intended by either 4 spaces
or one tab:

    1.  This is a list item with two paragraphs. Lorem ipsum dolor
        sit amet, consectetuer adipiscing elit. Aliquam hendrerit
        mi posuere lectus.

        Vestibulum enim wisi, viverra nec, fringilla in, laoreet
        vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
        sit amet velit.

    2.  Suspendisse id sem consectetuer libero luctus adipiscing.

It looks nice if you indent every line of the subsequent
paragraphs, but here again, Markdown will allow you to be
lazy:

    *   This is a list item with two paragraphs.

        This is the second paragraph in the list item. You're
    only required to indent the first line. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit.

    *   Another item in the same list.

To put a blockquote within a list item, the blockquote's >
delimiters need to be indented:

    *   A list item with a blockquote:

        > This is a blockquote
        > inside a list item.

To put a code block within a list item, the code block needs
to be indented *twice* -- 8 spaces or two tabs:

    *   A list item with a code block:

            <code goes here>


It's worth noting that it's possible to trigger an ordered list by
accident, by writing something like this:

    1986. What a great season.

In other words, a *number-period-space* sequence at the beginning of a
line. To avoid this, you can backslash-escape the period:

    1986\. What a great season.



<h3 id="precode">Code Blocks</h3>

Pre-formatted code blocks are used for writing about programming or
markup source code. Rather than forming normal paragraphs, the lines
of a code block are interpreted literally. Markdown wraps a code block
in both <pre> and <code> tags.

To produce a code block in Markdown, simply indent every line of the
block by at least 4 spaces or 1 tab. For example, given this input:

    This is a normal paragraph:

        This is a code block.

Markdown will generate:

    <p>This is a normal paragraph:</p>

    <pre><code>This is a code block.
    </code></pre>

One level of indentation -- 4 spaces or 1 tab -- is removed from each
line of the code block. For example, this:

    Here is an example of AppleScript:

        tell application "Foo"
            beep
        end tell

will turn into:

    <p>Here is an example of AppleScript:</p>

    <pre><code>tell application "Foo"
        beep
    end tell
    </code></pre>

A code block continues until it reaches a line that is not indented
(or the end of the article).

Within a code block, ampersands (&) and angle brackets (< and >)
are automatically converted into HTML entities. This makes it very
easy to include example HTML source code using Markdown -- just paste
it and indent it, and Markdown will handle the hassle of encoding the
ampersands and angle brackets. For example, this:

        <div class="footer">
            &copy; 2004 Foo Corporation
        </div>

will turn into:

    <pre><code>&lt;div class="footer"&gt;
        &amp;copy; 2004 Foo Corporation
    &lt;/div&gt;
    </code></pre>

Regular Markdown syntax is not processed within code blocks. E.g.,
asterisks are just literal asterisks within a code block. This means
it's also easy to use Markdown to write about Markdown's own syntax.



<h3 id="hr">Horizontal Rules</h3>

You can produce a horizontal rule tag (<hr />) by placing three or
more hyphens, asterisks, or underscores on a line by themselves. If you
wish, you may use spaces between the hyphens or asterisks. Each of the
following lines will produce a horizontal rule:

    * * *

    ***

    *****
	
    - - -

    ---------------------------------------

	_ _ _


* * *

<h2 id="span">Span Elements</h2>

<h3 id="link">Links</h3>

Markdown supports two style of links: *inline* and *reference*.

In both styles, the link text is delimited by [square brackets].

To create an inline link, use a set of regular parentheses immediately
after the link text's closing square bracket. Inside the parentheses,
put the URL where you want the link to point, along with an *optional*
title for the link, surrounded in quotes. For example:

    This is [an example](http://example.com/ "Title") inline link.

    [This link](http://example.net/) has no title attribute.

Will produce:

    <p>This is <a href="http://example.com/" title="Title">
    an example</a> inline link.</p>

    <p><a href="http://example.net/">This link</a> has no
    title attribute.</p>

If you're referring to a local resource on the same server, you can
use relative paths:

    See my [About](/about/) page for details.

Reference-style links use a second set of square brackets, inside
which you place a label of your choosing to identify the link:

    This is [an example][id] reference-style link.

You can optionally use a space to separate the sets of brackets:

    This is [an example] [id] reference-style link.

Then, anywhere in the document, you define your link label like this,
on a line by itself:

    [id]: http://example.com/  "Optional Title Here"

That is:

*   Square brackets containing the link identifier (optionally
    indented from the left margin using up to three spaces);
*   followed by a colon;
*   followed by one or more spaces (or tabs);
*   followed by the URL for the link;
*   optionally followed by a title attribute for the link, enclosed
    in double or single quotes.

The link URL may, optionally, be surrounded by angle brackets:

    [id]: <http://example.com/>  "Optional Title Here"

You can put the title attribute on the next line and use extra spaces
or tabs for padding, which tends to look better with longer URLs:

    [id]: http://example.com/longish/path/to/resource/here
        "Optional Title Here"

Link definitions are only used for creating links during Markdown
processing, and are stripped from your document in the HTML output.

Link definition names may constist of letters, numbers, spaces, and punctuation -- but they are *not* case sensitive. E.g. these two links:

	[link text][a]
	[link text][A]

are equivalent.

The *implicit link name* shortcut allows you to omit the name of the
link, in which case the link text itself is used as the name.
Just use an empty set of square brackets -- e.g., to link the word
"Google" to the google.com web site, you could simply write:

	[Google][]

And then define the link:

	[Google]: http://google.com/

Because link names may contain spaces, this shortcut even works for
multiple words in the link text:

	Visit [Daring Fireball][] for more information.

And then define the link:
	
	[Daring Fireball]: http://daringfireball.net/

Link definitions can be placed anywhere in your Markdown document. I
tend to put them immediately after each paragraph in which they're
used, but if you want, you can put them all at the end of your
document, sort of like footnotes.

Here's an example of reference links in action:

    I get 10 times more traffic from [Google] [1] than from
    [Yahoo] [2] or [MSN] [3].

      [1]: http://google.com/        "Google"
      [2]: http://search.yahoo.com/  "Yahoo Search"
      [3]: http://search.msn.com/    "MSN Search"

Using the implicit link name shortcut, you could instead write:

    I get 10 times more traffic from [Google][] than from
    [Yahoo][] or [MSN][].

      [google]: http://google.com/        "Google"
      [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
      [msn]:    http://search.msn.com/    "MSN Search"

Both of the above examples will produce the following HTML output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from
    <a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a>
    or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p>

For comparison, here is the same paragraph written using
Markdown's inline link style:

    I get 10 times more traffic from [Google](http://google.com/ "Google")
    than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or
    [MSN](http://search.msn.com/ "MSN Search").

The point of reference-style links is not that they're easier to
write. The point is that with reference-style links, your document
source is vastly more readable. Compare the above examples: using
reference-style links, the paragraph itself is only 81 characters
long; with inline-style links, it's 176 characters; and as raw HTML,
it's 234 characters. In the raw HTML, there's more markup than there
is text.

With Markdown's reference-style links, a source document much more
closely resembles the final output, as rendered in a browser. By
allowing you to move the markup-related metadata out of the paragraph,
you can add links without interrupting the narrative flow of your
prose.


<h3 id="em">Emphasis</h3>

Markdown treats asterisks (*) and underscores (_) as indicators of
emphasis. Text wrapped with one * or _ will be wrapped with an
HTML <em> tag; double *'s or _'s will be wrapped with an HTML
<strong> tag. E.g., this input:

    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__

will produce:

    <em>single asterisks</em>

    <em>single underscores</em>

    <strong>double asterisks</strong>

    <strong>double underscores</strong>

You can use whichever style you prefer; the lone restriction is that
the same character must be used to open and close an emphasis span.

Emphasis can be used in the middle of a word:

    un*fucking*believable

But if you surround an * or _ with spaces, it'll be treated as a
literal asterisk or underscore.

To produce a literal asterisk or underscore at a position where it
would otherwise be used as an emphasis delimiter, you can backslash
escape it:

    \*this text is surrounded by literal asterisks\*



<h3 id="code">Code</h3>

To indicate a span of code, wrap it with backtick quotes (  ).
Unlike a pre-formatted code block, a code span indicates code within a
normal paragraph. For example:

    Use the printf() function.

will produce:

    <p>Use the <code>printf()</code> function.</p>

To include a literal backtick character within a code span, you can use
multiple backticks as the opening and closing delimiters:

     There is a literal backtick () here.

which will produce this:

    <p><code>There is a literal backtick () here.</code></p>

The backtick delimiters surrounding a code span may include spaces --
one after the opening, one before the closing. This allows you to place
literal backtick characters at the beginning or end of a code span:

	A single backtick in a code span:     
	
	A backtick-delimited string in a code span:   foo  

will produce:

	<p>A single backtick in a code span: <code></code></p>
	
	<p>A backtick-delimited string in a code span: <code>foo</code></p>

With a code span, ampersands and angle brackets are encoded as HTML
entities automatically, which makes it easy to include example HTML
tags. Markdown will turn this:

    Please don't use any <blink> tags.

into:

    <p>Please don't use any <code>&lt;blink&gt;</code> tags.</p>

You can write this:

    &#8212; is the decimal-encoded equivalent of &mdash;.

to produce:

    <p><code>&amp;#8212;</code> is the decimal-encoded
    equivalent of <code>&amp;mdash;</code>.</p>



<h3 id="img">Images</h3>

Admittedly, it's fairly difficult to devise a "natural" syntax for
placing images into a plain text document format.

Markdown uses an image syntax that is intended to resemble the syntax
for links, allowing for two styles: *inline* and *reference*.

Inline image syntax looks like this:

    ![Alt text](/path/to/img.jpg)

    ![Alt text](/path/to/img.jpg "Optional title")

That is:

*   An exclamation mark: !;
*   followed by a set of square brackets, containing the alt
    attribute text for the image;
*   followed by a set of parentheses, containing the URL or path to
    the image, and an optional title attribute enclosed in double
    or single quotes.

Reference-style image syntax looks like this:

    ![Alt text][id]

Where "id" is the name of a defined image reference. Image references
are defined using syntax identical to link references:

    [id]: url/to/image  "Optional title attribute"

As of this writing, Markdown has no syntax for specifying the
dimensions of an image; if this is important to you, you can simply
use regular HTML <img> tags.


* * *


<h2 id="misc">Miscellaneous</h2>

<h3 id="autolink">Automatic Links</h3>

Markdown supports a shortcut style for creating "automatic" links for URLs and email addresses: simply surround the URL or email address with angle brackets. What this means is that if you want to show the actual text of a URL or email address, and also have it be a clickable link, you can do this:

    <http://example.com/>
    
Markdown will turn this into:

    <a href="http://example.com/">http://example.com/</a>

Automatic links for email addresses work similarly, except that
Markdown will also perform a bit of randomized decimal and hex
entity-encoding to help obscure your address from address-harvesting
spambots. For example, Markdown will turn this:

    <address@example.com>

into something like this:

    <a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
    &#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
    &#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
    &#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>

which will render in a browser as a clickable link to "address@example.com".

(This sort of entity-encoding trick will indeed fool many, if not
most, address-harvesting bots, but it definitely won't fool all of
them. It's better than nothing, but an address published in this way
will probably eventually start receiving spam.)



<h3 id="backslash">Backslash Escapes</h3>

Markdown allows you to use backslash escapes to generate literal
characters which would otherwise have special meaning in Markdown's
formatting syntax. For example, if you wanted to surround a word with
literal asterisks (instead of an HTML <em> tag), you can backslashes
before the asterisks, like this:

    \*literal asterisks\*

Markdown provides backslash escapes for the following characters:

    \   backslash
       backtick
    *   asterisk
    _   underscore
    {}  curly braces
    []  square brackets
    ()  parentheses
    #   hash mark
	+	plus sign
	-	minus sign (hyphen)
    .   dot
    !   exclamation mark

# Character Escapes

The MD5 value for + is "26b17225b626fb9238849fd60eabdf60".

# HTML Blocks

<p>test</p>

The MD5 value for <p>test</p> is:

6205333b793f34273d75379350b36826* test
+ test
- test

1. test
2. test

* test
+ test
- test

1. test
2. test
> foo
>
> > bar
>
> foo
Valid nesting:

**[Link](url)**

[**Link**](url)

**[**Link**](url)**

Invalid nesting:

[[Link](url)](url)## Unordered

Asterisks tight:

*	asterisk 1
*	asterisk 2
*	asterisk 3


Asterisks loose:

*	asterisk 1

*	asterisk 2

*	asterisk 3

* * *

Pluses tight:

+	Plus 1
+	Plus 2
+	Plus 3


Pluses loose:

+	Plus 1

+	Plus 2

+	Plus 3

* * *


Minuses tight:

-	Minus 1
-	Minus 2
-	Minus 3


Minuses loose:

-	Minus 1

-	Minus 2

-	Minus 3


## Ordered

Tight:

1.	First
2.	Second
3.	Third

and:

1. One
2. Two
3. Three


Loose using tabs:

1.	First

2.	Second

3.	Third

and using spaces:

1. One

2. Two

3. Three

Multiple paragraphs:

1.	Item 1, graf one.

	Item 2. graf two. The quick brown fox jumped over the lazy dog's
	back.
	
2.	Item 2.

3.	Item 3.



## Nested

*	Tab
	*	Tab
		*	Tab

Here's another:

1. First
2. Second:
	* Fee
	* Fie
	* Foe
3. Third

Same thing but with paragraphs:

1. First

2. Second:
	* Fee
	* Fie
	* Foe

3. Third


This was an error in Markdown 1.0.1:

*	this

	*	sub

	that
[Inline link 1 with parens](/url\(test\) "title").

[Inline link 2 with parens](</url\(test\)> "title").

[Inline link 3 with non-escaped parens](/url(test) "title").

[Inline link 4 with non-escaped parens](</url(test)> "title").

[Reference link 1 with parens][1].

[Reference link 2 with parens][2].

  [1]: /url(test) "title"
  [2]: </url(test)> "title"
This tests for a bug where quotes escaped by PHP when using 
preg_replace with the /e modifier must be correctly unescaped
(hence the _UnslashQuotes function found only in PHP Markdown).



Headers below should appear exactly as they are typed (no backslash
added or removed).

Header "quoted\" again \\""
===========================

Header "quoted\" again \\""
---------------------------

### Header "quoted\" again \\"" ###



Test with tabs for _Detab:

	Code	'block'	with	some	"tabs"	and	"quotes"
[Test](/"style="color:red)
[Test](/'style='color:red)

![](/"style="border-color:red;border-size:1px;border-style:solid)
![](/'style='border-color:red;border-size:1px;border-style:solid)
***This is strong and em.***

So is ***this*** word.

___This is strong and em.___

So is ___this___ word.
# Simple tables

Header 1  | Header 2
--------- | ---------
Cell 1    | Cell 2
Cell 3    | Cell 4

With leading pipes:

| Header 1  | Header 2
| --------- | ---------
| Cell 1    | Cell 2
| Cell 3    | Cell 4

With tailing pipes:

Header 1  | Header 2  |
--------- | --------- |
Cell 1    | Cell 2    |
Cell 3    | Cell 4    |

With leading and tailing pipes:

| Header 1  | Header 2  |
| --------- | --------- |
| Cell 1    | Cell 2    |
| Cell 3    | Cell 4    |

* * *

# One-column one-row table

With leading pipes:

| Header
| -------
| Cell

With tailing pipes:

Header  |
------- |
Cell    |

With leading and tailing pipes:

| Header  |
| ------- |
| Cell    |

* * *

Table alignement:

| Default   | Right     |  Center   |     Left  |
| --------- |:--------- |:---------:| ---------:|
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

Table alignement (alternate spacing):

| Default   | Right     |  Center   |     Left  |
| --------- | :-------- | :-------: | --------: |
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

* * * 

# Empty cells

| Header 1  | Header 2  |
| --------- | --------- |
| A         | B         |
| C         |           |

Header 1  | Header 2
--------- | ---------
A         | B
          | D

* * *

# Missing tailing pipe

Header 1  | Header 2  
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- 
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      

* * *

# Too many pipes in rows

| Header 1  | Header 2  |
| --------- 
| Cell      | Cell      | Extra cell? |
| Cell      | Cell      | Extra cell? |

+	this is a list item
	indented with tabs

+   this is a list item
    indented with spaces

Code:

	this code block is indented by one tab

And:

		this code block is indented by two tabs

And:

	+	this is an example list item
		indented with tabs
	
	+   this is an example list item
	    indented with spaces
> A list within a blockquote:
> 
> *	asterisk 1
> *	asterisk 2
> *	asterisk 3
Paragraph and no space:
* ciao

Paragraph and 1 space:
 * ciao

Paragraph and 3 spaces:
  * ciao

Paragraph and 4 spaces:
   * ciao

Paragraph before header:
#Header

Paragraph before blockquote:
>Some quote.
 .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>


As above: checking for bad interractions with the HTML block parser:

 html
<div>


Some *markdown* formatting.

 html
</div>


Some *markdown*


<div>
    <html>



function test();


<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">

<html>
    <title>

</div>

Two code blocks with no blank line between them:


<div>


<div>


Testing *confusion* with markers in the middle:


<div></div>


Testing mixing with title code blocks


<p>
 
<p>

 
<p>

<p>
 

<Fenced>


Code block starting and ending with empty lines:



<Fenced>




Indented code block containing fenced code block sample:

	
	<Fenced>
	

Fenced code block with indented code block sample:


Some text

	Indented code block sample code


Fenced code block with long markers:


Fenced


Fenced code block with fenced code block markers of different length in it:


In code block

Still in code block

Still in code block


Fenced code block with Markdown header and horizontal rule:


#test
---


Fenced code block with link definitions, footnote definition and 
abbreviation definitions:


[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language


* In a list item with smalish indent:

  
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
  
  
With HTML content.
  

<b>bold</b>


Bug with block level elements in this case:

  <div>
  </div>


Indented code block of a fenced code block:

    
	haha!
	

With class:
  
html
<b>bold</b>

  
 html
<b>bold</b>

  
.html
<b>bold</b>

  
 .html
<b>bold</b>


With extra attribute block:

{.html}
<b>bold</b>

  
 {.html #codeid}
<b>bold</b>


 .html{.bold}
<div>

  
 .html {#codeid}
</div>
First line. <br/>
Second line.

This is a first paragraph,
on multiple lines.
     
This is a second paragraph.
There are spaces in between the two.This is a first paragraph,
on multiple lines.

This is a second paragraph
which has multiple lines too.A first paragraph.



A second paragraph after 3 CR (carriage return).This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
     
A few spaces and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
	
1 tab to separate them and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.

A new long long long long long long long long long long long long long long long long paragraph on 1 line.An ampersand & in the text flow is escaped as an html entity.There is an [ampersand](http://validator.w3.org/check?uri=http://www.w3.org/&verbose=1) in the URI.This is \*an asterisk which should stay as is.This is * an asterisk which should stay as is.\\   backslash
\   backtick
\*   asterisk
\_   underscore
\{\}  curly braces
\[\]  square brackets
\(\)  parentheses
\#   hash mark
\+   plus sign
\-   minus sign (hyphen)
\.   dot
\!   exclamation mark> # heading level 1
> 
> paragraph>A blockquote with a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.

>and a second very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.>This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a blockquote.> A blockquote
> on multiple lines
> like this.>A blockquote 
>on multiple lines 
>like this. >A blockquote
>on multiple lines
>like this.
>
>But it has
>two paragraphs.>A blockquote
>on multiple lines
>like this> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.
> This is the first level of quoting.
>
> > This is nested blockquote.> This is the first level of quoting.
> > This is nested blockquote.
> Back to the first level.
> This is the first level of quoting.
> > This is nested blockquote.
	10 PRINT HELLO INFINITE
	20 GOTO 10    10 PRINT < > &
    20 GOTO 10    10 PRINT HELLO INFINITE
    20 GOTO 10# Contributing to Mardown Test Suite

1. [Getting Involved](#getting-involved)
2. [Discussion](#discussion)
3. [How To Report an Issue](#how-to-report-an-issue)
4. [Editing Markdown Specification](#editing-markdown-specification)
5. [Test Suite Guidelines](#test-suite-guidelines)
6. [Pull Request Guidelines](#pull-request-guidelines)

## Getting Involved

There are a number of ways to get involved with the development of the Markdown Test Suite. If you are a first time contributor to an open source project, you can still add value to this project. You may identify grammar issues, write prose, examples or documentation for the project. You may flag some errors and open new issues.

Read all bits of this document and that will guide you on how to participate.

## Discussion

### Mailing List

The Markdown Test Suite has been started a little bit after the start of the [Markdown Community Group](http://www.w3.org/community/markdown/). You may want to discuss about Markdown and this project on the [group mailing-list](http://lists.w3.org/Archives/Public/public-markdown/).

## How to Report an Issue

Don't be afraid to add details to your issue. The more context you give, the better for people participating to the project. Make a short summary, add a description with the context and give links to places which will help to understand.

## Editing Markdown Specification

There is much needed work on the [Markdown Specification](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html). It doesn't require strong competences in coding. Be systematic in the markup and follow the way it is already organized. Each time you added a new atomic section, create a commit for this specific part.

## Test Suite Guidelines

When proposing new tests, make sure they do not already exist in the current test suite. You will notice that there is a separate section dedicated to the specific extensions that some markdown generators have created. Keep them separate. We want to keep the core clean and close to the original specification of Markdown.

If you are not sure, create an issue.

### Markdown Extensions

Markdown extension tests are accepted. Use the following rules:

- place all extension tests under the test/extensions/ENGINE directory with filename equal to the feature name
- for each ENGINE and add a README.markdown under the engine directory with a link to its specification

where ENGINE is either of:

- a command line utility. E.g. pandoc, kramdown.
- a programming API. E.g. Redcarpet::Markdown.new().
- a programmatically accessible web service. E.g.: GFM via the GitHub API.
- a non programmatically accessible web service. E.g.: Stack Overflow flavored markdown.

To avoid test duplication for common features, use the following rules:

- if file tests/extensions/ENGINE/FEATURE.md is empty or not present, use tests/extensions/FEATURE.md instead
- if file tests/extensions/ENGINE/FEATURE.out not present, use tests/extensions/FEATURE.out instead
- for a given ENGINE, only features which have either a .md or a .out are implemented by that engine.
- in case of different outputs for a single feature input, keep directly under extensions/ only the output case that happens across the most engines

**version**

Only the latest stable version of each ENGINE is considered.

**options**

The IO behavior tested is for engine defaults, without any options (command line options, extra JSON parameters, etc.) passed to the engine.

**external state**

Tests that use external state not present in the markdown input shall not be included in this test suite.

For example, what GFM @user user tags render to also depends on the state of GitHub's databases (only render to a link if user exists), not only on the input markdown.

#### Examples

GFM and the "fenced code block" use the following file structure:

    tests/extensions/gfm/README.markdown
    tests/extensions/gfm/fenced-code-block.md
    tests/extensions/gfm/fenced-code-block.out

where README.markdown contains:

    https://help.github.com/articles/github-flavored-markdown

To avoid duplication with other engines, if the input / output (normalized to DOM) is the same across multiple engines use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

If the input is the same, and outputs are DOM different, but represent the same idea (e.g. both represent computer code) use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/gfm/fenced-code-block.out
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

#### New Extensions

Tests are modular, and if you want to test a new engine for your project, that should be easy to do.

If you feel that the new engine is reasonably popular, please send a pull request adding it.

## Commits and Pull Requests

* Keep your commits clean and commented
* Do not mix in one commit different things. Keep modifications related.
* Do not mix everything in one giant pull request. Create separate pull requests for different topic. That will help to have a more meaningful debate about the pull requests and will help to review the code.
* If it relates to a specific issue, add the number of the issue in the commit message.

Thanks for Contributing
as*te*risks*single asterisks*_single underscores_HTML entities are written using ampersand notation: &copy;These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

This is an H1
=============# This is an H1 # # This is an H1# this is an h1 with two trailing spaces  
A new paragraph.# This is an H1This is an H2
-------------## This is an H2 #### This is an H2### This is an H3 ###### This is an H3#### This is an H4 ######## This is an H4##### This is an H5 ########## This is an H5###### This is an H6  ############ This is an H6- - ----***___-------![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 for everyone"![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 logo for everyone")![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png)We love <code> and & for everything We love code for everything We love code for everything The MIT License (MIT)

Copyright (c) 2013 Karl Dubost

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
A first sentence  
and a line break.A first sentence     
and a line break.This is an automatic link <http://www.w3.org/>[W3C](http://www.w3.org/ "Discover w3c")[W3C](http://www.w3.org/)[World Wide Web Consortium][w3c]

[w3c]: <http://www.w3.org/>[World Wide Web Consortium][]

[World Wide Web Consortium]: http://www.w3.org/[w3c][]

[w3c]: http://www.w3.org/[World Wide Web Consortium] [w3c]

[w3c]: http://www.w3.org/[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/
   "Discover W3C"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ (Discover w3c)[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ 'Discover w3c'[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ "Discover w3c"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/*   a list containing a blockquote

    > this the blockquote in the list* a

        b
*   a list containing a block of code

	    10 PRINT HELLO INFINITE
	    20 GOTO 10*   This is a list item with two paragraphs. Lorem ipsum dolor
	sit amet, consectetuer adipiscing elit. Aliquam hendrerit
	mi posuere lectus.

	Vestibulum enim wisi, viverra nec, fringilla in, laoreet
	vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
	sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.*   This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.1\. ordered list escape1. 1

    - inner par list

2. 2
1. list item 1
8. list item 2
1. list item 31. list item 1
2. list item 2
3. list item 3This is a paragraph
on multiple lines
with hard return.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line. This is a paragraph with a trailing and leading space. This is a paragraph with 1 trailing tab.	  This is a paragraph with 2 leading spaces.   This is a paragraph with 3 leading spaces. This is a paragraph with 1 leading space.This is a paragraph with a trailing space. # Colophon - October 1st, 2014

This project was initiated to provide a test suite for Markdown markup, and eventually create a specification from this test results. A part of of the community has started a new endeavor which seems to get traction as [CommonMark](https://github.com/jgm/stmd). **We are then closing this project** and encourage you to contribute to CommonMark. 

The most interesting part of this project would not have been possible without the dedication of [Ciro Santilli](https://github.com/cirosantilli) @cirosantilli. So big applause and thank you to him.


The rest is kept around for archives and references.

# Markdown Test Suite

Inspired by questions on [W3C Markdown Community Group](http://www.w3.org/community/markdown).

Pull Requests are welcome. See the [CONTRIBUTING Guidelines](https://github.com/karlcow/markdown-testsuite/blob/master/CONTRIBUTING.md)

## Design goals

- Comprehensive.
- Small modularized tests.
- Easy to run tests using any programming language. In particular, data representations must have an implementation on all major languages.
- Develop a consensus based markdown specification at [markdown-spec.html](markdown-spec.html). Visualize it [here](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html).

## Test Scripts

Markdown Test Suite already includes tests for many important markdown engines.

To see what the scripts do run:

    ./cat-all.py -h
    ./run-tests.py -h

To configure the scripts do:

	cp config_local.py.example config_local.py

and edit config_local.py. It is already gitignored.

A Vagrantfile is provided with a provision script that installs all installable engines.

Sample output from run-tests.py:

    blackfriday   |......FFF..............FF...F....................................F....................................|   0.93s  102    7   6%
	gfm           |FF.....F.....F...FFFF..F....F........................FFFF...FF...............FF...F.......F...........| 262.88s  102   20  19%
    hoedown       |..............................F.................................................F.....................|   0.36s  102    2   1%
	kramdown      |......FFF.....FF.......FF.......FF.FFFFFFFFFFFFF.......................F..............................|  30.69s  102   23  22%
    lunamark      |FFFFFF.F.FFFFFFFFFFFF.F.....FFFF..FF............FFFFF..FFFFFFFFFF..............F...FFFFFFFFFFF........|   1.58s  103   53  51%
    markdown_pl   |.....................FFFF...............................F...............F.............................|   2.56s  102    6   5%
    markdown2     |......................................................................................................|   5.39s  103    0   0%
    marked        |..............F.................FFFFFFFFFFFFFFFF......................F.F.............................|   6.22s  102   19  18%
    maruku        |......FFF......F.......F.FFF...............................................FF.........................|  37.02s  102   10   9%
    md2html       |.........................FFF...F............................................FF........................|   7.42s  102    6   5%
    multimarkdown |......FFF....FF...F............FFF.FFFFFFFFFFFFF.....FFFF.........F...................................|   0.58s  102   27  26%
    pandoc        |FF...........F.F.FFFF..FFFFF....FF.FFFFFFFFFFFFF.....FFFF.....FF............FFF.FFF..................F|   1.11s  102   41  40%
    peg_markdown  |.................................................................F....................................|   0.46s  102    1   0%
    rdiscount     |.......F.........................................................F....................................|  25.19s  102    3   2%
    redcarpet     |......................................................................................................|  21.49s  102    0   0%
    showdown      |.......................................................................F..............................|   6.85s  102    1   0%

	Extensions:

    blackfriday   |F..|  0.04s    3    1  33%
	gfm           |F.|   2.37s    2    1  50%
    hoedown       |.|    0.00s    1    0   0%
    lunamark      |F.F|  0.05s    3    2  66%
    kramdown      |..|   0.62s    2    0   0%
    markdown_pl   ||     0.00s    0    0   0%
    markdown2     |F.|   0.14s    2    1  50%
    marked        |F.|   0.13s    2    1  50%
    maruku        |F..|  1.06s    3    1  33%
    md2html       |F.|   0.14s    2    0   0%
    multimarkdown |F.|   0.01s    2    1  50%
    pandoc        |F.|   0.02s    2    1  50%
    peg_markdown  |...|  0.02s    3    0   0%
    rdiscount     |F..|   0.74s    3    1  33%
    redcarpet     |..|   0.42s    2    0   0%
    showdown      |F..|  0.20s    3    1  33%

Where F indicates a failing test.

## Other Noticeable Test Suites

We haven't been the first test suite effort. Some projects have maintained their own test suite for a long time. Hopefully we can reach a state where people agree on the terms of what should be a good test suite for all developers.

- [Original test suite](http://daringfireball.net/projects/downloads/MarkdownTest_1.0.zip)
- [PHP markdown test suite:](https://github.com/michelf/mdtest/tree/master/Markdown.mdtest)
- [Markdown-js test suite](https://github.com/evilstreak/markdown-js/tree/master/test/features)
- [Python markdown 2 test suite](https://github.com/trentm/python-markdown2/tree/master/test/tm-cases)
- [multimarkdown test suite](https://github.com/fletcher/MMD-Test-Suite)
- [John MacFarlane's Standard Markdown spec](https://github.com/jgm/stmd)

In addition we should note the [wonderful work](http://johnmacfarlane.net/babelmark2/) made by John Mac Farlane. The Web service output the differences in between the different markdown implementations. It helps a lot when searching on the most common output.
as**te**risks**double asterisks**__double underscores__* list item 1
* list item 2
* list item 3
- list item 1
- list item 2
- list item 3 * list item 1
 * list item 2
 * list item 3  * list item 1
  * list item 2
  * list item 3   * list item 1
   * list item 2
   * list item 3+ list item 1
+ list item 2
+ list item 3* list item in paragraph

* another list item in paragraph*   This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a list.
*   and yet another long long long long long long long long long long long long long long long long long long long long long long line.*   This is a list item
    with the content on
    multiline and indented.
*   And this another list item
    with the same principle.€Some text about HTML, SGML and HTML4.

Let's talk about the U.S.A., (É.U. or É.-U. d'A. in French).

*[HTML4]: Hyper Text Markup Language version 4
*[HTML]: Hyper Text Markup Language
*[SGML]: Standard Generalized Markup Language
*[U.S.A.]: United States of America
*[É.U.] : États-Unis d'Amérique
*[É.-U. d'A.] : États-Unis d'Amérique

And here we have a CD, some CDs, and some other CD's.

*[CD]: Compact Disk

Let's transfert documents through TCP/IP, using TCP packets.

*[IP]: Internet Protocol
*[TCP]: Transmission Control Protocol

 ---

Bienvenue sur [CMS](http://www.bidulecms.com "Bidule CMS").

*[CMS]: Content Management System

 ---

ATCCE

*[ATCCE]: Abbreviation "Testing" Correct 'Character' < Escapes >* one
* two

1. three
2. four

* one
* two
1. three
2. fourAT&T has an ampersand in their name.

AT&amp;T is another way to write it.

This & that.

4 < 5.

6 > 5.

Here's a [link] [1] with an ampersand in the URL.

Here's a link with an amersand in the link text: [AT&T] [2].

Here's an inline [link](/script?foo=1&bar=2).

Here's an inline [link](</script?foo=1&bar=2>).


[1]: http://example.com/?foo=1&bar=2
[2]: http://att.com/  "AT&T"Link: <http://example.com/>.

With an ampersand: <http://example.com/?foo=1&bar=2>

* In a list?
* <http://example.com/>
* It should.

> Blockquoted: <http://example.com/>

Auto-links should not occur here: <http://example.com/>

	or here: <http://example.com/>These should all get escaped:

Backslash: \\

Backtick: \

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-



These should not, because they occur within a code block:

	Backslash: \\

	Backtick: \

	Asterisk: \*

	Underscore: \_

	Left brace: \{

	Right brace: \}

	Left bracket: \[

	Right bracket: \]

	Left paren: \(

	Right paren: \)

	Greater-than: \>

	Hash: \#

	Period: \.

	Bang: \!

	Plus: \+

	Minus: \-


Nor should these, which occur in code spans:

Backslash: \\

Backtick:   \  

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-


These should get escaped, even though they're matching pairs for
other Markdown constructs:

\*asterisks\*

\_underscores\_

\backticks\

This is a code span with a literal backslash-backtick sequence:   \  

This is a tag with unescaped backticks <span attr='ticks'>bar</span>.

This is a tag with backslashes <span attr='\\backslashes\\'>bar</span>.
  .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>
 

As above: checking for bad interractions with the HTML block parser:

  html
<div>
 

Some *markdown* formatting.

  html
</div>
 

Some *markdown*

 
<div>
    <html>
 

 
function test();
 

<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">
 
<html>
    <title>
 
</div>

Two code blocks with no blank line between them:

 
<div>
 
 
<div>
 

Testing *confusion* with code spans at the HTML block parser:

 
<div></div>
 

Testing mixing with title code blocks

 
<p>

<p>
 

<p>
 
<p>

 
<Fenced>
 

Code block starting and ending with empty lines:
 


<Fenced>


 

Indented code block containing fenced code block sample:

	 
	<Fenced>
	 

Fenced code block with indented code block sample:

 
Some text

	Indented code block sample code
 

Fenced code block with long markers:

 
Fenced
 

Fenced code block with fenced code block markers of different length in it:

 
In code block
 
Still in code block
 
Still in code block
 

Fenced code block with Markdown header and horizontal rule:

 
#test
---
 

Fenced code block with link definitions, footnote definition and
abbreviation definitions:

 
[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language
 

* In a list item with smalish indent:

   
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
   

With HTML content.

 
<b>bold</b>
 

Bug with block level elements in this case:
 
  <div>
  </div>
 

Indented code block of a fenced code block:

     
	haha!
	 

With class:

 html
<b>bold</b>
 

  html
<b>bold</b>
 

 .html
<b>bold</b>
 

  .html
<b>bold</b>
 

With extra attribute block:

 {.html}
<b>bold</b>
 

  {.html #codeid}
<b>bold</b>
 

  .html{.bold}
<div>
 
  
  .html {#codeid}
</div>
 > Example:
> 
>     sub status {
>         print "working";
>     }
> 
> Or:
> 
>     sub status {
>         return "working";
>     }

*	List Item:

		code block

		with a blank line

	within a list item.

*       code block
        as first element of a list item

*	List Item:
	
		code block with whitespace on preceding line
    Codeblock on second line
    <?php
    echo "hello!";
    ?>

foo bar

    <?php
    echo "hello!";

lorem ipsum

    echo "hello!";
    ?>
    
lorem ipsum	code block on the first line
	
Regular text.

    code block indented by spaces

Regular text.

	the lines in this block  
	all contain trailing spaces  

Regular Text.

	code block on the last line<test a=" content of attribute ">

Fix for backticks within HTML tag: <span attr='ticks'>like this</span>

Here's how you put   backticks   in a code span.A simple definition list:

Term 1
:   Definition 1

Term 2
:   Definition 2

With multiple terms:

Term 1
Term 2
:   Definition 1

Term 3
Term 4
:   Definition 2

With multiple definitions:

Term 1
:   Definition 1
:   Definition 2

Term 2
:   Definition 3
:   Definition 4

With multiple lines per definition:

Term 1
:   Definition 1 line 1 ...
Definition 1 line 2
:   Definition 2 line 1 ...
Definition 2 line 2

Term 2
:   Definition 3 line 2 ...
    Definition 3 line 2
:   Definition 4 line 2 ...
    Definition 4 line 2

With paragraphs:

Term 1

:   Definition 1 (paragraph)

Term 2

:   Definition 2 (paragraph)

With multiple paragraphs:

Term 1

:   Definition 1 paragraph 1 line 1 ...
	Definition 1 paragraph 1 line 2

    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)

    Definition 1 paragraph 2 line 1 ...
Definition 1 paragraph 2 line 2 (lazy)

* * *

A mix:

Term 1
Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)
    
    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

:   Definition 2 paragraph 1 line 1 ...
Definition 2 paragraph 1 line 2 (lazy)

Term 3
:   Definition 3 (no paragraph)
:   Definition 4 (no paragraph)
:   Definition 5 line 1 ...
    Definition 5 line 2 (no paragraph)

:   Definition 6 paragraph 1 line 1 ...
Definition 6 paragraph 1 line 2
:   Definition 7 (no paragraph)
:   Definition 8 paragraph 1 line 1 (forced paragraph) ...
    Definition 8 paragraph 1 line 2
    
    Definition 8 paragraph 2 line 1
    
Term 4
:   Definition 9 paragraph 1 line 1 (forced paragraph) ...
    Definition 9 paragraph 1 line 2
    
    Definition 9 paragraph 2 line 1
:   Definition 10 (no paragraph)

* * *

Special cases:

Term

:       code block
        as first element of a definition<michel.fortin@michelf.ca>

International domain names: <help@tūdaliņ.lv>


## Some weird valid email addresses

<abc.123@example.com>

<1234567890@example.com>

<_______@example.com>

<abc+mailbox/department=shipping@example.com>

<!#$%&'*+-/=?^_.{|}@example.com> (all of these characters are allowed)

<"abc@def"@example.com> (anything goes inside quotation marks)

<"Fred Bloggs"@example.com>

<jsmith@[192.0.2.1]>

<"A"@example.com>Combined emphasis:

1.  ***test test***
2.  ___test test___
3.  *test **test***
4.  **test *test***
5.  ***test* test**
6.  ***test** test*
7.  ***test* test**
8.  **test *test***
9.  *test **test***
10. _test __test___
11. __test _test___
12. ___test_ test__
13. ___test__ test_
14. ___test_ test__
15. __test _test___
16. _test __test___
17. *test __test__*
18. **test _test_**
19. **_test_ test**
20. *__test__ test*
21. **_test_ test**
22. **test _test_**
23. *test __test__*
24. _test **test**_
25. __test *test*__
26. __*test* test__
27. _**test** test_
28. __*test* test__
29. __test *test*__
30. _test **test**_


Incorrect nesting:

1.  *test  **test*  test**
2.  _test  __test_  test__
3.  **test  *test** test*
4.  __test  _test__ test_
5.  *test   *test*  test*
6.  _test   _test_  test_
7.  **test **test** test**
8.  __test __test__ test__
9. _**some text_**
10. *__some text*__
11. **_some text**_
12. *__some text*__

No emphasis:

1.  test*  test  *test
2.  test** test **test
3.  test_  test  _test
4.  test__ test __test



Middle-word emphasis (asterisks):

1.  *a*b
2.   a*b*
3.   a*b*c
4. **a**b
5.   a**b**
6.   a**b**c


Middle-word emphasis (underscore):

1.  _a_b
2.   a_b_
3.   a_b_c
4. __a__b
5.   a__b__
6.   a__b__c

my_precious_file.txt


## Tricky Cases

E**. **Test** TestTestTest

E**. **Test** Test Test Test


## Overlong emphasis

Name: ____________  
Organization: ____  
Region/Country: __

_____Cut here_____

____Cut here____

# Regression

_**Note**_: This _is emphasis_.
With asterisks

 * List item
 *
 * List item

With numbers

1. List item
2.
3. List item

With hyphens

- List item
-
- List item

With asterisks

 * List item
 * List item
 *

With numbers

1. List item
2. List item
3.

With hyphens

- List item
- List item
-
This is the first paragraph.[^first]

[^first]:  This is the first note.

* List item one.[^second]
* List item two.[^third]

[^third]: This is the third note, defined out of order.
[^second]: This is the second note.
[^fourth]: This is the fourth note.

# Header[^fourth]

Some paragraph with a footnote[^1], and another[^2].

[^1]: Content for fifth footnote.
[^2]: Content for sixth footnote spaning on 
    three lines, with some span-level markup like
    _emphasis_, a [link][].

[link]: http://michelf.ca/

Another paragraph with a named footnote[^fn-name].

[^fn-name]:
    Footnote beginning on the line next to the marker.

This paragraph should not have a footnote marker since 
the footnote is undefined.[^3]

This paragraph has a second footnote marker to footnote number one.[^1]

This paragraph links to a footnote with plenty of 
block-level content.[^block]

[^block]:
	Paragraph.
	
	*   List item
	
	> Blockquote
	
	    Code block

This paragraph host the footnote reference within a 
footnote test[^reference].

[^reference]:
	This footnote has a footnote of its own.[^nested]

[^nested]:
	This footnote should appear even though it is referenced
	from another footnote. But [^reference] should be litteral
	since the footnote with that name has already been used.

 - - -

Testing unusual footnote name[^1$^!"'].

[^1$^!"']: Haha!

 - - -
 
Footnotes mixed with images[^image-mixed]
![1800 Travel][img6]
![1830 Travel][img7]

[img6]: images/MGR-1800-travel.jpeg "Travel Speeds in 1800"
[^image-mixed]: Footnote Content
[img7]: images/MGR-1830-travel.jpeg "Travel Speeds in 1830"
In Markdown 1.0.0 and earlier. Version
8. This line turns into a list item.
Because a hard-wrapped line in the
middle of a paragraph looked like a
list item.

Here's one with a bullet.
* criminey.
Header  {#id1}
======

Header  { #id2}
------

### Header  {#id3 }
#### Header ##  { #id4 }

 - - -

Header  {.cl}
======

Header  { .cl}
------

### Header  {.cl }
#### Header ##  { .cl }

 - - -

Header  {.cl.class}
======

Header  { .cl .class}
------

### Header  {.cl .class }
#### Header ##  { .cl.class }

 - - -

Header  {#id5.cl.class}
======

Header  { #id6 .cl .class}
------

### Header  {.cl.class#id7 }
#### Header ##  { .cl.class#id8 }
Header
======

Header
------

### Header

 - - -

Header
======
Paragraph

Header
------
Paragraph

### Header
Paragraph

 - - -

Paragraph
Header
======
Paragraph

Paragraph
Header
------
Paragraph

Paragraph
### Header
ParagraphDashes:

---

 ---
 
  ---

   ---

	---

- - -

 - - -
 
  - - -

   - - -

	- - -


Asterisks:

***

 ***
 
  ***

   ***

	***

* * *

 * * *
 
  * * *

   * * *

	* * *


Underscores:

___

 ___
 
  ___

   ___

    ___

_ _ _

 _ _ _
 
  _ _ _

   _ _ _

    _ _ _
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")

Inline within a paragraph: [alt text](/url/).

![alt text](/url/  "title preceded by two spaces")

![alt text](/url/  "title has spaces afterward"  )

![alt text](</url/>)

![alt text](</url/> "with a title").

![Empty]()

![this is a stupid URL](http://example.com/(parens).jpg)


![alt text][foo]

  [foo]: /url/

![alt text][bar]

  [bar]: /url/ "Title here"Simple block on one line:

<div>foo</div>

And nested without indentation:

<div>
<div>
<div>
foo
</div>
<div style=">"/>
</div>
<div>bar</div>
</div>

And with attributes:

<div>
	<div id="foo">
	</div>
</div>

This was broken in 1.0.2b7:

<div class="inlinepage">
<div class="toggleableend">
foo
</div>
</div>
Here's a simple block:

<div>
	foo
</div>

This should be a code block, though:

	<div>
		foo
	</div>

As should this:

	<div>foo</div>

Now, nested:

<div>
	<div>
		<div>
			foo
		</div>
	</div>
</div>

This should just be an HTML comment:

<!-- Comment -->

Multiline:

<!--
Blah
Blah
-->

Code block:

	<!-- Comment -->

Just plain comment, with trailing spaces on the line:

<!-- foo -->   

Code:

	<hr />
	
Hr's:

<hr>

<hr/>

<hr />

<hr>   

<hr/>  

<hr /> 

<hr class="foo" id="bar" />

<hr class="foo" id="bar"/>

<hr class="foo" id="bar" >

<abbr title=" **Attribute Content Is Not A Code Span** ">ACINACS</abbr>

<abbr title="first backtick!">SB</abbr> 
<abbr title="second backtick!">SB</abbr>Paragraph one.

<!-- This is a simple comment -->

<!--
	This is another comment.
-->

Paragraph two.

<!-- one comment block -- -- with two comments -->

The end.
# Markdown inside code blocks

<div markdown="1">
foo
</div>

<div markdown='1'>
foo
</div>

<div markdown=1>
foo
</div>

<table>
<tr><td markdown="1">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="span">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="block">test _emphasis_ (block)</td></tr>
</table>

## More complicated

<table>
<tr><td markdown="1">
* this is _not_ a list item</td></tr>
<tr><td markdown="span">
* this is _not_ a list item</td></tr>
<tr><td markdown="block">
* this _is_ a list item
</td></tr>
</table>

## With indent

<div>
    <div markdown="1">
    This text is no code block: if it was, the 
    closing <div> would be too and the HTML block 
    would be invalid.

    Markdown content in HTML blocks is assumed to be 
    indented the same as the block opening tag.

    **This should be the third paragraph after the header.**
    </div>
</div>

## Code block with rogue </div>s in Markdown code span and block

<div>
    <div markdown="1">

    This is a code block however:

        </div>

    Funny isn't it? Here is a code span: </div>.

    </div>
</div>

<div>
  <div markdown="1">
    * List item, not a code block

Some text

      This is a code block.
  </div>
</div>

## No code block in markdown span mode

<p markdown="1">
    This is not a code block since Markdown parse paragraph 
    content as span. Code spans like </p> are allowed though.
</p>

<p markdown="1">_Hello_ _world_</p>

## Preserving attributes and tags on more than one line:

<p class="test" markdown="1" 
id="12">
Some _span_ content.
</p>


## Header confusion bug

<table class="canvas">
<tr>
<td id="main" markdown="1">Hello World!
============

Hello World!</td>
</tr>
</table>
Here is a block tag ins:

<ins>
<p>Some text</p>
</ins>

<ins>And here it is inside a paragraph.</ins>

And here it is <ins>in the middle of</ins> a paragraph.

<del>
<p>Some text</p>
</del>

<del>And here is ins as a paragraph.</del>

And here it is <del>in the middle of</del> a paragraph.
		    GNU GENERAL PUBLIC LICENSE
		       Version 2, June 1991

 Copyright (C) 1989, 1991 Free Software Foundation, Inc.,
 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

			    Preamble

  The licenses for most software are designed to take away your
freedom to share and change it.  By contrast, the GNU General Public
License is intended to guarantee your freedom to share and change free
software--to make sure the software is free for all its users.  This
General Public License applies to most of the Free Software
Foundation's software and to any other program whose authors commit to
using it.  (Some other Free Software Foundation software is covered by
the GNU Lesser General Public License instead.)  You can apply it to
your programs, too.

  When we speak of free software, we are referring to freedom, not
price.  Our General Public Licenses are designed to make sure that you
have the freedom to distribute copies of free software (and charge for
this service if you wish), that you receive source code or can get it
if you want it, that you can change the software or use pieces of it
in new free programs; and that you know you can do these things.

  To protect your rights, we need to make restrictions that forbid
anyone to deny you these rights or to ask you to surrender the rights.
These restrictions translate to certain responsibilities for you if you
distribute copies of the software, or if you modify it.

  For example, if you distribute copies of such a program, whether
gratis or for a fee, you must give the recipients all the rights that
you have.  You must make sure that they, too, receive or can get the
source code.  And you must show them these terms so they know their
rights.

  We protect your rights with two steps: (1) copyright the software, and
(2) offer you this license which gives you legal permission to copy,
distribute and/or modify the software.

  Also, for each author's protection and ours, we want to make certain
that everyone understands that there is no warranty for this free
software.  If the software is modified by someone else and passed on, we
want its recipients to know that what they have is not the original, so
that any problems introduced by others will not reflect on the original
authors' reputations.

  Finally, any free program is threatened constantly by software
patents.  We wish to avoid the danger that redistributors of a free
program will individually obtain patent licenses, in effect making the
program proprietary.  To prevent this, we have made it clear that any
patent must be licensed for everyone's free use or not licensed at all.

  The precise terms and conditions for copying, distribution and
modification follow.

		    GNU GENERAL PUBLIC LICENSE
   TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

  0. This License applies to any program or other work which contains
a notice placed by the copyright holder saying it may be distributed
under the terms of this General Public License.  The "Program", below,
refers to any such program or work, and a "work based on the Program"
means either the Program or any derivative work under copyright law:
that is to say, a work containing the Program or a portion of it,
either verbatim or with modifications and/or translated into another
language.  (Hereinafter, translation is included without limitation in
the term "modification".)  Each licensee is addressed as "you".

Activities other than copying, distribution and modification are not
covered by this License; they are outside its scope.  The act of
running the Program is not restricted, and the output from the Program
is covered only if its contents constitute a work based on the
Program (independent of having been made by running the Program).
Whether that is true depends on what the Program does.

  1. You may copy and distribute verbatim copies of the Program's
source code as you receive it, in any medium, provided that you
conspicuously and appropriately publish on each copy an appropriate
copyright notice and disclaimer of warranty; keep intact all the
notices that refer to this License and to the absence of any warranty;
and give any other recipients of the Program a copy of this License
along with the Program.

You may charge a fee for the physical act of transferring a copy, and
you may at your option offer warranty protection in exchange for a fee.

  2. You may modify your copy or copies of the Program or any portion
of it, thus forming a work based on the Program, and copy and
distribute such modifications or work under the terms of Section 1
above, provided that you also meet all of these conditions:

    a) You must cause the modified files to carry prominent notices
    stating that you changed the files and the date of any change.

    b) You must cause any work that you distribute or publish, that in
    whole or in part contains or is derived from the Program or any
    part thereof, to be licensed as a whole at no charge to all third
    parties under the terms of this License.

    c) If the modified program normally reads commands interactively
    when run, you must cause it, when started running for such
    interactive use in the most ordinary way, to print or display an
    announcement including an appropriate copyright notice and a
    notice that there is no warranty (or else, saying that you provide
    a warranty) and that users may redistribute the program under
    these conditions, and telling the user how to view a copy of this
    License.  (Exception: if the Program itself is interactive but
    does not normally print such an announcement, your work based on
    the Program is not required to print an announcement.)

These requirements apply to the modified work as a whole.  If
identifiable sections of that work are not derived from the Program,
and can be reasonably considered independent and separate works in
themselves, then this License, and its terms, do not apply to those
sections when you distribute them as separate works.  But when you
distribute the same sections as part of a whole which is a work based
on the Program, the distribution of the whole must be on the terms of
this License, whose permissions for other licensees extend to the
entire whole, and thus to each and every part regardless of who wrote it.

Thus, it is not the intent of this section to claim rights or contest
your rights to work written entirely by you; rather, the intent is to
exercise the right to control the distribution of derivative or
collective works based on the Program.

In addition, mere aggregation of another work not based on the Program
with the Program (or with a work based on the Program) on a volume of
a storage or distribution medium does not bring the other work under
the scope of this License.

  3. You may copy and distribute the Program (or a work based on it,
under Section 2) in object code or executable form under the terms of
Sections 1 and 2 above provided that you also do one of the following:

    a) Accompany it with the complete corresponding machine-readable
    source code, which must be distributed under the terms of Sections
    1 and 2 above on a medium customarily used for software interchange; or,

    b) Accompany it with a written offer, valid for at least three
    years, to give any third party, for a charge no more than your
    cost of physically performing source distribution, a complete
    machine-readable copy of the corresponding source code, to be
    distributed under the terms of Sections 1 and 2 above on a medium
    customarily used for software interchange; or,

    c) Accompany it with the information you received as to the offer
    to distribute corresponding source code.  (This alternative is
    allowed only for noncommercial distribution and only if you
    received the program in object code or executable form with such
    an offer, in accord with Subsection b above.)

The source code for a work means the preferred form of the work for
making modifications to it.  For an executable work, complete source
code means all the source code for all modules it contains, plus any
associated interface definition files, plus the scripts used to
control compilation and installation of the executable.  However, as a
special exception, the source code distributed need not include
anything that is normally distributed (in either source or binary
form) with the major components (compiler, kernel, and so on) of the
operating system on which the executable runs, unless that component
itself accompanies the executable.

If distribution of executable or object code is made by offering
access to copy from a designated place, then offering equivalent
access to copy the source code from the same place counts as
distribution of the source code, even though third parties are not
compelled to copy the source along with the object code.

  4. You may not copy, modify, sublicense, or distribute the Program
except as expressly provided under this License.  Any attempt
otherwise to copy, modify, sublicense or distribute the Program is
void, and will automatically terminate your rights under this License.
However, parties who have received copies, or rights, from you under
this License will not have their licenses terminated so long as such
parties remain in full compliance.

  5. You are not required to accept this License, since you have not
signed it.  However, nothing else grants you permission to modify or
distribute the Program or its derivative works.  These actions are
prohibited by law if you do not accept this License.  Therefore, by
modifying or distributing the Program (or any work based on the
Program), you indicate your acceptance of this License to do so, and
all its terms and conditions for copying, distributing or modifying
the Program or works based on it.

  6. Each time you redistribute the Program (or any work based on the
Program), the recipient automatically receives a license from the
original licensor to copy, distribute or modify the Program subject to
these terms and conditions.  You may not impose any further
restrictions on the recipients' exercise of the rights granted herein.
You are not responsible for enforcing compliance by third parties to
this License.

  7. If, as a consequence of a court judgment or allegation of patent
infringement or for any other reason (not limited to patent issues),
conditions are imposed on you (whether by court order, agreement or
otherwise) that contradict the conditions of this License, they do not
excuse you from the conditions of this License.  If you cannot
distribute so as to satisfy simultaneously your obligations under this
License and any other pertinent obligations, then as a consequence you
may not distribute the Program at all.  For example, if a patent
license would not permit royalty-free redistribution of the Program by
all those who receive copies directly or indirectly through you, then
the only way you could satisfy both it and this License would be to
refrain entirely from distribution of the Program.

If any portion of this section is held invalid or unenforceable under
any particular circumstance, the balance of the section is intended to
apply and the section as a whole is intended to apply in other
circumstances.

It is not the purpose of this section to induce you to infringe any
patents or other property right claims or to contest validity of any
such claims; this section has the sole purpose of protecting the
integrity of the free software distribution system, which is
implemented by public license practices.  Many people have made
generous contributions to the wide range of software distributed
through that system in reliance on consistent application of that
system; it is up to the author/donor to decide if he or she is willing
to distribute software through any other system and a licensee cannot
impose that choice.

This section is intended to make thoroughly clear what is believed to
be a consequence of the rest of this License.

  8. If the distribution and/or use of the Program is restricted in
certain countries either by patents or by copyrighted interfaces, the
original copyright holder who places the Program under this License
may add an explicit geographical distribution limitation excluding
those countries, so that distribution is permitted only in or among
countries not thus excluded.  In such case, this License incorporates
the limitation as if written in the body of this License.

  9. The Free Software Foundation may publish revised and/or new versions
of the General Public License from time to time.  Such new versions will
be similar in spirit to the present version, but may differ in detail to
address new problems or concerns.

Each version is given a distinguishing version number.  If the Program
specifies a version number of this License which applies to it and "any
later version", you have the option of following the terms and conditions
either of that version or of any later version published by the Free
Software Foundation.  If the Program does not specify a version number of
this License, you may choose any version ever published by the Free Software
Foundation.

  10. If you wish to incorporate parts of the Program into other free
programs whose distribution conditions are different, write to the author
to ask for permission.  For software which is copyrighted by the Free
Software Foundation, write to the Free Software Foundation; we sometimes
make exceptions for this.  Our decision will be guided by the two goals
of preserving the free status of all derivatives of our free software and
of promoting the sharing and reuse of software generally.

			    NO WARRANTY

  11. BECAUSE THE PROGRAM IS LICENSED FREE OF CHARGE, THERE IS NO WARRANTY
FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW.  EXCEPT WHEN
OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES
PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED
OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.  THE ENTIRE RISK AS
TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU.  SHOULD THE
PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING,
REPAIR OR CORRECTION.

  12. IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING
WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MAY MODIFY AND/OR
REDISTRIBUTE THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES,
INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING
OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED
TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY
YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER
PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES.

		     END OF TERMS AND CONDITIONS

	    How to Apply These Terms to Your New Programs

  If you develop a new program, and you want it to be of the greatest
possible use to the public, the best way to achieve this is to make it
free software which everyone can redistribute and change under these terms.

  To do so, attach the following notices to the program.  It is safest
to attach them to the start of each source file to most effectively
convey the exclusion of warranty; and each file should have at least
the "copyright" line and a pointer to where the full notice is found.

    <one line to give the program's name and a brief idea of what it does.>
    Copyright (C) <year>  <name of author>

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

Also add information on how to contact you by electronic and paper mail.

If the program is interactive, make it output a short notice like this
when it starts in an interactive mode:

    Gnomovision version 69, Copyright (C) year name of author
    Gnomovision comes with ABSOLUTELY NO WARRANTY; for details type show w'.
    This is free software, and you are welcome to redistribute it
    under certain conditions; type show c' for details.

The hypothetical commands show w' and show c' should show the appropriate
parts of the General Public License.  Of course, the commands you use may
be called something other than show w' and show c'; they could even be
mouse-clicks or menu items--whatever suits your program.

You should also get your employer (if you work as a programmer) or your
school, if any, to sign a "copyright disclaimer" for the program, if
necessary.  Here is a sample; alter the names:

  Yoyodyne, Inc., hereby disclaims all copyright interest in the program
  Gnomovision' (which makes passes at compilers) written by James Hacker.

  <signature of Ty Coon>, 1 April 1989
  Ty Coon, President of Vice

This General Public License does not permit incorporating your program into
proprietary programs.  If your program is a subroutine library, you may
consider it more useful to permit linking proprietary applications with the
library.  If this is what you want to do, use the GNU Lesser General
Public License instead of this License.
This is an [inline link](/url "title"){.class #inline-link}.

This is a [reference link][refid].

This is an ![inline image](/img "title"){.class #inline-img}.

This is a ![reference image][refid].

[refid]: /path/to/something (Title) { .class #ref data-key=val }

Just a [URL](/url/).

[URL and title](/url/ "title").

[URL and title](/url/  "title preceded by two spaces").

[URL and title](/url/	"title preceded by a tab").

[URL and title](/url/ "title has spaces afterward"  ).

[URL wrapped in angle brackets](</url/>).

[URL w/ angle brackets + title](</url/> "Here's the title").

[Empty]().

[With parens in the URL](http://en.wikipedia.org/wiki/WIMP_(computing))

(With outer parens and [parens in url](/foo(bar)))


[With parens in the URL](/foo(bar) "and a title")

(With outer parens and [parens in url](/foo(bar) "and a title"))
Foo [bar] [1].

Foo [bar][1].

Foo [bar]
[1].

[1]: /url/  "Title"


With [embedded [brackets]] [b].


Indented [once][].

Indented [twice][].

Indented [thrice][].

Indented [four][] times.

 [once]: /url

  [twice]: /url

   [thrice]: /url

    [four]: /url


[b]: /url/

* * *

[this] [this] should work

So should [this][this].

And [this] [].

And [this][].

And [this].

But not [that] [].

Nor [that][].

Nor [that].

[Something in brackets like [this][] should work]

[Same with [this].]

In this case, [this](/somethingelse/) points to something else.

Backslashing should suppress \[this] and [this\].

[this]: foo


* * *

Here's one where the [link
breaks] across lines.

Here's another where the [link 
breaks] across lines, but with a line-ending space.


[link breaks]: /url/
This is the [simple case].

[simple case]: /simple



This one has a [line
break].

This one has a [line 
break] with a line-ending space.

[line break]: /foo


[this] [that] and the [other]

[this]: /this
[that]: /that
[other]: /other
Foo [bar][].

Foo [bar](/url/ "Title with "quotes" inside").


  [bar]: /url/ "Title with "quotes" inside"

Markdown: Basics
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a class="selected" title="Markdown Basics">Basics</a></li>
    <li><a href="/projects/markdown/syntax" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


Getting the Gist of Markdown's Formatting Syntax
------------------------------------------------

This page offers a brief overview of what it's like to use Markdown.
The [syntax page] [s] provides complete, detailed documentation for
every feature, but Markdown should be very easy to pick up simply by
looking at a few examples of it in action. The examples on this page
are written in a before/after style, showing example syntax and the
HTML output produced by Markdown.

It's also helpful to simply try Markdown out; the [Dingus] [d] is a
web application that allows you type your own Markdown-formatted text
and translate it to XHTML.

**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL] [src].

  [s]: /projects/markdown/syntax  "Markdown Syntax"
  [d]: /projects/markdown/dingus  "Markdown Dingus"
  [src]: /projects/markdown/basics.text


## Paragraphs, Headers, Blockquotes ##

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

Markdown offers two styles of headers: *Setext* and *atx*.
Setext-style headers for <h1> and <h2> are created by
"underlining" with equal signs (=) and hyphens (-), respectively.
To create an atx-style header, you put 1-6 hash marks (#) at the
beginning of the line -- the number of hashes equals the resulting
HTML header level.

Blockquotes are indicated using email-style '>' angle brackets.

Markdown:

    A First Level Header
    ====================
    
    A Second Level Header
    ---------------------

    Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.

    The quick brown fox jumped over the lazy
    dog's back.
    
    ### Header 3

    > This is a blockquote.
    > 
    > This is the second paragraph in the blockquote.
    >
    > ## This is an H2 in a blockquote


Output:

    <h1>A First Level Header</h1>
    
    <h2>A Second Level Header</h2>
    
    <p>Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.</p>
    
    <p>The quick brown fox jumped over the lazy
    dog's back.</p>
    
    <h3>Header 3</h3>
    
    <blockquote>
        <p>This is a blockquote.</p>
        
        <p>This is the second paragraph in the blockquote.</p>
        
        <h2>This is an H2 in a blockquote</h2>
    </blockquote>



### Phrase Emphasis ###

Markdown uses asterisks and underscores to indicate spans of emphasis.

Markdown:

    Some of these words *are emphasized*.
    Some of these words _are emphasized also_.
    
    Use two asterisks for **strong emphasis**.
    Or, if you prefer, __use two underscores instead__.

Output:

    <p>Some of these words <em>are emphasized</em>.
    Some of these words <em>are emphasized also</em>.</p>
    
    <p>Use two asterisks for <strong>strong emphasis</strong>.
    Or, if you prefer, <strong>use two underscores instead</strong>.</p>
   


## Lists ##

Unordered (bulleted) lists use asterisks, pluses, and hyphens (*,
+, and -) as list markers. These three markers are
interchangable; this:

    *   Candy.
    *   Gum.
    *   Booze.

this:

    +   Candy.
    +   Gum.
    +   Booze.

and this:

    -   Candy.
    -   Gum.
    -   Booze.

all produce the same output:

    <ul>
    <li>Candy.</li>
    <li>Gum.</li>
    <li>Booze.</li>
    </ul>

Ordered (numbered) lists use regular numbers, followed by periods, as
list markers:

    1.  Red
    2.  Green
    3.  Blue

Output:

    <ol>
    <li>Red</li>
    <li>Green</li>
    <li>Blue</li>
    </ol>

If you put blank lines between items, you'll get <p> tags for the
list item text. You can create multi-paragraph list items by indenting
the paragraphs by 4 spaces or 1 tab:

    *   A list item.
    
        With multiple paragraphs.

    *   Another item in the list.

Output:

    <ul>
    <li><p>A list item.</p>
    <p>With multiple paragraphs.</p></li>
    <li><p>Another item in the list.</p></li>
    </ul>
    


### Links ###

Markdown supports two styles for creating links: *inline* and
*reference*. With both styles, you use square brackets to delimit the
text you want to turn into a link.

Inline-style links use parentheses immediately after the link text.
For example:

    This is an [example link](http://example.com/).

Output:

    <p>This is an <a href="http://example.com/">
    example link</a>.</p>

Optionally, you may include a title attribute in the parentheses:

    This is an [example link](http://example.com/ "With a Title").

Output:

    <p>This is an <a href="http://example.com/" title="With a Title">
    example link</a>.</p>

Reference-style links allow you to refer to your links by names, which
you define elsewhere in your document:

    I get 10 times more traffic from [Google][1] than from
    [Yahoo][2] or [MSN][3].

    [1]: http://google.com/        "Google"
    [2]: http://search.yahoo.com/  "Yahoo Search"
    [3]: http://search.msn.com/    "MSN Search"

Output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from <a href="http://search.yahoo.com/"
    title="Yahoo Search">Yahoo</a> or <a href="http://search.msn.com/"
    title="MSN Search">MSN</a>.</p>

The title attribute is optional. Link names may contain letters,
numbers and spaces, but are *not* case sensitive:

    I start my morning with a cup of coffee and
    [The New York Times][NY Times].

    [ny times]: http://www.nytimes.com/

Output:

    <p>I start my morning with a cup of coffee and
    <a href="http://www.nytimes.com/">The New York Times</a>.</p>


### Images ###

Image syntax is very much like link syntax.

Inline (titles are optional):

    ![alt text](/path/to/img.jpg "Title")

Reference-style:

    ![alt text][id]

    [id]: /path/to/img.jpg "Title"

Both of the above examples produce the same output:

    <img src="/path/to/img.jpg" alt="alt text" title="Title" />



### Code ###

In a regular paragraph, you can create code span by wrapping text in
backtick quotes. Any ampersands (&) and angle brackets (< or
>) will automatically be translated into HTML entities. This makes
it easy to use Markdown to write about HTML example code:

    I strongly recommend against using any <blink> tags.

    I wish SmartyPants used named entities like &mdash;
    instead of decimal-encoded entites like &#8212;.

Output:

    <p>I strongly recommend against using any
    <code>&lt;blink&gt;</code> tags.</p>
    
    <p>I wish SmartyPants used named entities like
    <code>&amp;mdash;</code> instead of decimal-encoded
    entites like <code>&amp;#8212;</code>.</p>


To specify an entire block of pre-formatted code, indent every line of
the block by 4 spaces or 1 tab. Just like with code spans, &, <,
and > characters will be escaped automatically.

Markdown:

    If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:

        <blockquote>
            <p>For example.</p>
        </blockquote>

Output:

    <p>If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:</p>
    
    <pre><code>&lt;blockquote&gt;
        &lt;p&gt;For example.&lt;/p&gt;
    &lt;/blockquote&gt;
    </code></pre>
Markdown: Syntax
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a href="/projects/markdown/basics" title="Markdown Basics">Basics</a></li>
    <li><a class="selected" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


*   [Overview](#overview)
    *   [Philosophy](#philosophy)
    *   [Inline HTML](#html)
    *   [Automatic Escaping for Special Characters](#autoescape)
*   [Block Elements](#block)
    *   [Paragraphs and Line Breaks](#p)
    *   [Headers](#header)
    *   [Blockquotes](#blockquote)
    *   [Lists](#list)
    *   [Code Blocks](#precode)
    *   [Horizontal Rules](#hr)
*   [Span Elements](#span)
    *   [Links](#link)
    *   [Emphasis](#em)
    *   [Code](#code)
    *   [Images](#img)
*   [Miscellaneous](#misc)
    *   [Backslash Escapes](#backslash)
    *   [Automatic Links](#autolink)


**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL][src].

  [src]: /projects/markdown/syntax.text

* * *

<h2 id="overview">Overview</h2>

<h3 id="philosophy">Philosophy</h3>

Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

Readability, however, is emphasized above all else. A Markdown-formatted
document should be publishable as-is, as plain text, without looking
like it's been marked up with tags or formatting instructions. While
Markdown's syntax has been influenced by several existing text-to-HTML
filters -- including [Setext] [1], [atx] [2], [Textile] [3], [reStructuredText] [4],
[Grutatext] [5], and [EtText] [6] -- the single biggest source of
inspiration for Markdown's syntax is the format of plain text email.

  [1]: http://docutils.sourceforge.net/mirror/setext.html
  [2]: http://www.aaronsw.com/2002/atx/
  [3]: http://textism.com/tools/textile/
  [4]: http://docutils.sourceforge.net/rst.html
  [5]: http://www.triptico.com/software/grutatxt.html
  [6]: http://ettext.taint.org/doc/

To this end, Markdown's syntax is comprised entirely of punctuation
characters, which punctuation characters have been carefully chosen so
as to look like what they mean. E.g., asterisks around a word actually
look like \*emphasis\*. Markdown lists look like, well, lists. Even
blockquotes look like quoted passages of text, assuming you've ever
used email.



<h3 id="html">Inline HTML</h3>

Markdown's syntax is intended for one purpose: to be used as a
format for *writing* for the web.

Markdown is not a replacement for HTML, or even close to it. Its
syntax is very small, corresponding only to a very small subset of
HTML tags. The idea is *not* to create a syntax that makes it easier
to insert HTML tags. In my opinion, HTML tags are already easy to
insert. The idea for Markdown is to make it easy to read, write, and
edit prose. HTML is a *publishing* format; Markdown is a *writing*
format. Thus, Markdown's formatting syntax only addresses issues that
can be conveyed in plain text.

For any markup that is not covered by Markdown's syntax, you simply
use HTML itself. There's no need to preface it or delimit it to
indicate that you're switching from Markdown to HTML; you just use
the tags.

The only restrictions are that block-level HTML elements -- e.g. <div>,
<table>, <pre>, <p>, etc. -- must be separated from surrounding
content by blank lines, and the start and end tags of the block should
not be indented with tabs or spaces. Markdown is smart enough not
to add extra (unwanted) <p> tags around HTML block-level tags.

For example, to add an HTML table to a Markdown article:

    This is a regular paragraph.

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    This is another regular paragraph.

Note that Markdown formatting syntax is not processed within block-level
HTML tags. E.g., you can't use Markdown-style *emphasis* inside an
HTML block.

Span-level HTML tags -- e.g. <span>, <cite>, or <del> -- can be
used anywhere in a Markdown paragraph, list item, or header. If you
want, you can even use HTML tags instead of Markdown formatting; e.g. if
you'd prefer to use HTML <a> or <img> tags instead of Markdown's
link or image syntax, go right ahead.

Unlike block-level HTML tags, Markdown syntax *is* processed within
span-level tags.


<h3 id="autoescape">Automatic Escaping for Special Characters</h3>

In HTML, there are two characters that demand special treatment: <
and &. Left angle brackets are used to start tags; ampersands are
used to denote HTML entities. If you want to use them as literal
characters, you must escape them as entities, e.g. &lt;, and
&amp;.

Ampersands in particular are bedeviling for web writers. If you want to
write about 'AT&T', you need to write 'AT&amp;T'. You even need to
escape ampersands within URLs. Thus, if you want to link to:

    http://images.google.com/images?num=30&q=larry+bird

you need to encode the URL as:

    http://images.google.com/images?num=30&amp;q=larry+bird

in your anchor tag href attribute. Needless to say, this is easy to
forget, and is probably the single most common source of HTML validation
errors in otherwise well-marked-up web sites.

Markdown allows you to use these characters naturally, taking care of
all the necessary escaping for you. If you use an ampersand as part of
an HTML entity, it remains unchanged; otherwise it will be translated
into &amp;.

So, if you want to include a copyright symbol in your article, you can write:

    &copy;

and Markdown will leave it alone. But if you write:

    AT&T

Markdown will translate it to:

    AT&amp;T

Similarly, because Markdown supports [inline HTML](#html), if you use
angle brackets as delimiters for HTML tags, Markdown will treat them as
such. But if you write:

    4 < 5

Markdown will translate it to:

    4 &lt; 5

However, inside Markdown code spans and blocks, angle brackets and
ampersands are *always* encoded automatically. This makes it easy to use
Markdown to write about HTML code. (As opposed to raw HTML, which is a
terrible format for writing about HTML syntax, because every single <
and & in your example code needs to be escaped.)


* * *


<h2 id="block">Block Elements</h2>


<h3 id="p">Paragraphs and Line Breaks</h3>

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing but spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

The implication of the "one or more consecutive lines of text" rule is
that Markdown supports "hard-wrapped" text paragraphs. This differs
significantly from most other text-to-HTML formatters (including Movable
Type's "Convert Line Breaks" option) which translate every line break
character in a paragraph into a <br /> tag.

When you *do* want to insert a <br /> break tag using Markdown, you
end a line with two or more spaces, then type return.

Yes, this takes a tad more effort to create a <br />, but a simplistic
"every line break is a <br />" rule wouldn't work for Markdown.
Markdown's email-style [blockquoting][bq] and multi-paragraph [list items][l]
work best -- and look better -- when you format them with hard breaks.

  [bq]: #blockquote
  [l]:  #list



<h3 id="header">Headers</h3>

Markdown supports two styles of headers, [Setext] [1] and [atx] [2].

Setext-style headers are "underlined" using equal signs (for first-level
headers) and dashes (for second-level headers). For example:

    This is an H1
    =============

    This is an H2
    -------------

Any number of underlining ='s or -'s will work.

Atx-style headers use 1-6 hash characters at the start of the line,
corresponding to header levels 1-6. For example:

    # This is an H1

    ## This is an H2

    ###### This is an H6

Optionally, you may "close" atx-style headers. This is purely
cosmetic -- you can use this if you think it looks better. The
closing hashes don't even need to match the number of hashes
used to open the header. (The number of opening hashes
determines the header level.) :

    # This is an H1 #

    ## This is an H2 ##

    ### This is an H3 ######


<h3 id="blockquote">Blockquotes</h3>

Markdown uses email-style > characters for blockquoting. If you're
familiar with quoting passages of text in an email message, then you
know how to create a blockquote in Markdown. It looks best if you hard
wrap the text and put a > before every line:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    > 
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

Markdown allows you to be lazy and only put the > before the first
line of a hard-wrapped paragraph:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

Blockquotes can be nested (i.e. a blockquote-in-a-blockquote) by
adding additional levels of >:

    > This is the first level of quoting.
    >
    > > This is nested blockquote.
    >
    > Back to the first level.

Blockquotes can contain other Markdown elements, including headers, lists,
and code blocks:

	> ## This is a header.
	> 
	> 1.   This is the first list item.
	> 2.   This is the second list item.
	> 
	> Here's some example code:
	> 
	>     return shell_exec("echo $input | $markdown_script");

Any decent text editor should make email-style quoting easy. For
example, with BBEdit, you can make a selection and choose Increase
Quote Level from the Text menu.


<h3 id="list">Lists</h3>

Markdown supports ordered (numbered) and unordered (bulleted) lists.

Unordered lists use asterisks, pluses, and hyphens -- interchangably
-- as list markers:

    *   Red
    *   Green
    *   Blue

is equivalent to:

    +   Red
    +   Green
    +   Blue

and:

    -   Red
    -   Green
    -   Blue

Ordered lists use numbers followed by periods:

    1.  Bird
    2.  McHale
    3.  Parish

It's important to note that the actual numbers you use to mark the
list have no effect on the HTML output Markdown produces. The HTML
Markdown produces from the above list is:

    <ol>
    <li>Bird</li>
    <li>McHale</li>
    <li>Parish</li>
    </ol>

If you instead wrote the list in Markdown like this:

    1.  Bird
    1.  McHale
    1.  Parish

or even:

    3. Bird
    1. McHale
    8. Parish

you'd get the exact same HTML output. The point is, if you want to,
you can use ordinal numbers in your ordered Markdown lists, so that
the numbers in your source match the numbers in your published HTML.
But if you want to be lazy, you don't have to.

If you do use lazy list numbering, however, you should still start the
list with the number 1. At some point in the future, Markdown may support
starting ordered lists at an arbitrary number.

List markers typically start at the left margin, but may be indented by
up to three spaces. List markers must be followed by one or more spaces
or a tab.

To make lists look nice, you can wrap items with hanging indents:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
        Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
        viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
        Suspendisse id sem consectetuer libero luctus adipiscing.

But if you want to be lazy, you don't have to:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.

If list items are separated by blank lines, Markdown will wrap the
items in <p> tags in the HTML output. For example, this input:

    *   Bird
    *   Magic

will turn into:

    <ul>
    <li>Bird</li>
    <li>Magic</li>
    </ul>

But this:

    *   Bird

    *   Magic

will turn into:

    <ul>
    <li><p>Bird</p></li>
    <li><p>Magic</p></li>
    </ul>

List items may consist of multiple paragraphs. Each subsequent
paragraph in a list item must be intended by either 4 spaces
or one tab:

    1.  This is a list item with two paragraphs. Lorem ipsum dolor
        sit amet, consectetuer adipiscing elit. Aliquam hendrerit
        mi posuere lectus.

        Vestibulum enim wisi, viverra nec, fringilla in, laoreet
        vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
        sit amet velit.

    2.  Suspendisse id sem consectetuer libero luctus adipiscing.

It looks nice if you indent every line of the subsequent
paragraphs, but here again, Markdown will allow you to be
lazy:

    *   This is a list item with two paragraphs.

        This is the second paragraph in the list item. You're
    only required to indent the first line. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit.

    *   Another item in the same list.

To put a blockquote within a list item, the blockquote's >
delimiters need to be indented:

    *   A list item with a blockquote:

        > This is a blockquote
        > inside a list item.

To put a code block within a list item, the code block needs
to be indented *twice* -- 8 spaces or two tabs:

    *   A list item with a code block:

            <code goes here>


It's worth noting that it's possible to trigger an ordered list by
accident, by writing something like this:

    1986. What a great season.

In other words, a *number-period-space* sequence at the beginning of a
line. To avoid this, you can backslash-escape the period:

    1986\. What a great season.



<h3 id="precode">Code Blocks</h3>

Pre-formatted code blocks are used for writing about programming or
markup source code. Rather than forming normal paragraphs, the lines
of a code block are interpreted literally. Markdown wraps a code block
in both <pre> and <code> tags.

To produce a code block in Markdown, simply indent every line of the
block by at least 4 spaces or 1 tab. For example, given this input:

    This is a normal paragraph:

        This is a code block.

Markdown will generate:

    <p>This is a normal paragraph:</p>

    <pre><code>This is a code block.
    </code></pre>

One level of indentation -- 4 spaces or 1 tab -- is removed from each
line of the code block. For example, this:

    Here is an example of AppleScript:

        tell application "Foo"
            beep
        end tell

will turn into:

    <p>Here is an example of AppleScript:</p>

    <pre><code>tell application "Foo"
        beep
    end tell
    </code></pre>

A code block continues until it reaches a line that is not indented
(or the end of the article).

Within a code block, ampersands (&) and angle brackets (< and >)
are automatically converted into HTML entities. This makes it very
easy to include example HTML source code using Markdown -- just paste
it and indent it, and Markdown will handle the hassle of encoding the
ampersands and angle brackets. For example, this:

        <div class="footer">
            &copy; 2004 Foo Corporation
        </div>

will turn into:

    <pre><code>&lt;div class="footer"&gt;
        &amp;copy; 2004 Foo Corporation
    &lt;/div&gt;
    </code></pre>

Regular Markdown syntax is not processed within code blocks. E.g.,
asterisks are just literal asterisks within a code block. This means
it's also easy to use Markdown to write about Markdown's own syntax.



<h3 id="hr">Horizontal Rules</h3>

You can produce a horizontal rule tag (<hr />) by placing three or
more hyphens, asterisks, or underscores on a line by themselves. If you
wish, you may use spaces between the hyphens or asterisks. Each of the
following lines will produce a horizontal rule:

    * * *

    ***

    *****
	
    - - -

    ---------------------------------------

	_ _ _


* * *

<h2 id="span">Span Elements</h2>

<h3 id="link">Links</h3>

Markdown supports two style of links: *inline* and *reference*.

In both styles, the link text is delimited by [square brackets].

To create an inline link, use a set of regular parentheses immediately
after the link text's closing square bracket. Inside the parentheses,
put the URL where you want the link to point, along with an *optional*
title for the link, surrounded in quotes. For example:

    This is [an example](http://example.com/ "Title") inline link.

    [This link](http://example.net/) has no title attribute.

Will produce:

    <p>This is <a href="http://example.com/" title="Title">
    an example</a> inline link.</p>

    <p><a href="http://example.net/">This link</a> has no
    title attribute.</p>

If you're referring to a local resource on the same server, you can
use relative paths:

    See my [About](/about/) page for details.

Reference-style links use a second set of square brackets, inside
which you place a label of your choosing to identify the link:

    This is [an example][id] reference-style link.

You can optionally use a space to separate the sets of brackets:

    This is [an example] [id] reference-style link.

Then, anywhere in the document, you define your link label like this,
on a line by itself:

    [id]: http://example.com/  "Optional Title Here"

That is:

*   Square brackets containing the link identifier (optionally
    indented from the left margin using up to three spaces);
*   followed by a colon;
*   followed by one or more spaces (or tabs);
*   followed by the URL for the link;
*   optionally followed by a title attribute for the link, enclosed
    in double or single quotes.

The link URL may, optionally, be surrounded by angle brackets:

    [id]: <http://example.com/>  "Optional Title Here"

You can put the title attribute on the next line and use extra spaces
or tabs for padding, which tends to look better with longer URLs:

    [id]: http://example.com/longish/path/to/resource/here
        "Optional Title Here"

Link definitions are only used for creating links during Markdown
processing, and are stripped from your document in the HTML output.

Link definition names may constist of letters, numbers, spaces, and punctuation -- but they are *not* case sensitive. E.g. these two links:

	[link text][a]
	[link text][A]

are equivalent.

The *implicit link name* shortcut allows you to omit the name of the
link, in which case the link text itself is used as the name.
Just use an empty set of square brackets -- e.g., to link the word
"Google" to the google.com web site, you could simply write:

	[Google][]

And then define the link:

	[Google]: http://google.com/

Because link names may contain spaces, this shortcut even works for
multiple words in the link text:

	Visit [Daring Fireball][] for more information.

And then define the link:
	
	[Daring Fireball]: http://daringfireball.net/

Link definitions can be placed anywhere in your Markdown document. I
tend to put them immediately after each paragraph in which they're
used, but if you want, you can put them all at the end of your
document, sort of like footnotes.

Here's an example of reference links in action:

    I get 10 times more traffic from [Google] [1] than from
    [Yahoo] [2] or [MSN] [3].

      [1]: http://google.com/        "Google"
      [2]: http://search.yahoo.com/  "Yahoo Search"
      [3]: http://search.msn.com/    "MSN Search"

Using the implicit link name shortcut, you could instead write:

    I get 10 times more traffic from [Google][] than from
    [Yahoo][] or [MSN][].

      [google]: http://google.com/        "Google"
      [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
      [msn]:    http://search.msn.com/    "MSN Search"

Both of the above examples will produce the following HTML output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from
    <a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a>
    or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p>

For comparison, here is the same paragraph written using
Markdown's inline link style:

    I get 10 times more traffic from [Google](http://google.com/ "Google")
    than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or
    [MSN](http://search.msn.com/ "MSN Search").

The point of reference-style links is not that they're easier to
write. The point is that with reference-style links, your document
source is vastly more readable. Compare the above examples: using
reference-style links, the paragraph itself is only 81 characters
long; with inline-style links, it's 176 characters; and as raw HTML,
it's 234 characters. In the raw HTML, there's more markup than there
is text.

With Markdown's reference-style links, a source document much more
closely resembles the final output, as rendered in a browser. By
allowing you to move the markup-related metadata out of the paragraph,
you can add links without interrupting the narrative flow of your
prose.


<h3 id="em">Emphasis</h3>

Markdown treats asterisks (*) and underscores (_) as indicators of
emphasis. Text wrapped with one * or _ will be wrapped with an
HTML <em> tag; double *'s or _'s will be wrapped with an HTML
<strong> tag. E.g., this input:

    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__

will produce:

    <em>single asterisks</em>

    <em>single underscores</em>

    <strong>double asterisks</strong>

    <strong>double underscores</strong>

You can use whichever style you prefer; the lone restriction is that
the same character must be used to open and close an emphasis span.

Emphasis can be used in the middle of a word:

    un*fucking*believable

But if you surround an * or _ with spaces, it'll be treated as a
literal asterisk or underscore.

To produce a literal asterisk or underscore at a position where it
would otherwise be used as an emphasis delimiter, you can backslash
escape it:

    \*this text is surrounded by literal asterisks\*



<h3 id="code">Code</h3>

To indicate a span of code, wrap it with backtick quotes (  ).
Unlike a pre-formatted code block, a code span indicates code within a
normal paragraph. For example:

    Use the printf() function.

will produce:

    <p>Use the <code>printf()</code> function.</p>

To include a literal backtick character within a code span, you can use
multiple backticks as the opening and closing delimiters:

     There is a literal backtick () here.

which will produce this:

    <p><code>There is a literal backtick () here.</code></p>

The backtick delimiters surrounding a code span may include spaces --
one after the opening, one before the closing. This allows you to place
literal backtick characters at the beginning or end of a code span:

	A single backtick in a code span:     
	
	A backtick-delimited string in a code span:   foo  

will produce:

	<p>A single backtick in a code span: <code></code></p>
	
	<p>A backtick-delimited string in a code span: <code>foo</code></p>

With a code span, ampersands and angle brackets are encoded as HTML
entities automatically, which makes it easy to include example HTML
tags. Markdown will turn this:

    Please don't use any <blink> tags.

into:

    <p>Please don't use any <code>&lt;blink&gt;</code> tags.</p>

You can write this:

    &#8212; is the decimal-encoded equivalent of &mdash;.

to produce:

    <p><code>&amp;#8212;</code> is the decimal-encoded
    equivalent of <code>&amp;mdash;</code>.</p>



<h3 id="img">Images</h3>

Admittedly, it's fairly difficult to devise a "natural" syntax for
placing images into a plain text document format.

Markdown uses an image syntax that is intended to resemble the syntax
for links, allowing for two styles: *inline* and *reference*.

Inline image syntax looks like this:

    ![Alt text](/path/to/img.jpg)

    ![Alt text](/path/to/img.jpg "Optional title")

That is:

*   An exclamation mark: !;
*   followed by a set of square brackets, containing the alt
    attribute text for the image;
*   followed by a set of parentheses, containing the URL or path to
    the image, and an optional title attribute enclosed in double
    or single quotes.

Reference-style image syntax looks like this:

    ![Alt text][id]

Where "id" is the name of a defined image reference. Image references
are defined using syntax identical to link references:

    [id]: url/to/image  "Optional title attribute"

As of this writing, Markdown has no syntax for specifying the
dimensions of an image; if this is important to you, you can simply
use regular HTML <img> tags.


* * *


<h2 id="misc">Miscellaneous</h2>

<h3 id="autolink">Automatic Links</h3>

Markdown supports a shortcut style for creating "automatic" links for URLs and email addresses: simply surround the URL or email address with angle brackets. What this means is that if you want to show the actual text of a URL or email address, and also have it be a clickable link, you can do this:

    <http://example.com/>
    
Markdown will turn this into:

    <a href="http://example.com/">http://example.com/</a>

Automatic links for email addresses work similarly, except that
Markdown will also perform a bit of randomized decimal and hex
entity-encoding to help obscure your address from address-harvesting
spambots. For example, Markdown will turn this:

    <address@example.com>

into something like this:

    <a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
    &#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
    &#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
    &#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>

which will render in a browser as a clickable link to "address@example.com".

(This sort of entity-encoding trick will indeed fool many, if not
most, address-harvesting bots, but it definitely won't fool all of
them. It's better than nothing, but an address published in this way
will probably eventually start receiving spam.)



<h3 id="backslash">Backslash Escapes</h3>

Markdown allows you to use backslash escapes to generate literal
characters which would otherwise have special meaning in Markdown's
formatting syntax. For example, if you wanted to surround a word with
literal asterisks (instead of an HTML <em> tag), you can backslashes
before the asterisks, like this:

    \*literal asterisks\*

Markdown provides backslash escapes for the following characters:

    \   backslash
       backtick
    *   asterisk
    _   underscore
    {}  curly braces
    []  square brackets
    ()  parentheses
    #   hash mark
	+	plus sign
	-	minus sign (hyphen)
    .   dot
    !   exclamation mark

# Character Escapes

The MD5 value for + is "26b17225b626fb9238849fd60eabdf60".

# HTML Blocks

<p>test</p>

The MD5 value for <p>test</p> is:

6205333b793f34273d75379350b36826* test
+ test
- test

1. test
2. test

* test
+ test
- test

1. test
2. test
> foo
>
> > bar
>
> foo
Valid nesting:

**[Link](url)**

[**Link**](url)

**[**Link**](url)**

Invalid nesting:

[[Link](url)](url)## Unordered

Asterisks tight:

*	asterisk 1
*	asterisk 2
*	asterisk 3


Asterisks loose:

*	asterisk 1

*	asterisk 2

*	asterisk 3

* * *

Pluses tight:

+	Plus 1
+	Plus 2
+	Plus 3


Pluses loose:

+	Plus 1

+	Plus 2

+	Plus 3

* * *


Minuses tight:

-	Minus 1
-	Minus 2
-	Minus 3


Minuses loose:

-	Minus 1

-	Minus 2

-	Minus 3


## Ordered

Tight:

1.	First
2.	Second
3.	Third

and:

1. One
2. Two
3. Three


Loose using tabs:

1.	First

2.	Second

3.	Third

and using spaces:

1. One

2. Two

3. Three

Multiple paragraphs:

1.	Item 1, graf one.

	Item 2. graf two. The quick brown fox jumped over the lazy dog's
	back.
	
2.	Item 2.

3.	Item 3.



## Nested

*	Tab
	*	Tab
		*	Tab

Here's another:

1. First
2. Second:
	* Fee
	* Fie
	* Foe
3. Third

Same thing but with paragraphs:

1. First

2. Second:
	* Fee
	* Fie
	* Foe

3. Third


This was an error in Markdown 1.0.1:

*	this

	*	sub

	that
[Inline link 1 with parens](/url\(test\) "title").

[Inline link 2 with parens](</url\(test\)> "title").

[Inline link 3 with non-escaped parens](/url(test) "title").

[Inline link 4 with non-escaped parens](</url(test)> "title").

[Reference link 1 with parens][1].

[Reference link 2 with parens][2].

  [1]: /url(test) "title"
  [2]: </url(test)> "title"
This tests for a bug where quotes escaped by PHP when using 
preg_replace with the /e modifier must be correctly unescaped
(hence the _UnslashQuotes function found only in PHP Markdown).



Headers below should appear exactly as they are typed (no backslash
added or removed).

Header "quoted\" again \\""
===========================

Header "quoted\" again \\""
---------------------------

### Header "quoted\" again \\"" ###



Test with tabs for _Detab:

	Code	'block'	with	some	"tabs"	and	"quotes"
[Test](/"style="color:red)
[Test](/'style='color:red)

![](/"style="border-color:red;border-size:1px;border-style:solid)
![](/'style='border-color:red;border-size:1px;border-style:solid)
***This is strong and em.***

So is ***this*** word.

___This is strong and em.___

So is ___this___ word.
# Simple tables

Header 1  | Header 2
--------- | ---------
Cell 1    | Cell 2
Cell 3    | Cell 4

With leading pipes:

| Header 1  | Header 2
| --------- | ---------
| Cell 1    | Cell 2
| Cell 3    | Cell 4

With tailing pipes:

Header 1  | Header 2  |
--------- | --------- |
Cell 1    | Cell 2    |
Cell 3    | Cell 4    |

With leading and tailing pipes:

| Header 1  | Header 2  |
| --------- | --------- |
| Cell 1    | Cell 2    |
| Cell 3    | Cell 4    |

* * *

# One-column one-row table

With leading pipes:

| Header
| -------
| Cell

With tailing pipes:

Header  |
------- |
Cell    |

With leading and tailing pipes:

| Header  |
| ------- |
| Cell    |

* * *

Table alignement:

| Default   | Right     |  Center   |     Left  |
| --------- |:--------- |:---------:| ---------:|
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

Table alignement (alternate spacing):

| Default   | Right     |  Center   |     Left  |
| --------- | :-------- | :-------: | --------: |
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

* * * 

# Empty cells

| Header 1  | Header 2  |
| --------- | --------- |
| A         | B         |
| C         |           |

Header 1  | Header 2
--------- | ---------
A         | B
          | D

* * *

# Missing tailing pipe

Header 1  | Header 2  
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- 
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      

* * *

# Too many pipes in rows

| Header 1  | Header 2  |
| --------- 
| Cell      | Cell      | Extra cell? |
| Cell      | Cell      | Extra cell? |

+	this is a list item
	indented with tabs

+   this is a list item
    indented with spaces

Code:

	this code block is indented by one tab

And:

		this code block is indented by two tabs

And:

	+	this is an example list item
		indented with tabs
	
	+   this is an example list item
	    indented with spaces
> A list within a blockquote:
> 
> *	asterisk 1
> *	asterisk 2
> *	asterisk 3
Paragraph and no space:
* ciao

Paragraph and 1 space:
 * ciao

Paragraph and 3 spaces:
  * ciao

Paragraph and 4 spaces:
   * ciao

Paragraph before header:
#Header

Paragraph before blockquote:
>Some quote.
 .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>


As above: checking for bad interractions with the HTML block parser:

 html
<div>


Some *markdown* formatting.

 html
</div>


Some *markdown*


<div>
    <html>



function test();


<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">

<html>
    <title>

</div>

Two code blocks with no blank line between them:


<div>


<div>


Testing *confusion* with markers in the middle:


<div></div>


Testing mixing with title code blocks


<p>
 
<p>

 
<p>

<p>
 

<Fenced>


Code block starting and ending with empty lines:



<Fenced>




Indented code block containing fenced code block sample:

	
	<Fenced>
	

Fenced code block with indented code block sample:


Some text

	Indented code block sample code


Fenced code block with long markers:


Fenced


Fenced code block with fenced code block markers of different length in it:


In code block

Still in code block

Still in code block


Fenced code block with Markdown header and horizontal rule:


#test
---


Fenced code block with link definitions, footnote definition and 
abbreviation definitions:


[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language


* In a list item with smalish indent:

  
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
  
  
With HTML content.
  

<b>bold</b>


Bug with block level elements in this case:

  <div>
  </div>


Indented code block of a fenced code block:

    
	haha!
	

With class:
  
html
<b>bold</b>

  
 html
<b>bold</b>

  
.html
<b>bold</b>

  
 .html
<b>bold</b>


With extra attribute block:

{.html}
<b>bold</b>

  
 {.html #codeid}
<b>bold</b>


 .html{.bold}
<div>

  
 .html {#codeid}
</div>
First line. <br/>
Second line.

This is a first paragraph,
on multiple lines.
     
This is a second paragraph.
There are spaces in between the two.This is a first paragraph,
on multiple lines.

This is a second paragraph
which has multiple lines too.A first paragraph.



A second paragraph after 3 CR (carriage return).This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
     
A few spaces and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
	
1 tab to separate them and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.

A new long long long long long long long long long long long long long long long long paragraph on 1 line.An ampersand & in the text flow is escaped as an html entity.There is an [ampersand](http://validator.w3.org/check?uri=http://www.w3.org/&verbose=1) in the URI.This is \*an asterisk which should stay as is.This is * an asterisk which should stay as is.\\   backslash
\   backtick
\*   asterisk
\_   underscore
\{\}  curly braces
\[\]  square brackets
\(\)  parentheses
\#   hash mark
\+   plus sign
\-   minus sign (hyphen)
\.   dot
\!   exclamation mark> # heading level 1
> 
> paragraph>A blockquote with a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.

>and a second very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.>This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a blockquote.> A blockquote
> on multiple lines
> like this.>A blockquote 
>on multiple lines 
>like this. >A blockquote
>on multiple lines
>like this.
>
>But it has
>two paragraphs.>A blockquote
>on multiple lines
>like this> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.
> This is the first level of quoting.
>
> > This is nested blockquote.> This is the first level of quoting.
> > This is nested blockquote.
> Back to the first level.
> This is the first level of quoting.
> > This is nested blockquote.
	10 PRINT HELLO INFINITE
	20 GOTO 10    10 PRINT < > &
    20 GOTO 10    10 PRINT HELLO INFINITE
    20 GOTO 10# Contributing to Mardown Test Suite

1. [Getting Involved](#getting-involved)
2. [Discussion](#discussion)
3. [How To Report an Issue](#how-to-report-an-issue)
4. [Editing Markdown Specification](#editing-markdown-specification)
5. [Test Suite Guidelines](#test-suite-guidelines)
6. [Pull Request Guidelines](#pull-request-guidelines)

## Getting Involved

There are a number of ways to get involved with the development of the Markdown Test Suite. If you are a first time contributor to an open source project, you can still add value to this project. You may identify grammar issues, write prose, examples or documentation for the project. You may flag some errors and open new issues.

Read all bits of this document and that will guide you on how to participate.

## Discussion

### Mailing List

The Markdown Test Suite has been started a little bit after the start of the [Markdown Community Group](http://www.w3.org/community/markdown/). You may want to discuss about Markdown and this project on the [group mailing-list](http://lists.w3.org/Archives/Public/public-markdown/).

## How to Report an Issue

Don't be afraid to add details to your issue. The more context you give, the better for people participating to the project. Make a short summary, add a description with the context and give links to places which will help to understand.

## Editing Markdown Specification

There is much needed work on the [Markdown Specification](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html). It doesn't require strong competences in coding. Be systematic in the markup and follow the way it is already organized. Each time you added a new atomic section, create a commit for this specific part.

## Test Suite Guidelines

When proposing new tests, make sure they do not already exist in the current test suite. You will notice that there is a separate section dedicated to the specific extensions that some markdown generators have created. Keep them separate. We want to keep the core clean and close to the original specification of Markdown.

If you are not sure, create an issue.

### Markdown Extensions

Markdown extension tests are accepted. Use the following rules:

- place all extension tests under the test/extensions/ENGINE directory with filename equal to the feature name
- for each ENGINE and add a README.markdown under the engine directory with a link to its specification

where ENGINE is either of:

- a command line utility. E.g. pandoc, kramdown.
- a programming API. E.g. Redcarpet::Markdown.new().
- a programmatically accessible web service. E.g.: GFM via the GitHub API.
- a non programmatically accessible web service. E.g.: Stack Overflow flavored markdown.

To avoid test duplication for common features, use the following rules:

- if file tests/extensions/ENGINE/FEATURE.md is empty or not present, use tests/extensions/FEATURE.md instead
- if file tests/extensions/ENGINE/FEATURE.out not present, use tests/extensions/FEATURE.out instead
- for a given ENGINE, only features which have either a .md or a .out are implemented by that engine.
- in case of different outputs for a single feature input, keep directly under extensions/ only the output case that happens across the most engines

**version**

Only the latest stable version of each ENGINE is considered.

**options**

The IO behavior tested is for engine defaults, without any options (command line options, extra JSON parameters, etc.) passed to the engine.

**external state**

Tests that use external state not present in the markdown input shall not be included in this test suite.

For example, what GFM @user user tags render to also depends on the state of GitHub's databases (only render to a link if user exists), not only on the input markdown.

#### Examples

GFM and the "fenced code block" use the following file structure:

    tests/extensions/gfm/README.markdown
    tests/extensions/gfm/fenced-code-block.md
    tests/extensions/gfm/fenced-code-block.out

where README.markdown contains:

    https://help.github.com/articles/github-flavored-markdown

To avoid duplication with other engines, if the input / output (normalized to DOM) is the same across multiple engines use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

If the input is the same, and outputs are DOM different, but represent the same idea (e.g. both represent computer code) use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/gfm/fenced-code-block.out
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

#### New Extensions

Tests are modular, and if you want to test a new engine for your project, that should be easy to do.

If you feel that the new engine is reasonably popular, please send a pull request adding it.

## Commits and Pull Requests

* Keep your commits clean and commented
* Do not mix in one commit different things. Keep modifications related.
* Do not mix everything in one giant pull request. Create separate pull requests for different topic. That will help to have a more meaningful debate about the pull requests and will help to review the code.
* If it relates to a specific issue, add the number of the issue in the commit message.

Thanks for Contributing
as*te*risks*single asterisks*_single underscores_HTML entities are written using ampersand notation: &copy;These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

This is an H1
=============# This is an H1 # # This is an H1# this is an h1 with two trailing spaces  
A new paragraph.# This is an H1This is an H2
-------------## This is an H2 #### This is an H2### This is an H3 ###### This is an H3#### This is an H4 ######## This is an H4##### This is an H5 ########## This is an H5###### This is an H6  ############ This is an H6- - ----***___-------![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 for everyone"![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 logo for everyone")![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png)We love <code> and & for everything We love code for everything We love code for everything The MIT License (MIT)

Copyright (c) 2013 Karl Dubost

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
A first sentence  
and a line break.A first sentence     
and a line break.This is an automatic link <http://www.w3.org/>[W3C](http://www.w3.org/ "Discover w3c")[W3C](http://www.w3.org/)[World Wide Web Consortium][w3c]

[w3c]: <http://www.w3.org/>[World Wide Web Consortium][]

[World Wide Web Consortium]: http://www.w3.org/[w3c][]

[w3c]: http://www.w3.org/[World Wide Web Consortium] [w3c]

[w3c]: http://www.w3.org/[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/
   "Discover W3C"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ (Discover w3c)[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ 'Discover w3c'[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ "Discover w3c"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/*   a list containing a blockquote

    > this the blockquote in the list* a

        b
*   a list containing a block of code

	    10 PRINT HELLO INFINITE
	    20 GOTO 10*   This is a list item with two paragraphs. Lorem ipsum dolor
	sit amet, consectetuer adipiscing elit. Aliquam hendrerit
	mi posuere lectus.

	Vestibulum enim wisi, viverra nec, fringilla in, laoreet
	vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
	sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.*   This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.1\. ordered list escape1. 1

    - inner par list

2. 2
1. list item 1
8. list item 2
1. list item 31. list item 1
2. list item 2
3. list item 3This is a paragraph
on multiple lines
with hard return.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line. This is a paragraph with a trailing and leading space. This is a paragraph with 1 trailing tab.	  This is a paragraph with 2 leading spaces.   This is a paragraph with 3 leading spaces. This is a paragraph with 1 leading space.This is a paragraph with a trailing space. # Colophon - October 1st, 2014

This project was initiated to provide a test suite for Markdown markup, and eventually create a specification from this test results. A part of of the community has started a new endeavor which seems to get traction as [CommonMark](https://github.com/jgm/stmd). **We are then closing this project** and encourage you to contribute to CommonMark. 

The most interesting part of this project would not have been possible without the dedication of [Ciro Santilli](https://github.com/cirosantilli) @cirosantilli. So big applause and thank you to him.


The rest is kept around for archives and references.

# Markdown Test Suite

Inspired by questions on [W3C Markdown Community Group](http://www.w3.org/community/markdown).

Pull Requests are welcome. See the [CONTRIBUTING Guidelines](https://github.com/karlcow/markdown-testsuite/blob/master/CONTRIBUTING.md)

## Design goals

- Comprehensive.
- Small modularized tests.
- Easy to run tests using any programming language. In particular, data representations must have an implementation on all major languages.
- Develop a consensus based markdown specification at [markdown-spec.html](markdown-spec.html). Visualize it [here](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html).

## Test Scripts

Markdown Test Suite already includes tests for many important markdown engines.

To see what the scripts do run:

    ./cat-all.py -h
    ./run-tests.py -h

To configure the scripts do:

	cp config_local.py.example config_local.py

and edit config_local.py. It is already gitignored.

A Vagrantfile is provided with a provision script that installs all installable engines.

Sample output from run-tests.py:

    blackfriday   |......FFF..............FF...F....................................F....................................|   0.93s  102    7   6%
	gfm           |FF.....F.....F...FFFF..F....F........................FFFF...FF...............FF...F.......F...........| 262.88s  102   20  19%
    hoedown       |..............................F.................................................F.....................|   0.36s  102    2   1%
	kramdown      |......FFF.....FF.......FF.......FF.FFFFFFFFFFFFF.......................F..............................|  30.69s  102   23  22%
    lunamark      |FFFFFF.F.FFFFFFFFFFFF.F.....FFFF..FF............FFFFF..FFFFFFFFFF..............F...FFFFFFFFFFF........|   1.58s  103   53  51%
    markdown_pl   |.....................FFFF...............................F...............F.............................|   2.56s  102    6   5%
    markdown2     |......................................................................................................|   5.39s  103    0   0%
    marked        |..............F.................FFFFFFFFFFFFFFFF......................F.F.............................|   6.22s  102   19  18%
    maruku        |......FFF......F.......F.FFF...............................................FF.........................|  37.02s  102   10   9%
    md2html       |.........................FFF...F............................................FF........................|   7.42s  102    6   5%
    multimarkdown |......FFF....FF...F............FFF.FFFFFFFFFFFFF.....FFFF.........F...................................|   0.58s  102   27  26%
    pandoc        |FF...........F.F.FFFF..FFFFF....FF.FFFFFFFFFFFFF.....FFFF.....FF............FFF.FFF..................F|   1.11s  102   41  40%
    peg_markdown  |.................................................................F....................................|   0.46s  102    1   0%
    rdiscount     |.......F.........................................................F....................................|  25.19s  102    3   2%
    redcarpet     |......................................................................................................|  21.49s  102    0   0%
    showdown      |.......................................................................F..............................|   6.85s  102    1   0%

	Extensions:

    blackfriday   |F..|  0.04s    3    1  33%
	gfm           |F.|   2.37s    2    1  50%
    hoedown       |.|    0.00s    1    0   0%
    lunamark      |F.F|  0.05s    3    2  66%
    kramdown      |..|   0.62s    2    0   0%
    markdown_pl   ||     0.00s    0    0   0%
    markdown2     |F.|   0.14s    2    1  50%
    marked        |F.|   0.13s    2    1  50%
    maruku        |F..|  1.06s    3    1  33%
    md2html       |F.|   0.14s    2    0   0%
    multimarkdown |F.|   0.01s    2    1  50%
    pandoc        |F.|   0.02s    2    1  50%
    peg_markdown  |...|  0.02s    3    0   0%
    rdiscount     |F..|   0.74s    3    1  33%
    redcarpet     |..|   0.42s    2    0   0%
    showdown      |F..|  0.20s    3    1  33%

Where F indicates a failing test.

## Other Noticeable Test Suites

We haven't been the first test suite effort. Some projects have maintained their own test suite for a long time. Hopefully we can reach a state where people agree on the terms of what should be a good test suite for all developers.

- [Original test suite](http://daringfireball.net/projects/downloads/MarkdownTest_1.0.zip)
- [PHP markdown test suite:](https://github.com/michelf/mdtest/tree/master/Markdown.mdtest)
- [Markdown-js test suite](https://github.com/evilstreak/markdown-js/tree/master/test/features)
- [Python markdown 2 test suite](https://github.com/trentm/python-markdown2/tree/master/test/tm-cases)
- [multimarkdown test suite](https://github.com/fletcher/MMD-Test-Suite)
- [John MacFarlane's Standard Markdown spec](https://github.com/jgm/stmd)

In addition we should note the [wonderful work](http://johnmacfarlane.net/babelmark2/) made by John Mac Farlane. The Web service output the differences in between the different markdown implementations. It helps a lot when searching on the most common output.
as**te**risks**double asterisks**__double underscores__* list item 1
* list item 2
* list item 3
- list item 1
- list item 2
- list item 3 * list item 1
 * list item 2
 * list item 3  * list item 1
  * list item 2
  * list item 3   * list item 1
   * list item 2
   * list item 3+ list item 1
+ list item 2
+ list item 3* list item in paragraph

* another list item in paragraph*   This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a list.
*   and yet another long long long long long long long long long long long long long long long long long long long long long long line.*   This is a list item
    with the content on
    multiline and indented.
*   And this another list item
    with the same principle.€Some text about HTML, SGML and HTML4.

Let's talk about the U.S.A., (É.U. or É.-U. d'A. in French).

*[HTML4]: Hyper Text Markup Language version 4
*[HTML]: Hyper Text Markup Language
*[SGML]: Standard Generalized Markup Language
*[U.S.A.]: United States of America
*[É.U.] : États-Unis d'Amérique
*[É.-U. d'A.] : États-Unis d'Amérique

And here we have a CD, some CDs, and some other CD's.

*[CD]: Compact Disk

Let's transfert documents through TCP/IP, using TCP packets.

*[IP]: Internet Protocol
*[TCP]: Transmission Control Protocol

 ---

Bienvenue sur [CMS](http://www.bidulecms.com "Bidule CMS").

*[CMS]: Content Management System

 ---

ATCCE

*[ATCCE]: Abbreviation "Testing" Correct 'Character' < Escapes >* one
* two

1. three
2. four

* one
* two
1. three
2. fourAT&T has an ampersand in their name.

AT&amp;T is another way to write it.

This & that.

4 < 5.

6 > 5.

Here's a [link] [1] with an ampersand in the URL.

Here's a link with an amersand in the link text: [AT&T] [2].

Here's an inline [link](/script?foo=1&bar=2).

Here's an inline [link](</script?foo=1&bar=2>).


[1]: http://example.com/?foo=1&bar=2
[2]: http://att.com/  "AT&T"Link: <http://example.com/>.

With an ampersand: <http://example.com/?foo=1&bar=2>

* In a list?
* <http://example.com/>
* It should.

> Blockquoted: <http://example.com/>

Auto-links should not occur here: <http://example.com/>

	or here: <http://example.com/>These should all get escaped:

Backslash: \\

Backtick: \

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-



These should not, because they occur within a code block:

	Backslash: \\

	Backtick: \

	Asterisk: \*

	Underscore: \_

	Left brace: \{

	Right brace: \}

	Left bracket: \[

	Right bracket: \]

	Left paren: \(

	Right paren: \)

	Greater-than: \>

	Hash: \#

	Period: \.

	Bang: \!

	Plus: \+

	Minus: \-


Nor should these, which occur in code spans:

Backslash: \\

Backtick:   \  

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-


These should get escaped, even though they're matching pairs for
other Markdown constructs:

\*asterisks\*

\_underscores\_

\backticks\

This is a code span with a literal backslash-backtick sequence:   \  

This is a tag with unescaped backticks <span attr='ticks'>bar</span>.

This is a tag with backslashes <span attr='\\backslashes\\'>bar</span>.
  .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>
 

As above: checking for bad interractions with the HTML block parser:

  html
<div>
 

Some *markdown* formatting.

  html
</div>
 

Some *markdown*

 
<div>
    <html>
 

 
function test();
 

<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">
 
<html>
    <title>
 
</div>

Two code blocks with no blank line between them:

 
<div>
 
 
<div>
 

Testing *confusion* with code spans at the HTML block parser:

 
<div></div>
 

Testing mixing with title code blocks

 
<p>

<p>
 

<p>
 
<p>

 
<Fenced>
 

Code block starting and ending with empty lines:
 


<Fenced>


 

Indented code block containing fenced code block sample:

	 
	<Fenced>
	 

Fenced code block with indented code block sample:

 
Some text

	Indented code block sample code
 

Fenced code block with long markers:

 
Fenced
 

Fenced code block with fenced code block markers of different length in it:

 
In code block
 
Still in code block
 
Still in code block
 

Fenced code block with Markdown header and horizontal rule:

 
#test
---
 

Fenced code block with link definitions, footnote definition and
abbreviation definitions:

 
[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language
 

* In a list item with smalish indent:

   
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
   

With HTML content.

 
<b>bold</b>
 

Bug with block level elements in this case:
 
  <div>
  </div>
 

Indented code block of a fenced code block:

     
	haha!
	 

With class:

 html
<b>bold</b>
 

  html
<b>bold</b>
 

 .html
<b>bold</b>
 

  .html
<b>bold</b>
 

With extra attribute block:

 {.html}
<b>bold</b>
 

  {.html #codeid}
<b>bold</b>
 

  .html{.bold}
<div>
 
  
  .html {#codeid}
</div>
 > Example:
> 
>     sub status {
>         print "working";
>     }
> 
> Or:
> 
>     sub status {
>         return "working";
>     }

*	List Item:

		code block

		with a blank line

	within a list item.

*       code block
        as first element of a list item

*	List Item:
	
		code block with whitespace on preceding line
    Codeblock on second line
    <?php
    echo "hello!";
    ?>

foo bar

    <?php
    echo "hello!";

lorem ipsum

    echo "hello!";
    ?>
    
lorem ipsum	code block on the first line
	
Regular text.

    code block indented by spaces

Regular text.

	the lines in this block  
	all contain trailing spaces  

Regular Text.

	code block on the last line<test a=" content of attribute ">

Fix for backticks within HTML tag: <span attr='ticks'>like this</span>

Here's how you put   backticks   in a code span.A simple definition list:

Term 1
:   Definition 1

Term 2
:   Definition 2

With multiple terms:

Term 1
Term 2
:   Definition 1

Term 3
Term 4
:   Definition 2

With multiple definitions:

Term 1
:   Definition 1
:   Definition 2

Term 2
:   Definition 3
:   Definition 4

With multiple lines per definition:

Term 1
:   Definition 1 line 1 ...
Definition 1 line 2
:   Definition 2 line 1 ...
Definition 2 line 2

Term 2
:   Definition 3 line 2 ...
    Definition 3 line 2
:   Definition 4 line 2 ...
    Definition 4 line 2

With paragraphs:

Term 1

:   Definition 1 (paragraph)

Term 2

:   Definition 2 (paragraph)

With multiple paragraphs:

Term 1

:   Definition 1 paragraph 1 line 1 ...
	Definition 1 paragraph 1 line 2

    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)

    Definition 1 paragraph 2 line 1 ...
Definition 1 paragraph 2 line 2 (lazy)

* * *

A mix:

Term 1
Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)
    
    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

:   Definition 2 paragraph 1 line 1 ...
Definition 2 paragraph 1 line 2 (lazy)

Term 3
:   Definition 3 (no paragraph)
:   Definition 4 (no paragraph)
:   Definition 5 line 1 ...
    Definition 5 line 2 (no paragraph)

:   Definition 6 paragraph 1 line 1 ...
Definition 6 paragraph 1 line 2
:   Definition 7 (no paragraph)
:   Definition 8 paragraph 1 line 1 (forced paragraph) ...
    Definition 8 paragraph 1 line 2
    
    Definition 8 paragraph 2 line 1
    
Term 4
:   Definition 9 paragraph 1 line 1 (forced paragraph) ...
    Definition 9 paragraph 1 line 2
    
    Definition 9 paragraph 2 line 1
:   Definition 10 (no paragraph)

* * *

Special cases:

Term

:       code block
        as first element of a definition<michel.fortin@michelf.ca>

International domain names: <help@tūdaliņ.lv>


## Some weird valid email addresses

<abc.123@example.com>

<1234567890@example.com>

<_______@example.com>

<abc+mailbox/department=shipping@example.com>

<!#$%&'*+-/=?^_.{|}@example.com> (all of these characters are allowed)

<"abc@def"@example.com> (anything goes inside quotation marks)

<"Fred Bloggs"@example.com>

<jsmith@[192.0.2.1]>

<"A"@example.com>Combined emphasis:

1.  ***test test***
2.  ___test test___
3.  *test **test***
4.  **test *test***
5.  ***test* test**
6.  ***test** test*
7.  ***test* test**
8.  **test *test***
9.  *test **test***
10. _test __test___
11. __test _test___
12. ___test_ test__
13. ___test__ test_
14. ___test_ test__
15. __test _test___
16. _test __test___
17. *test __test__*
18. **test _test_**
19. **_test_ test**
20. *__test__ test*
21. **_test_ test**
22. **test _test_**
23. *test __test__*
24. _test **test**_
25. __test *test*__
26. __*test* test__
27. _**test** test_
28. __*test* test__
29. __test *test*__
30. _test **test**_


Incorrect nesting:

1.  *test  **test*  test**
2.  _test  __test_  test__
3.  **test  *test** test*
4.  __test  _test__ test_
5.  *test   *test*  test*
6.  _test   _test_  test_
7.  **test **test** test**
8.  __test __test__ test__
9. _**some text_**
10. *__some text*__
11. **_some text**_
12. *__some text*__

No emphasis:

1.  test*  test  *test
2.  test** test **test
3.  test_  test  _test
4.  test__ test __test



Middle-word emphasis (asterisks):

1.  *a*b
2.   a*b*
3.   a*b*c
4. **a**b
5.   a**b**
6.   a**b**c


Middle-word emphasis (underscore):

1.  _a_b
2.   a_b_
3.   a_b_c
4. __a__b
5.   a__b__
6.   a__b__c

my_precious_file.txt


## Tricky Cases

E**. **Test** TestTestTest

E**. **Test** Test Test Test


## Overlong emphasis

Name: ____________  
Organization: ____  
Region/Country: __

_____Cut here_____

____Cut here____

# Regression

_**Note**_: This _is emphasis_.
With asterisks

 * List item
 *
 * List item

With numbers

1. List item
2.
3. List item

With hyphens

- List item
-
- List item

With asterisks

 * List item
 * List item
 *

With numbers

1. List item
2. List item
3.

With hyphens

- List item
- List item
-
This is the first paragraph.[^first]

[^first]:  This is the first note.

* List item one.[^second]
* List item two.[^third]

[^third]: This is the third note, defined out of order.
[^second]: This is the second note.
[^fourth]: This is the fourth note.

# Header[^fourth]

Some paragraph with a footnote[^1], and another[^2].

[^1]: Content for fifth footnote.
[^2]: Content for sixth footnote spaning on 
    three lines, with some span-level markup like
    _emphasis_, a [link][].

[link]: http://michelf.ca/

Another paragraph with a named footnote[^fn-name].

[^fn-name]:
    Footnote beginning on the line next to the marker.

This paragraph should not have a footnote marker since 
the footnote is undefined.[^3]

This paragraph has a second footnote marker to footnote number one.[^1]

This paragraph links to a footnote with plenty of 
block-level content.[^block]

[^block]:
	Paragraph.
	
	*   List item
	
	> Blockquote
	
	    Code block

This paragraph host the footnote reference within a 
footnote test[^reference].

[^reference]:
	This footnote has a footnote of its own.[^nested]

[^nested]:
	This footnote should appear even though it is referenced
	from another footnote. But [^reference] should be litteral
	since the footnote with that name has already been used.

 - - -

Testing unusual footnote name[^1$^!"'].

[^1$^!"']: Haha!

 - - -
 
Footnotes mixed with images[^image-mixed]
![1800 Travel][img6]
![1830 Travel][img7]

[img6]: images/MGR-1800-travel.jpeg "Travel Speeds in 1800"
[^image-mixed]: Footnote Content
[img7]: images/MGR-1830-travel.jpeg "Travel Speeds in 1830"
In Markdown 1.0.0 and earlier. Version
8. This line turns into a list item.
Because a hard-wrapped line in the
middle of a paragraph looked like a
list item.

Here's one with a bullet.
* criminey.
Header  {#id1}
======

Header  { #id2}
------

### Header  {#id3 }
#### Header ##  { #id4 }

 - - -

Header  {.cl}
======

Header  { .cl}
------

### Header  {.cl }
#### Header ##  { .cl }

 - - -

Header  {.cl.class}
======

Header  { .cl .class}
------

### Header  {.cl .class }
#### Header ##  { .cl.class }

 - - -

Header  {#id5.cl.class}
======

Header  { #id6 .cl .class}
------

### Header  {.cl.class#id7 }
#### Header ##  { .cl.class#id8 }
Header
======

Header
------

### Header

 - - -

Header
======
Paragraph

Header
------
Paragraph

### Header
Paragraph

 - - -

Paragraph
Header
======
Paragraph

Paragraph
Header
------
Paragraph

Paragraph
### Header
ParagraphDashes:

---

 ---
 
  ---

   ---

	---

- - -

 - - -
 
  - - -

   - - -

	- - -


Asterisks:

***

 ***
 
  ***

   ***

	***

* * *

 * * *
 
  * * *

   * * *

	* * *


Underscores:

___

 ___
 
  ___

   ___

    ___

_ _ _

 _ _ _
 
  _ _ _

   _ _ _

    _ _ _
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")

Inline within a paragraph: [alt text](/url/).

![alt text](/url/  "title preceded by two spaces")

![alt text](/url/  "title has spaces afterward"  )

![alt text](</url/>)

![alt text](</url/> "with a title").

![Empty]()

![this is a stupid URL](http://example.com/(parens).jpg)


![alt text][foo]

  [foo]: /url/

![alt text][bar]

  [bar]: /url/ "Title here"Simple block on one line:

<div>foo</div>

And nested without indentation:

<div>
<div>
<div>
foo
</div>
<div style=">"/>
</div>
<div>bar</div>
</div>

And with attributes:

<div>
	<div id="foo">
	</div>
</div>

This was broken in 1.0.2b7:

<div class="inlinepage">
<div class="toggleableend">
foo
</div>
</div>
Here's a simple block:

<div>
	foo
</div>

This should be a code block, though:

	<div>
		foo
	</div>

As should this:

	<div>foo</div>

Now, nested:

<div>
	<div>
		<div>
			foo
		</div>
	</div>
</div>

This should just be an HTML comment:

<!-- Comment -->

Multiline:

<!--
Blah
Blah
-->

Code block:

	<!-- Comment -->

Just plain comment, with trailing spaces on the line:

<!-- foo -->   

Code:

	<hr />
	
Hr's:

<hr>

<hr/>

<hr />

<hr>   

<hr/>  

<hr /> 

<hr class="foo" id="bar" />

<hr class="foo" id="bar"/>

<hr class="foo" id="bar" >

<abbr title=" **Attribute Content Is Not A Code Span** ">ACINACS</abbr>

<abbr title="first backtick!">SB</abbr> 
<abbr title="second backtick!">SB</abbr>Paragraph one.

<!-- This is a simple comment -->

<!--
	This is another comment.
-->

Paragraph two.

<!-- one comment block -- -- with two comments -->

The end.
# Markdown inside code blocks

<div markdown="1">
foo
</div>

<div markdown='1'>
foo
</div>

<div markdown=1>
foo
</div>

<table>
<tr><td markdown="1">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="span">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="block">test _emphasis_ (block)</td></tr>
</table>

## More complicated

<table>
<tr><td markdown="1">
* this is _not_ a list item</td></tr>
<tr><td markdown="span">
* this is _not_ a list item</td></tr>
<tr><td markdown="block">
* this _is_ a list item
</td></tr>
</table>

## With indent

<div>
    <div markdown="1">
    This text is no code block: if it was, the 
    closing <div> would be too and the HTML block 
    would be invalid.

    Markdown content in HTML blocks is assumed to be 
    indented the same as the block opening tag.

    **This should be the third paragraph after the header.**
    </div>
</div>

## Code block with rogue </div>s in Markdown code span and block

<div>
    <div markdown="1">

    This is a code block however:

        </div>

    Funny isn't it? Here is a code span: </div>.

    </div>
</div>

<div>
  <div markdown="1">
    * List item, not a code block

Some text

      This is a code block.
  </div>
</div>

## No code block in markdown span mode

<p markdown="1">
    This is not a code block since Markdown parse paragraph 
    content as span. Code spans like </p> are allowed though.
</p>

<p markdown="1">_Hello_ _world_</p>

## Preserving attributes and tags on more than one line:

<p class="test" markdown="1" 
id="12">
Some _span_ content.
</p>


## Header confusion bug

<table class="canvas">
<tr>
<td id="main" markdown="1">Hello World!
============

Hello World!</td>
</tr>
</table>
Here is a block tag ins:

<ins>
<p>Some text</p>
</ins>

<ins>And here it is inside a paragraph.</ins>

And here it is <ins>in the middle of</ins> a paragraph.

<del>
<p>Some text</p>
</del>

<del>And here is ins as a paragraph.</del>

And here it is <del>in the middle of</del> a paragraph.
		    GNU GENERAL PUBLIC LICENSE
		       Version 2, June 1991

 Copyright (C) 1989, 1991 Free Software Foundation, Inc.,
 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

			    Preamble

  The licenses for most software are designed to take away your
freedom to share and change it.  By contrast, the GNU General Public
License is intended to guarantee your freedom to share and change free
software--to make sure the software is free for all its users.  This
General Public License applies to most of the Free Software
Foundation's software and to any other program whose authors commit to
using it.  (Some other Free Software Foundation software is covered by
the GNU Lesser General Public License instead.)  You can apply it to
your programs, too.

  When we speak of free software, we are referring to freedom, not
price.  Our General Public Licenses are designed to make sure that you
have the freedom to distribute copies of free software (and charge for
this service if you wish), that you receive source code or can get it
if you want it, that you can change the software or use pieces of it
in new free programs; and that you know you can do these things.

  To protect your rights, we need to make restrictions that forbid
anyone to deny you these rights or to ask you to surrender the rights.
These restrictions translate to certain responsibilities for you if you
distribute copies of the software, or if you modify it.

  For example, if you distribute copies of such a program, whether
gratis or for a fee, you must give the recipients all the rights that
you have.  You must make sure that they, too, receive or can get the
source code.  And you must show them these terms so they know their
rights.

  We protect your rights with two steps: (1) copyright the software, and
(2) offer you this license which gives you legal permission to copy,
distribute and/or modify the software.

  Also, for each author's protection and ours, we want to make certain
that everyone understands that there is no warranty for this free
software.  If the software is modified by someone else and passed on, we
want its recipients to know that what they have is not the original, so
that any problems introduced by others will not reflect on the original
authors' reputations.

  Finally, any free program is threatened constantly by software
patents.  We wish to avoid the danger that redistributors of a free
program will individually obtain patent licenses, in effect making the
program proprietary.  To prevent this, we have made it clear that any
patent must be licensed for everyone's free use or not licensed at all.

  The precise terms and conditions for copying, distribution and
modification follow.

		    GNU GENERAL PUBLIC LICENSE
   TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

  0. This License applies to any program or other work which contains
a notice placed by the copyright holder saying it may be distributed
under the terms of this General Public License.  The "Program", below,
refers to any such program or work, and a "work based on the Program"
means either the Program or any derivative work under copyright law:
that is to say, a work containing the Program or a portion of it,
either verbatim or with modifications and/or translated into another
language.  (Hereinafter, translation is included without limitation in
the term "modification".)  Each licensee is addressed as "you".

Activities other than copying, distribution and modification are not
covered by this License; they are outside its scope.  The act of
running the Program is not restricted, and the output from the Program
is covered only if its contents constitute a work based on the
Program (independent of having been made by running the Program).
Whether that is true depends on what the Program does.

  1. You may copy and distribute verbatim copies of the Program's
source code as you receive it, in any medium, provided that you
conspicuously and appropriately publish on each copy an appropriate
copyright notice and disclaimer of warranty; keep intact all the
notices that refer to this License and to the absence of any warranty;
and give any other recipients of the Program a copy of this License
along with the Program.

You may charge a fee for the physical act of transferring a copy, and
you may at your option offer warranty protection in exchange for a fee.

  2. You may modify your copy or copies of the Program or any portion
of it, thus forming a work based on the Program, and copy and
distribute such modifications or work under the terms of Section 1
above, provided that you also meet all of these conditions:

    a) You must cause the modified files to carry prominent notices
    stating that you changed the files and the date of any change.

    b) You must cause any work that you distribute or publish, that in
    whole or in part contains or is derived from the Program or any
    part thereof, to be licensed as a whole at no charge to all third
    parties under the terms of this License.

    c) If the modified program normally reads commands interactively
    when run, you must cause it, when started running for such
    interactive use in the most ordinary way, to print or display an
    announcement including an appropriate copyright notice and a
    notice that there is no warranty (or else, saying that you provide
    a warranty) and that users may redistribute the program under
    these conditions, and telling the user how to view a copy of this
    License.  (Exception: if the Program itself is interactive but
    does not normally print such an announcement, your work based on
    the Program is not required to print an announcement.)

These requirements apply to the modified work as a whole.  If
identifiable sections of that work are not derived from the Program,
and can be reasonably considered independent and separate works in
themselves, then this License, and its terms, do not apply to those
sections when you distribute them as separate works.  But when you
distribute the same sections as part of a whole which is a work based
on the Program, the distribution of the whole must be on the terms of
this License, whose permissions for other licensees extend to the
entire whole, and thus to each and every part regardless of who wrote it.

Thus, it is not the intent of this section to claim rights or contest
your rights to work written entirely by you; rather, the intent is to
exercise the right to control the distribution of derivative or
collective works based on the Program.

In addition, mere aggregation of another work not based on the Program
with the Program (or with a work based on the Program) on a volume of
a storage or distribution medium does not bring the other work under
the scope of this License.

  3. You may copy and distribute the Program (or a work based on it,
under Section 2) in object code or executable form under the terms of
Sections 1 and 2 above provided that you also do one of the following:

    a) Accompany it with the complete corresponding machine-readable
    source code, which must be distributed under the terms of Sections
    1 and 2 above on a medium customarily used for software interchange; or,

    b) Accompany it with a written offer, valid for at least three
    years, to give any third party, for a charge no more than your
    cost of physically performing source distribution, a complete
    machine-readable copy of the corresponding source code, to be
    distributed under the terms of Sections 1 and 2 above on a medium
    customarily used for software interchange; or,

    c) Accompany it with the information you received as to the offer
    to distribute corresponding source code.  (This alternative is
    allowed only for noncommercial distribution and only if you
    received the program in object code or executable form with such
    an offer, in accord with Subsection b above.)

The source code for a work means the preferred form of the work for
making modifications to it.  For an executable work, complete source
code means all the source code for all modules it contains, plus any
associated interface definition files, plus the scripts used to
control compilation and installation of the executable.  However, as a
special exception, the source code distributed need not include
anything that is normally distributed (in either source or binary
form) with the major components (compiler, kernel, and so on) of the
operating system on which the executable runs, unless that component
itself accompanies the executable.

If distribution of executable or object code is made by offering
access to copy from a designated place, then offering equivalent
access to copy the source code from the same place counts as
distribution of the source code, even though third parties are not
compelled to copy the source along with the object code.

  4. You may not copy, modify, sublicense, or distribute the Program
except as expressly provided under this License.  Any attempt
otherwise to copy, modify, sublicense or distribute the Program is
void, and will automatically terminate your rights under this License.
However, parties who have received copies, or rights, from you under
this License will not have their licenses terminated so long as such
parties remain in full compliance.

  5. You are not required to accept this License, since you have not
signed it.  However, nothing else grants you permission to modify or
distribute the Program or its derivative works.  These actions are
prohibited by law if you do not accept this License.  Therefore, by
modifying or distributing the Program (or any work based on the
Program), you indicate your acceptance of this License to do so, and
all its terms and conditions for copying, distributing or modifying
the Program or works based on it.

  6. Each time you redistribute the Program (or any work based on the
Program), the recipient automatically receives a license from the
original licensor to copy, distribute or modify the Program subject to
these terms and conditions.  You may not impose any further
restrictions on the recipients' exercise of the rights granted herein.
You are not responsible for enforcing compliance by third parties to
this License.

  7. If, as a consequence of a court judgment or allegation of patent
infringement or for any other reason (not limited to patent issues),
conditions are imposed on you (whether by court order, agreement or
otherwise) that contradict the conditions of this License, they do not
excuse you from the conditions of this License.  If you cannot
distribute so as to satisfy simultaneously your obligations under this
License and any other pertinent obligations, then as a consequence you
may not distribute the Program at all.  For example, if a patent
license would not permit royalty-free redistribution of the Program by
all those who receive copies directly or indirectly through you, then
the only way you could satisfy both it and this License would be to
refrain entirely from distribution of the Program.

If any portion of this section is held invalid or unenforceable under
any particular circumstance, the balance of the section is intended to
apply and the section as a whole is intended to apply in other
circumstances.

It is not the purpose of this section to induce you to infringe any
patents or other property right claims or to contest validity of any
such claims; this section has the sole purpose of protecting the
integrity of the free software distribution system, which is
implemented by public license practices.  Many people have made
generous contributions to the wide range of software distributed
through that system in reliance on consistent application of that
system; it is up to the author/donor to decide if he or she is willing
to distribute software through any other system and a licensee cannot
impose that choice.

This section is intended to make thoroughly clear what is believed to
be a consequence of the rest of this License.

  8. If the distribution and/or use of the Program is restricted in
certain countries either by patents or by copyrighted interfaces, the
original copyright holder who places the Program under this License
may add an explicit geographical distribution limitation excluding
those countries, so that distribution is permitted only in or among
countries not thus excluded.  In such case, this License incorporates
the limitation as if written in the body of this License.

  9. The Free Software Foundation may publish revised and/or new versions
of the General Public License from time to time.  Such new versions will
be similar in spirit to the present version, but may differ in detail to
address new problems or concerns.

Each version is given a distinguishing version number.  If the Program
specifies a version number of this License which applies to it and "any
later version", you have the option of following the terms and conditions
either of that version or of any later version published by the Free
Software Foundation.  If the Program does not specify a version number of
this License, you may choose any version ever published by the Free Software
Foundation.

  10. If you wish to incorporate parts of the Program into other free
programs whose distribution conditions are different, write to the author
to ask for permission.  For software which is copyrighted by the Free
Software Foundation, write to the Free Software Foundation; we sometimes
make exceptions for this.  Our decision will be guided by the two goals
of preserving the free status of all derivatives of our free software and
of promoting the sharing and reuse of software generally.

			    NO WARRANTY

  11. BECAUSE THE PROGRAM IS LICENSED FREE OF CHARGE, THERE IS NO WARRANTY
FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW.  EXCEPT WHEN
OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES
PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED
OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.  THE ENTIRE RISK AS
TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU.  SHOULD THE
PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING,
REPAIR OR CORRECTION.

  12. IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING
WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MAY MODIFY AND/OR
REDISTRIBUTE THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES,
INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING
OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED
TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY
YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER
PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES.

		     END OF TERMS AND CONDITIONS

	    How to Apply These Terms to Your New Programs

  If you develop a new program, and you want it to be of the greatest
possible use to the public, the best way to achieve this is to make it
free software which everyone can redistribute and change under these terms.

  To do so, attach the following notices to the program.  It is safest
to attach them to the start of each source file to most effectively
convey the exclusion of warranty; and each file should have at least
the "copyright" line and a pointer to where the full notice is found.

    <one line to give the program's name and a brief idea of what it does.>
    Copyright (C) <year>  <name of author>

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

Also add information on how to contact you by electronic and paper mail.

If the program is interactive, make it output a short notice like this
when it starts in an interactive mode:

    Gnomovision version 69, Copyright (C) year name of author
    Gnomovision comes with ABSOLUTELY NO WARRANTY; for details type show w'.
    This is free software, and you are welcome to redistribute it
    under certain conditions; type show c' for details.

The hypothetical commands show w' and show c' should show the appropriate
parts of the General Public License.  Of course, the commands you use may
be called something other than show w' and show c'; they could even be
mouse-clicks or menu items--whatever suits your program.

You should also get your employer (if you work as a programmer) or your
school, if any, to sign a "copyright disclaimer" for the program, if
necessary.  Here is a sample; alter the names:

  Yoyodyne, Inc., hereby disclaims all copyright interest in the program
  Gnomovision' (which makes passes at compilers) written by James Hacker.

  <signature of Ty Coon>, 1 April 1989
  Ty Coon, President of Vice

This General Public License does not permit incorporating your program into
proprietary programs.  If your program is a subroutine library, you may
consider it more useful to permit linking proprietary applications with the
library.  If this is what you want to do, use the GNU Lesser General
Public License instead of this License.
This is an [inline link](/url "title"){.class #inline-link}.

This is a [reference link][refid].

This is an ![inline image](/img "title"){.class #inline-img}.

This is a ![reference image][refid].

[refid]: /path/to/something (Title) { .class #ref data-key=val }

Just a [URL](/url/).

[URL and title](/url/ "title").

[URL and title](/url/  "title preceded by two spaces").

[URL and title](/url/	"title preceded by a tab").

[URL and title](/url/ "title has spaces afterward"  ).

[URL wrapped in angle brackets](</url/>).

[URL w/ angle brackets + title](</url/> "Here's the title").

[Empty]().

[With parens in the URL](http://en.wikipedia.org/wiki/WIMP_(computing))

(With outer parens and [parens in url](/foo(bar)))


[With parens in the URL](/foo(bar) "and a title")

(With outer parens and [parens in url](/foo(bar) "and a title"))
Foo [bar] [1].

Foo [bar][1].

Foo [bar]
[1].

[1]: /url/  "Title"


With [embedded [brackets]] [b].


Indented [once][].

Indented [twice][].

Indented [thrice][].

Indented [four][] times.

 [once]: /url

  [twice]: /url

   [thrice]: /url

    [four]: /url


[b]: /url/

* * *

[this] [this] should work

So should [this][this].

And [this] [].

And [this][].

And [this].

But not [that] [].

Nor [that][].

Nor [that].

[Something in brackets like [this][] should work]

[Same with [this].]

In this case, [this](/somethingelse/) points to something else.

Backslashing should suppress \[this] and [this\].

[this]: foo


* * *

Here's one where the [link
breaks] across lines.

Here's another where the [link 
breaks] across lines, but with a line-ending space.


[link breaks]: /url/
This is the [simple case].

[simple case]: /simple



This one has a [line
break].

This one has a [line 
break] with a line-ending space.

[line break]: /foo


[this] [that] and the [other]

[this]: /this
[that]: /that
[other]: /other
Foo [bar][].

Foo [bar](/url/ "Title with "quotes" inside").


  [bar]: /url/ "Title with "quotes" inside"

Markdown: Basics
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a class="selected" title="Markdown Basics">Basics</a></li>
    <li><a href="/projects/markdown/syntax" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


Getting the Gist of Markdown's Formatting Syntax
------------------------------------------------

This page offers a brief overview of what it's like to use Markdown.
The [syntax page] [s] provides complete, detailed documentation for
every feature, but Markdown should be very easy to pick up simply by
looking at a few examples of it in action. The examples on this page
are written in a before/after style, showing example syntax and the
HTML output produced by Markdown.

It's also helpful to simply try Markdown out; the [Dingus] [d] is a
web application that allows you type your own Markdown-formatted text
and translate it to XHTML.

**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL] [src].

  [s]: /projects/markdown/syntax  "Markdown Syntax"
  [d]: /projects/markdown/dingus  "Markdown Dingus"
  [src]: /projects/markdown/basics.text


## Paragraphs, Headers, Blockquotes ##

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

Markdown offers two styles of headers: *Setext* and *atx*.
Setext-style headers for <h1> and <h2> are created by
"underlining" with equal signs (=) and hyphens (-), respectively.
To create an atx-style header, you put 1-6 hash marks (#) at the
beginning of the line -- the number of hashes equals the resulting
HTML header level.

Blockquotes are indicated using email-style '>' angle brackets.

Markdown:

    A First Level Header
    ====================
    
    A Second Level Header
    ---------------------

    Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.

    The quick brown fox jumped over the lazy
    dog's back.
    
    ### Header 3

    > This is a blockquote.
    > 
    > This is the second paragraph in the blockquote.
    >
    > ## This is an H2 in a blockquote


Output:

    <h1>A First Level Header</h1>
    
    <h2>A Second Level Header</h2>
    
    <p>Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.</p>
    
    <p>The quick brown fox jumped over the lazy
    dog's back.</p>
    
    <h3>Header 3</h3>
    
    <blockquote>
        <p>This is a blockquote.</p>
        
        <p>This is the second paragraph in the blockquote.</p>
        
        <h2>This is an H2 in a blockquote</h2>
    </blockquote>



### Phrase Emphasis ###

Markdown uses asterisks and underscores to indicate spans of emphasis.

Markdown:

    Some of these words *are emphasized*.
    Some of these words _are emphasized also_.
    
    Use two asterisks for **strong emphasis**.
    Or, if you prefer, __use two underscores instead__.

Output:

    <p>Some of these words <em>are emphasized</em>.
    Some of these words <em>are emphasized also</em>.</p>
    
    <p>Use two asterisks for <strong>strong emphasis</strong>.
    Or, if you prefer, <strong>use two underscores instead</strong>.</p>
   


## Lists ##

Unordered (bulleted) lists use asterisks, pluses, and hyphens (*,
+, and -) as list markers. These three markers are
interchangable; this:

    *   Candy.
    *   Gum.
    *   Booze.

this:

    +   Candy.
    +   Gum.
    +   Booze.

and this:

    -   Candy.
    -   Gum.
    -   Booze.

all produce the same output:

    <ul>
    <li>Candy.</li>
    <li>Gum.</li>
    <li>Booze.</li>
    </ul>

Ordered (numbered) lists use regular numbers, followed by periods, as
list markers:

    1.  Red
    2.  Green
    3.  Blue

Output:

    <ol>
    <li>Red</li>
    <li>Green</li>
    <li>Blue</li>
    </ol>

If you put blank lines between items, you'll get <p> tags for the
list item text. You can create multi-paragraph list items by indenting
the paragraphs by 4 spaces or 1 tab:

    *   A list item.
    
        With multiple paragraphs.

    *   Another item in the list.

Output:

    <ul>
    <li><p>A list item.</p>
    <p>With multiple paragraphs.</p></li>
    <li><p>Another item in the list.</p></li>
    </ul>
    


### Links ###

Markdown supports two styles for creating links: *inline* and
*reference*. With both styles, you use square brackets to delimit the
text you want to turn into a link.

Inline-style links use parentheses immediately after the link text.
For example:

    This is an [example link](http://example.com/).

Output:

    <p>This is an <a href="http://example.com/">
    example link</a>.</p>

Optionally, you may include a title attribute in the parentheses:

    This is an [example link](http://example.com/ "With a Title").

Output:

    <p>This is an <a href="http://example.com/" title="With a Title">
    example link</a>.</p>

Reference-style links allow you to refer to your links by names, which
you define elsewhere in your document:

    I get 10 times more traffic from [Google][1] than from
    [Yahoo][2] or [MSN][3].

    [1]: http://google.com/        "Google"
    [2]: http://search.yahoo.com/  "Yahoo Search"
    [3]: http://search.msn.com/    "MSN Search"

Output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from <a href="http://search.yahoo.com/"
    title="Yahoo Search">Yahoo</a> or <a href="http://search.msn.com/"
    title="MSN Search">MSN</a>.</p>

The title attribute is optional. Link names may contain letters,
numbers and spaces, but are *not* case sensitive:

    I start my morning with a cup of coffee and
    [The New York Times][NY Times].

    [ny times]: http://www.nytimes.com/

Output:

    <p>I start my morning with a cup of coffee and
    <a href="http://www.nytimes.com/">The New York Times</a>.</p>


### Images ###

Image syntax is very much like link syntax.

Inline (titles are optional):

    ![alt text](/path/to/img.jpg "Title")

Reference-style:

    ![alt text][id]

    [id]: /path/to/img.jpg "Title"

Both of the above examples produce the same output:

    <img src="/path/to/img.jpg" alt="alt text" title="Title" />



### Code ###

In a regular paragraph, you can create code span by wrapping text in
backtick quotes. Any ampersands (&) and angle brackets (< or
>) will automatically be translated into HTML entities. This makes
it easy to use Markdown to write about HTML example code:

    I strongly recommend against using any <blink> tags.

    I wish SmartyPants used named entities like &mdash;
    instead of decimal-encoded entites like &#8212;.

Output:

    <p>I strongly recommend against using any
    <code>&lt;blink&gt;</code> tags.</p>
    
    <p>I wish SmartyPants used named entities like
    <code>&amp;mdash;</code> instead of decimal-encoded
    entites like <code>&amp;#8212;</code>.</p>


To specify an entire block of pre-formatted code, indent every line of
the block by 4 spaces or 1 tab. Just like with code spans, &, <,
and > characters will be escaped automatically.

Markdown:

    If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:

        <blockquote>
            <p>For example.</p>
        </blockquote>

Output:

    <p>If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:</p>
    
    <pre><code>&lt;blockquote&gt;
        &lt;p&gt;For example.&lt;/p&gt;
    &lt;/blockquote&gt;
    </code></pre>
Markdown: Syntax
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a href="/projects/markdown/basics" title="Markdown Basics">Basics</a></li>
    <li><a class="selected" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


*   [Overview](#overview)
    *   [Philosophy](#philosophy)
    *   [Inline HTML](#html)
    *   [Automatic Escaping for Special Characters](#autoescape)
*   [Block Elements](#block)
    *   [Paragraphs and Line Breaks](#p)
    *   [Headers](#header)
    *   [Blockquotes](#blockquote)
    *   [Lists](#list)
    *   [Code Blocks](#precode)
    *   [Horizontal Rules](#hr)
*   [Span Elements](#span)
    *   [Links](#link)
    *   [Emphasis](#em)
    *   [Code](#code)
    *   [Images](#img)
*   [Miscellaneous](#misc)
    *   [Backslash Escapes](#backslash)
    *   [Automatic Links](#autolink)


**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL][src].

  [src]: /projects/markdown/syntax.text

* * *

<h2 id="overview">Overview</h2>

<h3 id="philosophy">Philosophy</h3>

Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

Readability, however, is emphasized above all else. A Markdown-formatted
document should be publishable as-is, as plain text, without looking
like it's been marked up with tags or formatting instructions. While
Markdown's syntax has been influenced by several existing text-to-HTML
filters -- including [Setext] [1], [atx] [2], [Textile] [3], [reStructuredText] [4],
[Grutatext] [5], and [EtText] [6] -- the single biggest source of
inspiration for Markdown's syntax is the format of plain text email.

  [1]: http://docutils.sourceforge.net/mirror/setext.html
  [2]: http://www.aaronsw.com/2002/atx/
  [3]: http://textism.com/tools/textile/
  [4]: http://docutils.sourceforge.net/rst.html
  [5]: http://www.triptico.com/software/grutatxt.html
  [6]: http://ettext.taint.org/doc/

To this end, Markdown's syntax is comprised entirely of punctuation
characters, which punctuation characters have been carefully chosen so
as to look like what they mean. E.g., asterisks around a word actually
look like \*emphasis\*. Markdown lists look like, well, lists. Even
blockquotes look like quoted passages of text, assuming you've ever
used email.



<h3 id="html">Inline HTML</h3>

Markdown's syntax is intended for one purpose: to be used as a
format for *writing* for the web.

Markdown is not a replacement for HTML, or even close to it. Its
syntax is very small, corresponding only to a very small subset of
HTML tags. The idea is *not* to create a syntax that makes it easier
to insert HTML tags. In my opinion, HTML tags are already easy to
insert. The idea for Markdown is to make it easy to read, write, and
edit prose. HTML is a *publishing* format; Markdown is a *writing*
format. Thus, Markdown's formatting syntax only addresses issues that
can be conveyed in plain text.

For any markup that is not covered by Markdown's syntax, you simply
use HTML itself. There's no need to preface it or delimit it to
indicate that you're switching from Markdown to HTML; you just use
the tags.

The only restrictions are that block-level HTML elements -- e.g. <div>,
<table>, <pre>, <p>, etc. -- must be separated from surrounding
content by blank lines, and the start and end tags of the block should
not be indented with tabs or spaces. Markdown is smart enough not
to add extra (unwanted) <p> tags around HTML block-level tags.

For example, to add an HTML table to a Markdown article:

    This is a regular paragraph.

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    This is another regular paragraph.

Note that Markdown formatting syntax is not processed within block-level
HTML tags. E.g., you can't use Markdown-style *emphasis* inside an
HTML block.

Span-level HTML tags -- e.g. <span>, <cite>, or <del> -- can be
used anywhere in a Markdown paragraph, list item, or header. If you
want, you can even use HTML tags instead of Markdown formatting; e.g. if
you'd prefer to use HTML <a> or <img> tags instead of Markdown's
link or image syntax, go right ahead.

Unlike block-level HTML tags, Markdown syntax *is* processed within
span-level tags.


<h3 id="autoescape">Automatic Escaping for Special Characters</h3>

In HTML, there are two characters that demand special treatment: <
and &. Left angle brackets are used to start tags; ampersands are
used to denote HTML entities. If you want to use them as literal
characters, you must escape them as entities, e.g. &lt;, and
&amp;.

Ampersands in particular are bedeviling for web writers. If you want to
write about 'AT&T', you need to write 'AT&amp;T'. You even need to
escape ampersands within URLs. Thus, if you want to link to:

    http://images.google.com/images?num=30&q=larry+bird

you need to encode the URL as:

    http://images.google.com/images?num=30&amp;q=larry+bird

in your anchor tag href attribute. Needless to say, this is easy to
forget, and is probably the single most common source of HTML validation
errors in otherwise well-marked-up web sites.

Markdown allows you to use these characters naturally, taking care of
all the necessary escaping for you. If you use an ampersand as part of
an HTML entity, it remains unchanged; otherwise it will be translated
into &amp;.

So, if you want to include a copyright symbol in your article, you can write:

    &copy;

and Markdown will leave it alone. But if you write:

    AT&T

Markdown will translate it to:

    AT&amp;T

Similarly, because Markdown supports [inline HTML](#html), if you use
angle brackets as delimiters for HTML tags, Markdown will treat them as
such. But if you write:

    4 < 5

Markdown will translate it to:

    4 &lt; 5

However, inside Markdown code spans and blocks, angle brackets and
ampersands are *always* encoded automatically. This makes it easy to use
Markdown to write about HTML code. (As opposed to raw HTML, which is a
terrible format for writing about HTML syntax, because every single <
and & in your example code needs to be escaped.)


* * *


<h2 id="block">Block Elements</h2>


<h3 id="p">Paragraphs and Line Breaks</h3>

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing but spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

The implication of the "one or more consecutive lines of text" rule is
that Markdown supports "hard-wrapped" text paragraphs. This differs
significantly from most other text-to-HTML formatters (including Movable
Type's "Convert Line Breaks" option) which translate every line break
character in a paragraph into a <br /> tag.

When you *do* want to insert a <br /> break tag using Markdown, you
end a line with two or more spaces, then type return.

Yes, this takes a tad more effort to create a <br />, but a simplistic
"every line break is a <br />" rule wouldn't work for Markdown.
Markdown's email-style [blockquoting][bq] and multi-paragraph [list items][l]
work best -- and look better -- when you format them with hard breaks.

  [bq]: #blockquote
  [l]:  #list



<h3 id="header">Headers</h3>

Markdown supports two styles of headers, [Setext] [1] and [atx] [2].

Setext-style headers are "underlined" using equal signs (for first-level
headers) and dashes (for second-level headers). For example:

    This is an H1
    =============

    This is an H2
    -------------

Any number of underlining ='s or -'s will work.

Atx-style headers use 1-6 hash characters at the start of the line,
corresponding to header levels 1-6. For example:

    # This is an H1

    ## This is an H2

    ###### This is an H6

Optionally, you may "close" atx-style headers. This is purely
cosmetic -- you can use this if you think it looks better. The
closing hashes don't even need to match the number of hashes
used to open the header. (The number of opening hashes
determines the header level.) :

    # This is an H1 #

    ## This is an H2 ##

    ### This is an H3 ######


<h3 id="blockquote">Blockquotes</h3>

Markdown uses email-style > characters for blockquoting. If you're
familiar with quoting passages of text in an email message, then you
know how to create a blockquote in Markdown. It looks best if you hard
wrap the text and put a > before every line:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    > 
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

Markdown allows you to be lazy and only put the > before the first
line of a hard-wrapped paragraph:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

Blockquotes can be nested (i.e. a blockquote-in-a-blockquote) by
adding additional levels of >:

    > This is the first level of quoting.
    >
    > > This is nested blockquote.
    >
    > Back to the first level.

Blockquotes can contain other Markdown elements, including headers, lists,
and code blocks:

	> ## This is a header.
	> 
	> 1.   This is the first list item.
	> 2.   This is the second list item.
	> 
	> Here's some example code:
	> 
	>     return shell_exec("echo $input | $markdown_script");

Any decent text editor should make email-style quoting easy. For
example, with BBEdit, you can make a selection and choose Increase
Quote Level from the Text menu.


<h3 id="list">Lists</h3>

Markdown supports ordered (numbered) and unordered (bulleted) lists.

Unordered lists use asterisks, pluses, and hyphens -- interchangably
-- as list markers:

    *   Red
    *   Green
    *   Blue

is equivalent to:

    +   Red
    +   Green
    +   Blue

and:

    -   Red
    -   Green
    -   Blue

Ordered lists use numbers followed by periods:

    1.  Bird
    2.  McHale
    3.  Parish

It's important to note that the actual numbers you use to mark the
list have no effect on the HTML output Markdown produces. The HTML
Markdown produces from the above list is:

    <ol>
    <li>Bird</li>
    <li>McHale</li>
    <li>Parish</li>
    </ol>

If you instead wrote the list in Markdown like this:

    1.  Bird
    1.  McHale
    1.  Parish

or even:

    3. Bird
    1. McHale
    8. Parish

you'd get the exact same HTML output. The point is, if you want to,
you can use ordinal numbers in your ordered Markdown lists, so that
the numbers in your source match the numbers in your published HTML.
But if you want to be lazy, you don't have to.

If you do use lazy list numbering, however, you should still start the
list with the number 1. At some point in the future, Markdown may support
starting ordered lists at an arbitrary number.

List markers typically start at the left margin, but may be indented by
up to three spaces. List markers must be followed by one or more spaces
or a tab.

To make lists look nice, you can wrap items with hanging indents:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
        Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
        viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
        Suspendisse id sem consectetuer libero luctus adipiscing.

But if you want to be lazy, you don't have to:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.

If list items are separated by blank lines, Markdown will wrap the
items in <p> tags in the HTML output. For example, this input:

    *   Bird
    *   Magic

will turn into:

    <ul>
    <li>Bird</li>
    <li>Magic</li>
    </ul>

But this:

    *   Bird

    *   Magic

will turn into:

    <ul>
    <li><p>Bird</p></li>
    <li><p>Magic</p></li>
    </ul>

List items may consist of multiple paragraphs. Each subsequent
paragraph in a list item must be intended by either 4 spaces
or one tab:

    1.  This is a list item with two paragraphs. Lorem ipsum dolor
        sit amet, consectetuer adipiscing elit. Aliquam hendrerit
        mi posuere lectus.

        Vestibulum enim wisi, viverra nec, fringilla in, laoreet
        vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
        sit amet velit.

    2.  Suspendisse id sem consectetuer libero luctus adipiscing.

It looks nice if you indent every line of the subsequent
paragraphs, but here again, Markdown will allow you to be
lazy:

    *   This is a list item with two paragraphs.

        This is the second paragraph in the list item. You're
    only required to indent the first line. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit.

    *   Another item in the same list.

To put a blockquote within a list item, the blockquote's >
delimiters need to be indented:

    *   A list item with a blockquote:

        > This is a blockquote
        > inside a list item.

To put a code block within a list item, the code block needs
to be indented *twice* -- 8 spaces or two tabs:

    *   A list item with a code block:

            <code goes here>


It's worth noting that it's possible to trigger an ordered list by
accident, by writing something like this:

    1986. What a great season.

In other words, a *number-period-space* sequence at the beginning of a
line. To avoid this, you can backslash-escape the period:

    1986\. What a great season.



<h3 id="precode">Code Blocks</h3>

Pre-formatted code blocks are used for writing about programming or
markup source code. Rather than forming normal paragraphs, the lines
of a code block are interpreted literally. Markdown wraps a code block
in both <pre> and <code> tags.

To produce a code block in Markdown, simply indent every line of the
block by at least 4 spaces or 1 tab. For example, given this input:

    This is a normal paragraph:

        This is a code block.

Markdown will generate:

    <p>This is a normal paragraph:</p>

    <pre><code>This is a code block.
    </code></pre>

One level of indentation -- 4 spaces or 1 tab -- is removed from each
line of the code block. For example, this:

    Here is an example of AppleScript:

        tell application "Foo"
            beep
        end tell

will turn into:

    <p>Here is an example of AppleScript:</p>

    <pre><code>tell application "Foo"
        beep
    end tell
    </code></pre>

A code block continues until it reaches a line that is not indented
(or the end of the article).

Within a code block, ampersands (&) and angle brackets (< and >)
are automatically converted into HTML entities. This makes it very
easy to include example HTML source code using Markdown -- just paste
it and indent it, and Markdown will handle the hassle of encoding the
ampersands and angle brackets. For example, this:

        <div class="footer">
            &copy; 2004 Foo Corporation
        </div>

will turn into:

    <pre><code>&lt;div class="footer"&gt;
        &amp;copy; 2004 Foo Corporation
    &lt;/div&gt;
    </code></pre>

Regular Markdown syntax is not processed within code blocks. E.g.,
asterisks are just literal asterisks within a code block. This means
it's also easy to use Markdown to write about Markdown's own syntax.



<h3 id="hr">Horizontal Rules</h3>

You can produce a horizontal rule tag (<hr />) by placing three or
more hyphens, asterisks, or underscores on a line by themselves. If you
wish, you may use spaces between the hyphens or asterisks. Each of the
following lines will produce a horizontal rule:

    * * *

    ***

    *****
	
    - - -

    ---------------------------------------

	_ _ _


* * *

<h2 id="span">Span Elements</h2>

<h3 id="link">Links</h3>

Markdown supports two style of links: *inline* and *reference*.

In both styles, the link text is delimited by [square brackets].

To create an inline link, use a set of regular parentheses immediately
after the link text's closing square bracket. Inside the parentheses,
put the URL where you want the link to point, along with an *optional*
title for the link, surrounded in quotes. For example:

    This is [an example](http://example.com/ "Title") inline link.

    [This link](http://example.net/) has no title attribute.

Will produce:

    <p>This is <a href="http://example.com/" title="Title">
    an example</a> inline link.</p>

    <p><a href="http://example.net/">This link</a> has no
    title attribute.</p>

If you're referring to a local resource on the same server, you can
use relative paths:

    See my [About](/about/) page for details.

Reference-style links use a second set of square brackets, inside
which you place a label of your choosing to identify the link:

    This is [an example][id] reference-style link.

You can optionally use a space to separate the sets of brackets:

    This is [an example] [id] reference-style link.

Then, anywhere in the document, you define your link label like this,
on a line by itself:

    [id]: http://example.com/  "Optional Title Here"

That is:

*   Square brackets containing the link identifier (optionally
    indented from the left margin using up to three spaces);
*   followed by a colon;
*   followed by one or more spaces (or tabs);
*   followed by the URL for the link;
*   optionally followed by a title attribute for the link, enclosed
    in double or single quotes.

The link URL may, optionally, be surrounded by angle brackets:

    [id]: <http://example.com/>  "Optional Title Here"

You can put the title attribute on the next line and use extra spaces
or tabs for padding, which tends to look better with longer URLs:

    [id]: http://example.com/longish/path/to/resource/here
        "Optional Title Here"

Link definitions are only used for creating links during Markdown
processing, and are stripped from your document in the HTML output.

Link definition names may constist of letters, numbers, spaces, and punctuation -- but they are *not* case sensitive. E.g. these two links:

	[link text][a]
	[link text][A]

are equivalent.

The *implicit link name* shortcut allows you to omit the name of the
link, in which case the link text itself is used as the name.
Just use an empty set of square brackets -- e.g., to link the word
"Google" to the google.com web site, you could simply write:

	[Google][]

And then define the link:

	[Google]: http://google.com/

Because link names may contain spaces, this shortcut even works for
multiple words in the link text:

	Visit [Daring Fireball][] for more information.

And then define the link:
	
	[Daring Fireball]: http://daringfireball.net/

Link definitions can be placed anywhere in your Markdown document. I
tend to put them immediately after each paragraph in which they're
used, but if you want, you can put them all at the end of your
document, sort of like footnotes.

Here's an example of reference links in action:

    I get 10 times more traffic from [Google] [1] than from
    [Yahoo] [2] or [MSN] [3].

      [1]: http://google.com/        "Google"
      [2]: http://search.yahoo.com/  "Yahoo Search"
      [3]: http://search.msn.com/    "MSN Search"

Using the implicit link name shortcut, you could instead write:

    I get 10 times more traffic from [Google][] than from
    [Yahoo][] or [MSN][].

      [google]: http://google.com/        "Google"
      [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
      [msn]:    http://search.msn.com/    "MSN Search"

Both of the above examples will produce the following HTML output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from
    <a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a>
    or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p>

For comparison, here is the same paragraph written using
Markdown's inline link style:

    I get 10 times more traffic from [Google](http://google.com/ "Google")
    than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or
    [MSN](http://search.msn.com/ "MSN Search").

The point of reference-style links is not that they're easier to
write. The point is that with reference-style links, your document
source is vastly more readable. Compare the above examples: using
reference-style links, the paragraph itself is only 81 characters
long; with inline-style links, it's 176 characters; and as raw HTML,
it's 234 characters. In the raw HTML, there's more markup than there
is text.

With Markdown's reference-style links, a source document much more
closely resembles the final output, as rendered in a browser. By
allowing you to move the markup-related metadata out of the paragraph,
you can add links without interrupting the narrative flow of your
prose.


<h3 id="em">Emphasis</h3>

Markdown treats asterisks (*) and underscores (_) as indicators of
emphasis. Text wrapped with one * or _ will be wrapped with an
HTML <em> tag; double *'s or _'s will be wrapped with an HTML
<strong> tag. E.g., this input:

    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__

will produce:

    <em>single asterisks</em>

    <em>single underscores</em>

    <strong>double asterisks</strong>

    <strong>double underscores</strong>

You can use whichever style you prefer; the lone restriction is that
the same character must be used to open and close an emphasis span.

Emphasis can be used in the middle of a word:

    un*fucking*believable

But if you surround an * or _ with spaces, it'll be treated as a
literal asterisk or underscore.

To produce a literal asterisk or underscore at a position where it
would otherwise be used as an emphasis delimiter, you can backslash
escape it:

    \*this text is surrounded by literal asterisks\*



<h3 id="code">Code</h3>

To indicate a span of code, wrap it with backtick quotes (  ).
Unlike a pre-formatted code block, a code span indicates code within a
normal paragraph. For example:

    Use the printf() function.

will produce:

    <p>Use the <code>printf()</code> function.</p>

To include a literal backtick character within a code span, you can use
multiple backticks as the opening and closing delimiters:

     There is a literal backtick () here.

which will produce this:

    <p><code>There is a literal backtick () here.</code></p>

The backtick delimiters surrounding a code span may include spaces --
one after the opening, one before the closing. This allows you to place
literal backtick characters at the beginning or end of a code span:

	A single backtick in a code span:     
	
	A backtick-delimited string in a code span:   foo  

will produce:

	<p>A single backtick in a code span: <code></code></p>
	
	<p>A backtick-delimited string in a code span: <code>foo</code></p>

With a code span, ampersands and angle brackets are encoded as HTML
entities automatically, which makes it easy to include example HTML
tags. Markdown will turn this:

    Please don't use any <blink> tags.

into:

    <p>Please don't use any <code>&lt;blink&gt;</code> tags.</p>

You can write this:

    &#8212; is the decimal-encoded equivalent of &mdash;.

to produce:

    <p><code>&amp;#8212;</code> is the decimal-encoded
    equivalent of <code>&amp;mdash;</code>.</p>



<h3 id="img">Images</h3>

Admittedly, it's fairly difficult to devise a "natural" syntax for
placing images into a plain text document format.

Markdown uses an image syntax that is intended to resemble the syntax
for links, allowing for two styles: *inline* and *reference*.

Inline image syntax looks like this:

    ![Alt text](/path/to/img.jpg)

    ![Alt text](/path/to/img.jpg "Optional title")

That is:

*   An exclamation mark: !;
*   followed by a set of square brackets, containing the alt
    attribute text for the image;
*   followed by a set of parentheses, containing the URL or path to
    the image, and an optional title attribute enclosed in double
    or single quotes.

Reference-style image syntax looks like this:

    ![Alt text][id]

Where "id" is the name of a defined image reference. Image references
are defined using syntax identical to link references:

    [id]: url/to/image  "Optional title attribute"

As of this writing, Markdown has no syntax for specifying the
dimensions of an image; if this is important to you, you can simply
use regular HTML <img> tags.


* * *


<h2 id="misc">Miscellaneous</h2>

<h3 id="autolink">Automatic Links</h3>

Markdown supports a shortcut style for creating "automatic" links for URLs and email addresses: simply surround the URL or email address with angle brackets. What this means is that if you want to show the actual text of a URL or email address, and also have it be a clickable link, you can do this:

    <http://example.com/>
    
Markdown will turn this into:

    <a href="http://example.com/">http://example.com/</a>

Automatic links for email addresses work similarly, except that
Markdown will also perform a bit of randomized decimal and hex
entity-encoding to help obscure your address from address-harvesting
spambots. For example, Markdown will turn this:

    <address@example.com>

into something like this:

    <a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
    &#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
    &#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
    &#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>

which will render in a browser as a clickable link to "address@example.com".

(This sort of entity-encoding trick will indeed fool many, if not
most, address-harvesting bots, but it definitely won't fool all of
them. It's better than nothing, but an address published in this way
will probably eventually start receiving spam.)



<h3 id="backslash">Backslash Escapes</h3>

Markdown allows you to use backslash escapes to generate literal
characters which would otherwise have special meaning in Markdown's
formatting syntax. For example, if you wanted to surround a word with
literal asterisks (instead of an HTML <em> tag), you can backslashes
before the asterisks, like this:

    \*literal asterisks\*

Markdown provides backslash escapes for the following characters:

    \   backslash
       backtick
    *   asterisk
    _   underscore
    {}  curly braces
    []  square brackets
    ()  parentheses
    #   hash mark
	+	plus sign
	-	minus sign (hyphen)
    .   dot
    !   exclamation mark

# Character Escapes

The MD5 value for + is "26b17225b626fb9238849fd60eabdf60".

# HTML Blocks

<p>test</p>

The MD5 value for <p>test</p> is:

6205333b793f34273d75379350b36826* test
+ test
- test

1. test
2. test

* test
+ test
- test

1. test
2. test
> foo
>
> > bar
>
> foo
Valid nesting:

**[Link](url)**

[**Link**](url)

**[**Link**](url)**

Invalid nesting:

[[Link](url)](url)## Unordered

Asterisks tight:

*	asterisk 1
*	asterisk 2
*	asterisk 3


Asterisks loose:

*	asterisk 1

*	asterisk 2

*	asterisk 3

* * *

Pluses tight:

+	Plus 1
+	Plus 2
+	Plus 3


Pluses loose:

+	Plus 1

+	Plus 2

+	Plus 3

* * *


Minuses tight:

-	Minus 1
-	Minus 2
-	Minus 3


Minuses loose:

-	Minus 1

-	Minus 2

-	Minus 3


## Ordered

Tight:

1.	First
2.	Second
3.	Third

and:

1. One
2. Two
3. Three


Loose using tabs:

1.	First

2.	Second

3.	Third

and using spaces:

1. One

2. Two

3. Three

Multiple paragraphs:

1.	Item 1, graf one.

	Item 2. graf two. The quick brown fox jumped over the lazy dog's
	back.
	
2.	Item 2.

3.	Item 3.



## Nested

*	Tab
	*	Tab
		*	Tab

Here's another:

1. First
2. Second:
	* Fee
	* Fie
	* Foe
3. Third

Same thing but with paragraphs:

1. First

2. Second:
	* Fee
	* Fie
	* Foe

3. Third


This was an error in Markdown 1.0.1:

*	this

	*	sub

	that
[Inline link 1 with parens](/url\(test\) "title").

[Inline link 2 with parens](</url\(test\)> "title").

[Inline link 3 with non-escaped parens](/url(test) "title").

[Inline link 4 with non-escaped parens](</url(test)> "title").

[Reference link 1 with parens][1].

[Reference link 2 with parens][2].

  [1]: /url(test) "title"
  [2]: </url(test)> "title"
This tests for a bug where quotes escaped by PHP when using 
preg_replace with the /e modifier must be correctly unescaped
(hence the _UnslashQuotes function found only in PHP Markdown).



Headers below should appear exactly as they are typed (no backslash
added or removed).

Header "quoted\" again \\""
===========================

Header "quoted\" again \\""
---------------------------

### Header "quoted\" again \\"" ###



Test with tabs for _Detab:

	Code	'block'	with	some	"tabs"	and	"quotes"
[Test](/"style="color:red)
[Test](/'style='color:red)

![](/"style="border-color:red;border-size:1px;border-style:solid)
![](/'style='border-color:red;border-size:1px;border-style:solid)
***This is strong and em.***

So is ***this*** word.

___This is strong and em.___

So is ___this___ word.
# Simple tables

Header 1  | Header 2
--------- | ---------
Cell 1    | Cell 2
Cell 3    | Cell 4

With leading pipes:

| Header 1  | Header 2
| --------- | ---------
| Cell 1    | Cell 2
| Cell 3    | Cell 4

With tailing pipes:

Header 1  | Header 2  |
--------- | --------- |
Cell 1    | Cell 2    |
Cell 3    | Cell 4    |

With leading and tailing pipes:

| Header 1  | Header 2  |
| --------- | --------- |
| Cell 1    | Cell 2    |
| Cell 3    | Cell 4    |

* * *

# One-column one-row table

With leading pipes:

| Header
| -------
| Cell

With tailing pipes:

Header  |
------- |
Cell    |

With leading and tailing pipes:

| Header  |
| ------- |
| Cell    |

* * *

Table alignement:

| Default   | Right     |  Center   |     Left  |
| --------- |:--------- |:---------:| ---------:|
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

Table alignement (alternate spacing):

| Default   | Right     |  Center   |     Left  |
| --------- | :-------- | :-------: | --------: |
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

* * * 

# Empty cells

| Header 1  | Header 2  |
| --------- | --------- |
| A         | B         |
| C         |           |

Header 1  | Header 2
--------- | ---------
A         | B
          | D

* * *

# Missing tailing pipe

Header 1  | Header 2  
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- 
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      

* * *

# Too many pipes in rows

| Header 1  | Header 2  |
| --------- 
| Cell      | Cell      | Extra cell? |
| Cell      | Cell      | Extra cell? |

+	this is a list item
	indented with tabs

+   this is a list item
    indented with spaces

Code:

	this code block is indented by one tab

And:

		this code block is indented by two tabs

And:

	+	this is an example list item
		indented with tabs
	
	+   this is an example list item
	    indented with spaces
> A list within a blockquote:
> 
> *	asterisk 1
> *	asterisk 2
> *	asterisk 3
Paragraph and no space:
* ciao

Paragraph and 1 space:
 * ciao

Paragraph and 3 spaces:
  * ciao

Paragraph and 4 spaces:
   * ciao

Paragraph before header:
#Header

Paragraph before blockquote:
>Some quote.
 .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>


As above: checking for bad interractions with the HTML block parser:

 html
<div>


Some *markdown* formatting.

 html
</div>


Some *markdown*


<div>
    <html>



function test();


<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">

<html>
    <title>

</div>

Two code blocks with no blank line between them:


<div>


<div>


Testing *confusion* with markers in the middle:


<div></div>


Testing mixing with title code blocks


<p>
 
<p>

 
<p>

<p>
 

<Fenced>


Code block starting and ending with empty lines:



<Fenced>




Indented code block containing fenced code block sample:

	
	<Fenced>
	

Fenced code block with indented code block sample:


Some text

	Indented code block sample code


Fenced code block with long markers:


Fenced


Fenced code block with fenced code block markers of different length in it:


In code block

Still in code block

Still in code block


Fenced code block with Markdown header and horizontal rule:


#test
---


Fenced code block with link definitions, footnote definition and 
abbreviation definitions:


[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language


* In a list item with smalish indent:

  
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
  
  
With HTML content.
  

<b>bold</b>


Bug with block level elements in this case:

  <div>
  </div>


Indented code block of a fenced code block:

    
	haha!
	

With class:
  
html
<b>bold</b>

  
 html
<b>bold</b>

  
.html
<b>bold</b>

  
 .html
<b>bold</b>


With extra attribute block:

{.html}
<b>bold</b>

  
 {.html #codeid}
<b>bold</b>


 .html{.bold}
<div>

  
 .html {#codeid}
</div>
First line. <br/>
Second line.

This is a first paragraph,
on multiple lines.
     
This is a second paragraph.
There are spaces in between the two.This is a first paragraph,
on multiple lines.

This is a second paragraph
which has multiple lines too.A first paragraph.



A second paragraph after 3 CR (carriage return).This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
     
A few spaces and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
	
1 tab to separate them and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.

A new long long long long long long long long long long long long long long long long paragraph on 1 line.An ampersand & in the text flow is escaped as an html entity.There is an [ampersand](http://validator.w3.org/check?uri=http://www.w3.org/&verbose=1) in the URI.This is \*an asterisk which should stay as is.This is * an asterisk which should stay as is.\\   backslash
\   backtick
\*   asterisk
\_   underscore
\{\}  curly braces
\[\]  square brackets
\(\)  parentheses
\#   hash mark
\+   plus sign
\-   minus sign (hyphen)
\.   dot
\!   exclamation mark> # heading level 1
> 
> paragraph>A blockquote with a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.

>and a second very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.>This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a blockquote.> A blockquote
> on multiple lines
> like this.>A blockquote 
>on multiple lines 
>like this. >A blockquote
>on multiple lines
>like this.
>
>But it has
>two paragraphs.>A blockquote
>on multiple lines
>like this> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.
> This is the first level of quoting.
>
> > This is nested blockquote.> This is the first level of quoting.
> > This is nested blockquote.
> Back to the first level.
> This is the first level of quoting.
> > This is nested blockquote.
	10 PRINT HELLO INFINITE
	20 GOTO 10    10 PRINT < > &
    20 GOTO 10    10 PRINT HELLO INFINITE
    20 GOTO 10# Contributing to Mardown Test Suite

1. [Getting Involved](#getting-involved)
2. [Discussion](#discussion)
3. [How To Report an Issue](#how-to-report-an-issue)
4. [Editing Markdown Specification](#editing-markdown-specification)
5. [Test Suite Guidelines](#test-suite-guidelines)
6. [Pull Request Guidelines](#pull-request-guidelines)

## Getting Involved

There are a number of ways to get involved with the development of the Markdown Test Suite. If you are a first time contributor to an open source project, you can still add value to this project. You may identify grammar issues, write prose, examples or documentation for the project. You may flag some errors and open new issues.

Read all bits of this document and that will guide you on how to participate.

## Discussion

### Mailing List

The Markdown Test Suite has been started a little bit after the start of the [Markdown Community Group](http://www.w3.org/community/markdown/). You may want to discuss about Markdown and this project on the [group mailing-list](http://lists.w3.org/Archives/Public/public-markdown/).

## How to Report an Issue

Don't be afraid to add details to your issue. The more context you give, the better for people participating to the project. Make a short summary, add a description with the context and give links to places which will help to understand.

## Editing Markdown Specification

There is much needed work on the [Markdown Specification](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html). It doesn't require strong competences in coding. Be systematic in the markup and follow the way it is already organized. Each time you added a new atomic section, create a commit for this specific part.

## Test Suite Guidelines

When proposing new tests, make sure they do not already exist in the current test suite. You will notice that there is a separate section dedicated to the specific extensions that some markdown generators have created. Keep them separate. We want to keep the core clean and close to the original specification of Markdown.

If you are not sure, create an issue.

### Markdown Extensions

Markdown extension tests are accepted. Use the following rules:

- place all extension tests under the test/extensions/ENGINE directory with filename equal to the feature name
- for each ENGINE and add a README.markdown under the engine directory with a link to its specification

where ENGINE is either of:

- a command line utility. E.g. pandoc, kramdown.
- a programming API. E.g. Redcarpet::Markdown.new().
- a programmatically accessible web service. E.g.: GFM via the GitHub API.
- a non programmatically accessible web service. E.g.: Stack Overflow flavored markdown.

To avoid test duplication for common features, use the following rules:

- if file tests/extensions/ENGINE/FEATURE.md is empty or not present, use tests/extensions/FEATURE.md instead
- if file tests/extensions/ENGINE/FEATURE.out not present, use tests/extensions/FEATURE.out instead
- for a given ENGINE, only features which have either a .md or a .out are implemented by that engine.
- in case of different outputs for a single feature input, keep directly under extensions/ only the output case that happens across the most engines

**version**

Only the latest stable version of each ENGINE is considered.

**options**

The IO behavior tested is for engine defaults, without any options (command line options, extra JSON parameters, etc.) passed to the engine.

**external state**

Tests that use external state not present in the markdown input shall not be included in this test suite.

For example, what GFM @user user tags render to also depends on the state of GitHub's databases (only render to a link if user exists), not only on the input markdown.

#### Examples

GFM and the "fenced code block" use the following file structure:

    tests/extensions/gfm/README.markdown
    tests/extensions/gfm/fenced-code-block.md
    tests/extensions/gfm/fenced-code-block.out

where README.markdown contains:

    https://help.github.com/articles/github-flavored-markdown

To avoid duplication with other engines, if the input / output (normalized to DOM) is the same across multiple engines use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

If the input is the same, and outputs are DOM different, but represent the same idea (e.g. both represent computer code) use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/gfm/fenced-code-block.out
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

#### New Extensions

Tests are modular, and if you want to test a new engine for your project, that should be easy to do.

If you feel that the new engine is reasonably popular, please send a pull request adding it.

## Commits and Pull Requests

* Keep your commits clean and commented
* Do not mix in one commit different things. Keep modifications related.
* Do not mix everything in one giant pull request. Create separate pull requests for different topic. That will help to have a more meaningful debate about the pull requests and will help to review the code.
* If it relates to a specific issue, add the number of the issue in the commit message.

Thanks for Contributing
as*te*risks*single asterisks*_single underscores_HTML entities are written using ampersand notation: &copy;These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

This is an H1
=============# This is an H1 # # This is an H1# this is an h1 with two trailing spaces  
A new paragraph.# This is an H1This is an H2
-------------## This is an H2 #### This is an H2### This is an H3 ###### This is an H3#### This is an H4 ######## This is an H4##### This is an H5 ########## This is an H5###### This is an H6  ############ This is an H6- - ----***___-------![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 for everyone"![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 logo for everyone")![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png)We love <code> and & for everything We love code for everything We love code for everything The MIT License (MIT)

Copyright (c) 2013 Karl Dubost

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
A first sentence  
and a line break.A first sentence     
and a line break.This is an automatic link <http://www.w3.org/>[W3C](http://www.w3.org/ "Discover w3c")[W3C](http://www.w3.org/)[World Wide Web Consortium][w3c]

[w3c]: <http://www.w3.org/>[World Wide Web Consortium][]

[World Wide Web Consortium]: http://www.w3.org/[w3c][]

[w3c]: http://www.w3.org/[World Wide Web Consortium] [w3c]

[w3c]: http://www.w3.org/[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/
   "Discover W3C"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ (Discover w3c)[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ 'Discover w3c'[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ "Discover w3c"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/*   a list containing a blockquote

    > this the blockquote in the list* a

        b
*   a list containing a block of code

	    10 PRINT HELLO INFINITE
	    20 GOTO 10*   This is a list item with two paragraphs. Lorem ipsum dolor
	sit amet, consectetuer adipiscing elit. Aliquam hendrerit
	mi posuere lectus.

	Vestibulum enim wisi, viverra nec, fringilla in, laoreet
	vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
	sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.*   This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.1\. ordered list escape1. 1

    - inner par list

2. 2
1. list item 1
8. list item 2
1. list item 31. list item 1
2. list item 2
3. list item 3This is a paragraph
on multiple lines
with hard return.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line. This is a paragraph with a trailing and leading space. This is a paragraph with 1 trailing tab.	  This is a paragraph with 2 leading spaces.   This is a paragraph with 3 leading spaces. This is a paragraph with 1 leading space.This is a paragraph with a trailing space. # Colophon - October 1st, 2014

This project was initiated to provide a test suite for Markdown markup, and eventually create a specification from this test results. A part of of the community has started a new endeavor which seems to get traction as [CommonMark](https://github.com/jgm/stmd). **We are then closing this project** and encourage you to contribute to CommonMark. 

The most interesting part of this project would not have been possible without the dedication of [Ciro Santilli](https://github.com/cirosantilli) @cirosantilli. So big applause and thank you to him.


The rest is kept around for archives and references.

# Markdown Test Suite

Inspired by questions on [W3C Markdown Community Group](http://www.w3.org/community/markdown).

Pull Requests are welcome. See the [CONTRIBUTING Guidelines](https://github.com/karlcow/markdown-testsuite/blob/master/CONTRIBUTING.md)

## Design goals

- Comprehensive.
- Small modularized tests.
- Easy to run tests using any programming language. In particular, data representations must have an implementation on all major languages.
- Develop a consensus based markdown specification at [markdown-spec.html](markdown-spec.html). Visualize it [here](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html).

## Test Scripts

Markdown Test Suite already includes tests for many important markdown engines.

To see what the scripts do run:

    ./cat-all.py -h
    ./run-tests.py -h

To configure the scripts do:

	cp config_local.py.example config_local.py

and edit config_local.py. It is already gitignored.

A Vagrantfile is provided with a provision script that installs all installable engines.

Sample output from run-tests.py:

    blackfriday   |......FFF..............FF...F....................................F....................................|   0.93s  102    7   6%
	gfm           |FF.....F.....F...FFFF..F....F........................FFFF...FF...............FF...F.......F...........| 262.88s  102   20  19%
    hoedown       |..............................F.................................................F.....................|   0.36s  102    2   1%
	kramdown      |......FFF.....FF.......FF.......FF.FFFFFFFFFFFFF.......................F..............................|  30.69s  102   23  22%
    lunamark      |FFFFFF.F.FFFFFFFFFFFF.F.....FFFF..FF............FFFFF..FFFFFFFFFF..............F...FFFFFFFFFFF........|   1.58s  103   53  51%
    markdown_pl   |.....................FFFF...............................F...............F.............................|   2.56s  102    6   5%
    markdown2     |......................................................................................................|   5.39s  103    0   0%
    marked        |..............F.................FFFFFFFFFFFFFFFF......................F.F.............................|   6.22s  102   19  18%
    maruku        |......FFF......F.......F.FFF...............................................FF.........................|  37.02s  102   10   9%
    md2html       |.........................FFF...F............................................FF........................|   7.42s  102    6   5%
    multimarkdown |......FFF....FF...F............FFF.FFFFFFFFFFFFF.....FFFF.........F...................................|   0.58s  102   27  26%
    pandoc        |FF...........F.F.FFFF..FFFFF....FF.FFFFFFFFFFFFF.....FFFF.....FF............FFF.FFF..................F|   1.11s  102   41  40%
    peg_markdown  |.................................................................F....................................|   0.46s  102    1   0%
    rdiscount     |.......F.........................................................F....................................|  25.19s  102    3   2%
    redcarpet     |......................................................................................................|  21.49s  102    0   0%
    showdown      |.......................................................................F..............................|   6.85s  102    1   0%

	Extensions:

    blackfriday   |F..|  0.04s    3    1  33%
	gfm           |F.|   2.37s    2    1  50%
    hoedown       |.|    0.00s    1    0   0%
    lunamark      |F.F|  0.05s    3    2  66%
    kramdown      |..|   0.62s    2    0   0%
    markdown_pl   ||     0.00s    0    0   0%
    markdown2     |F.|   0.14s    2    1  50%
    marked        |F.|   0.13s    2    1  50%
    maruku        |F..|  1.06s    3    1  33%
    md2html       |F.|   0.14s    2    0   0%
    multimarkdown |F.|   0.01s    2    1  50%
    pandoc        |F.|   0.02s    2    1  50%
    peg_markdown  |...|  0.02s    3    0   0%
    rdiscount     |F..|   0.74s    3    1  33%
    redcarpet     |..|   0.42s    2    0   0%
    showdown      |F..|  0.20s    3    1  33%

Where F indicates a failing test.

## Other Noticeable Test Suites

We haven't been the first test suite effort. Some projects have maintained their own test suite for a long time. Hopefully we can reach a state where people agree on the terms of what should be a good test suite for all developers.

- [Original test suite](http://daringfireball.net/projects/downloads/MarkdownTest_1.0.zip)
- [PHP markdown test suite:](https://github.com/michelf/mdtest/tree/master/Markdown.mdtest)
- [Markdown-js test suite](https://github.com/evilstreak/markdown-js/tree/master/test/features)
- [Python markdown 2 test suite](https://github.com/trentm/python-markdown2/tree/master/test/tm-cases)
- [multimarkdown test suite](https://github.com/fletcher/MMD-Test-Suite)
- [John MacFarlane's Standard Markdown spec](https://github.com/jgm/stmd)

In addition we should note the [wonderful work](http://johnmacfarlane.net/babelmark2/) made by John Mac Farlane. The Web service output the differences in between the different markdown implementations. It helps a lot when searching on the most common output.
as**te**risks**double asterisks**__double underscores__* list item 1
* list item 2
* list item 3
- list item 1
- list item 2
- list item 3 * list item 1
 * list item 2
 * list item 3  * list item 1
  * list item 2
  * list item 3   * list item 1
   * list item 2
   * list item 3+ list item 1
+ list item 2
+ list item 3* list item in paragraph

* another list item in paragraph*   This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a list.
*   and yet another long long long long long long long long long long long long long long long long long long long long long long line.*   This is a list item
    with the content on
    multiline and indented.
*   And this another list item
    with the same principle.€Some text about HTML, SGML and HTML4.

Let's talk about the U.S.A., (É.U. or É.-U. d'A. in French).

*[HTML4]: Hyper Text Markup Language version 4
*[HTML]: Hyper Text Markup Language
*[SGML]: Standard Generalized Markup Language
*[U.S.A.]: United States of America
*[É.U.] : États-Unis d'Amérique
*[É.-U. d'A.] : États-Unis d'Amérique

And here we have a CD, some CDs, and some other CD's.

*[CD]: Compact Disk

Let's transfert documents through TCP/IP, using TCP packets.

*[IP]: Internet Protocol
*[TCP]: Transmission Control Protocol

 ---

Bienvenue sur [CMS](http://www.bidulecms.com "Bidule CMS").

*[CMS]: Content Management System

 ---

ATCCE

*[ATCCE]: Abbreviation "Testing" Correct 'Character' < Escapes >* one
* two

1. three
2. four

* one
* two
1. three
2. fourAT&T has an ampersand in their name.

AT&amp;T is another way to write it.

This & that.

4 < 5.

6 > 5.

Here's a [link] [1] with an ampersand in the URL.

Here's a link with an amersand in the link text: [AT&T] [2].

Here's an inline [link](/script?foo=1&bar=2).

Here's an inline [link](</script?foo=1&bar=2>).


[1]: http://example.com/?foo=1&bar=2
[2]: http://att.com/  "AT&T"Link: <http://example.com/>.

With an ampersand: <http://example.com/?foo=1&bar=2>

* In a list?
* <http://example.com/>
* It should.

> Blockquoted: <http://example.com/>

Auto-links should not occur here: <http://example.com/>

	or here: <http://example.com/>These should all get escaped:

Backslash: \\

Backtick: \

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-



These should not, because they occur within a code block:

	Backslash: \\

	Backtick: \

	Asterisk: \*

	Underscore: \_

	Left brace: \{

	Right brace: \}

	Left bracket: \[

	Right bracket: \]

	Left paren: \(

	Right paren: \)

	Greater-than: \>

	Hash: \#

	Period: \.

	Bang: \!

	Plus: \+

	Minus: \-


Nor should these, which occur in code spans:

Backslash: \\

Backtick:   \  

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-


These should get escaped, even though they're matching pairs for
other Markdown constructs:

\*asterisks\*

\_underscores\_

\backticks\

This is a code span with a literal backslash-backtick sequence:   \  

This is a tag with unescaped backticks <span attr='ticks'>bar</span>.

This is a tag with backslashes <span attr='\\backslashes\\'>bar</span>.
  .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>
 

As above: checking for bad interractions with the HTML block parser:

  html
<div>
 

Some *markdown* formatting.

  html
</div>
 

Some *markdown*

 
<div>
    <html>
 

 
function test();
 

<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">
 
<html>
    <title>
 
</div>

Two code blocks with no blank line between them:

 
<div>
 
 
<div>
 

Testing *confusion* with code spans at the HTML block parser:

 
<div></div>
 

Testing mixing with title code blocks

 
<p>

<p>
 

<p>
 
<p>

 
<Fenced>
 

Code block starting and ending with empty lines:
 


<Fenced>


 

Indented code block containing fenced code block sample:

	 
	<Fenced>
	 

Fenced code block with indented code block sample:

 
Some text

	Indented code block sample code
 

Fenced code block with long markers:

 
Fenced
 

Fenced code block with fenced code block markers of different length in it:

 
In code block
 
Still in code block
 
Still in code block
 

Fenced code block with Markdown header and horizontal rule:

 
#test
---
 

Fenced code block with link definitions, footnote definition and
abbreviation definitions:

 
[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language
 

* In a list item with smalish indent:

   
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
   

With HTML content.

 
<b>bold</b>
 

Bug with block level elements in this case:
 
  <div>
  </div>
 

Indented code block of a fenced code block:

     
	haha!
	 

With class:

 html
<b>bold</b>
 

  html
<b>bold</b>
 

 .html
<b>bold</b>
 

  .html
<b>bold</b>
 

With extra attribute block:

 {.html}
<b>bold</b>
 

  {.html #codeid}
<b>bold</b>
 

  .html{.bold}
<div>
 
  
  .html {#codeid}
</div>
 > Example:
> 
>     sub status {
>         print "working";
>     }
> 
> Or:
> 
>     sub status {
>         return "working";
>     }

*	List Item:

		code block

		with a blank line

	within a list item.

*       code block
        as first element of a list item

*	List Item:
	
		code block with whitespace on preceding line
    Codeblock on second line
    <?php
    echo "hello!";
    ?>

foo bar

    <?php
    echo "hello!";

lorem ipsum

    echo "hello!";
    ?>
    
lorem ipsum	code block on the first line
	
Regular text.

    code block indented by spaces

Regular text.

	the lines in this block  
	all contain trailing spaces  

Regular Text.

	code block on the last line<test a=" content of attribute ">

Fix for backticks within HTML tag: <span attr='ticks'>like this</span>

Here's how you put   backticks   in a code span.A simple definition list:

Term 1
:   Definition 1

Term 2
:   Definition 2

With multiple terms:

Term 1
Term 2
:   Definition 1

Term 3
Term 4
:   Definition 2

With multiple definitions:

Term 1
:   Definition 1
:   Definition 2

Term 2
:   Definition 3
:   Definition 4

With multiple lines per definition:

Term 1
:   Definition 1 line 1 ...
Definition 1 line 2
:   Definition 2 line 1 ...
Definition 2 line 2

Term 2
:   Definition 3 line 2 ...
    Definition 3 line 2
:   Definition 4 line 2 ...
    Definition 4 line 2

With paragraphs:

Term 1

:   Definition 1 (paragraph)

Term 2

:   Definition 2 (paragraph)

With multiple paragraphs:

Term 1

:   Definition 1 paragraph 1 line 1 ...
	Definition 1 paragraph 1 line 2

    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)

    Definition 1 paragraph 2 line 1 ...
Definition 1 paragraph 2 line 2 (lazy)

* * *

A mix:

Term 1
Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)
    
    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

:   Definition 2 paragraph 1 line 1 ...
Definition 2 paragraph 1 line 2 (lazy)

Term 3
:   Definition 3 (no paragraph)
:   Definition 4 (no paragraph)
:   Definition 5 line 1 ...
    Definition 5 line 2 (no paragraph)

:   Definition 6 paragraph 1 line 1 ...
Definition 6 paragraph 1 line 2
:   Definition 7 (no paragraph)
:   Definition 8 paragraph 1 line 1 (forced paragraph) ...
    Definition 8 paragraph 1 line 2
    
    Definition 8 paragraph 2 line 1
    
Term 4
:   Definition 9 paragraph 1 line 1 (forced paragraph) ...
    Definition 9 paragraph 1 line 2
    
    Definition 9 paragraph 2 line 1
:   Definition 10 (no paragraph)

* * *

Special cases:

Term

:       code block
        as first element of a definition<michel.fortin@michelf.ca>

International domain names: <help@tūdaliņ.lv>


## Some weird valid email addresses

<abc.123@example.com>

<1234567890@example.com>

<_______@example.com>

<abc+mailbox/department=shipping@example.com>

<!#$%&'*+-/=?^_.{|}@example.com> (all of these characters are allowed)

<"abc@def"@example.com> (anything goes inside quotation marks)

<"Fred Bloggs"@example.com>

<jsmith@[192.0.2.1]>

<"A"@example.com>Combined emphasis:

1.  ***test test***
2.  ___test test___
3.  *test **test***
4.  **test *test***
5.  ***test* test**
6.  ***test** test*
7.  ***test* test**
8.  **test *test***
9.  *test **test***
10. _test __test___
11. __test _test___
12. ___test_ test__
13. ___test__ test_
14. ___test_ test__
15. __test _test___
16. _test __test___
17. *test __test__*
18. **test _test_**
19. **_test_ test**
20. *__test__ test*
21. **_test_ test**
22. **test _test_**
23. *test __test__*
24. _test **test**_
25. __test *test*__
26. __*test* test__
27. _**test** test_
28. __*test* test__
29. __test *test*__
30. _test **test**_


Incorrect nesting:

1.  *test  **test*  test**
2.  _test  __test_  test__
3.  **test  *test** test*
4.  __test  _test__ test_
5.  *test   *test*  test*
6.  _test   _test_  test_
7.  **test **test** test**
8.  __test __test__ test__
9. _**some text_**
10. *__some text*__
11. **_some text**_
12. *__some text*__

No emphasis:

1.  test*  test  *test
2.  test** test **test
3.  test_  test  _test
4.  test__ test __test



Middle-word emphasis (asterisks):

1.  *a*b
2.   a*b*
3.   a*b*c
4. **a**b
5.   a**b**
6.   a**b**c


Middle-word emphasis (underscore):

1.  _a_b
2.   a_b_
3.   a_b_c
4. __a__b
5.   a__b__
6.   a__b__c

my_precious_file.txt


## Tricky Cases

E**. **Test** TestTestTest

E**. **Test** Test Test Test


## Overlong emphasis

Name: ____________  
Organization: ____  
Region/Country: __

_____Cut here_____

____Cut here____

# Regression

_**Note**_: This _is emphasis_.
With asterisks

 * List item
 *
 * List item

With numbers

1. List item
2.
3. List item

With hyphens

- List item
-
- List item

With asterisks

 * List item
 * List item
 *

With numbers

1. List item
2. List item
3.

With hyphens

- List item
- List item
-
This is the first paragraph.[^first]

[^first]:  This is the first note.

* List item one.[^second]
* List item two.[^third]

[^third]: This is the third note, defined out of order.
[^second]: This is the second note.
[^fourth]: This is the fourth note.

# Header[^fourth]

Some paragraph with a footnote[^1], and another[^2].

[^1]: Content for fifth footnote.
[^2]: Content for sixth footnote spaning on 
    three lines, with some span-level markup like
    _emphasis_, a [link][].

[link]: http://michelf.ca/

Another paragraph with a named footnote[^fn-name].

[^fn-name]:
    Footnote beginning on the line next to the marker.

This paragraph should not have a footnote marker since 
the footnote is undefined.[^3]

This paragraph has a second footnote marker to footnote number one.[^1]

This paragraph links to a footnote with plenty of 
block-level content.[^block]

[^block]:
	Paragraph.
	
	*   List item
	
	> Blockquote
	
	    Code block

This paragraph host the footnote reference within a 
footnote test[^reference].

[^reference]:
	This footnote has a footnote of its own.[^nested]

[^nested]:
	This footnote should appear even though it is referenced
	from another footnote. But [^reference] should be litteral
	since the footnote with that name has already been used.

 - - -

Testing unusual footnote name[^1$^!"'].

[^1$^!"']: Haha!

 - - -
 
Footnotes mixed with images[^image-mixed]
![1800 Travel][img6]
![1830 Travel][img7]

[img6]: images/MGR-1800-travel.jpeg "Travel Speeds in 1800"
[^image-mixed]: Footnote Content
[img7]: images/MGR-1830-travel.jpeg "Travel Speeds in 1830"
In Markdown 1.0.0 and earlier. Version
8. This line turns into a list item.
Because a hard-wrapped line in the
middle of a paragraph looked like a
list item.

Here's one with a bullet.
* criminey.
Header  {#id1}
======

Header  { #id2}
------

### Header  {#id3 }
#### Header ##  { #id4 }

 - - -

Header  {.cl}
======

Header  { .cl}
------

### Header  {.cl }
#### Header ##  { .cl }

 - - -

Header  {.cl.class}
======

Header  { .cl .class}
------

### Header  {.cl .class }
#### Header ##  { .cl.class }

 - - -

Header  {#id5.cl.class}
======

Header  { #id6 .cl .class}
------

### Header  {.cl.class#id7 }
#### Header ##  { .cl.class#id8 }
Header
======

Header
------

### Header

 - - -

Header
======
Paragraph

Header
------
Paragraph

### Header
Paragraph

 - - -

Paragraph
Header
======
Paragraph

Paragraph
Header
------
Paragraph

Paragraph
### Header
ParagraphDashes:

---

 ---
 
  ---

   ---

	---

- - -

 - - -
 
  - - -

   - - -

	- - -


Asterisks:

***

 ***
 
  ***

   ***

	***

* * *

 * * *
 
  * * *

   * * *

	* * *


Underscores:

___

 ___
 
  ___

   ___

    ___

_ _ _

 _ _ _
 
  _ _ _

   _ _ _

    _ _ _
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")

Inline within a paragraph: [alt text](/url/).

![alt text](/url/  "title preceded by two spaces")

![alt text](/url/  "title has spaces afterward"  )

![alt text](</url/>)

![alt text](</url/> "with a title").

![Empty]()

![this is a stupid URL](http://example.com/(parens).jpg)


![alt text][foo]

  [foo]: /url/

![alt text][bar]

  [bar]: /url/ "Title here"Simple block on one line:

<div>foo</div>

And nested without indentation:

<div>
<div>
<div>
foo
</div>
<div style=">"/>
</div>
<div>bar</div>
</div>

And with attributes:

<div>
	<div id="foo">
	</div>
</div>

This was broken in 1.0.2b7:

<div class="inlinepage">
<div class="toggleableend">
foo
</div>
</div>
Here's a simple block:

<div>
	foo
</div>

This should be a code block, though:

	<div>
		foo
	</div>

As should this:

	<div>foo</div>

Now, nested:

<div>
	<div>
		<div>
			foo
		</div>
	</div>
</div>

This should just be an HTML comment:

<!-- Comment -->

Multiline:

<!--
Blah
Blah
-->

Code block:

	<!-- Comment -->

Just plain comment, with trailing spaces on the line:

<!-- foo -->   

Code:

	<hr />
	
Hr's:

<hr>

<hr/>

<hr />

<hr>   

<hr/>  

<hr /> 

<hr class="foo" id="bar" />

<hr class="foo" id="bar"/>

<hr class="foo" id="bar" >

<abbr title=" **Attribute Content Is Not A Code Span** ">ACINACS</abbr>

<abbr title="first backtick!">SB</abbr> 
<abbr title="second backtick!">SB</abbr>Paragraph one.

<!-- This is a simple comment -->

<!--
	This is another comment.
-->

Paragraph two.

<!-- one comment block -- -- with two comments -->

The end.
# Markdown inside code blocks

<div markdown="1">
foo
</div>

<div markdown='1'>
foo
</div>

<div markdown=1>
foo
</div>

<table>
<tr><td markdown="1">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="span">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="block">test _emphasis_ (block)</td></tr>
</table>

## More complicated

<table>
<tr><td markdown="1">
* this is _not_ a list item</td></tr>
<tr><td markdown="span">
* this is _not_ a list item</td></tr>
<tr><td markdown="block">
* this _is_ a list item
</td></tr>
</table>

## With indent

<div>
    <div markdown="1">
    This text is no code block: if it was, the 
    closing <div> would be too and the HTML block 
    would be invalid.

    Markdown content in HTML blocks is assumed to be 
    indented the same as the block opening tag.

    **This should be the third paragraph after the header.**
    </div>
</div>

## Code block with rogue </div>s in Markdown code span and block

<div>
    <div markdown="1">

    This is a code block however:

        </div>

    Funny isn't it? Here is a code span: </div>.

    </div>
</div>

<div>
  <div markdown="1">
    * List item, not a code block

Some text

      This is a code block.
  </div>
</div>

## No code block in markdown span mode

<p markdown="1">
    This is not a code block since Markdown parse paragraph 
    content as span. Code spans like </p> are allowed though.
</p>

<p markdown="1">_Hello_ _world_</p>

## Preserving attributes and tags on more than one line:

<p class="test" markdown="1" 
id="12">
Some _span_ content.
</p>


## Header confusion bug

<table class="canvas">
<tr>
<td id="main" markdown="1">Hello World!
============

Hello World!</td>
</tr>
</table>
Here is a block tag ins:

<ins>
<p>Some text</p>
</ins>

<ins>And here it is inside a paragraph.</ins>

And here it is <ins>in the middle of</ins> a paragraph.

<del>
<p>Some text</p>
</del>

<del>And here is ins as a paragraph.</del>

And here it is <del>in the middle of</del> a paragraph.
		    GNU GENERAL PUBLIC LICENSE
		       Version 2, June 1991

 Copyright (C) 1989, 1991 Free Software Foundation, Inc.,
 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

			    Preamble

  The licenses for most software are designed to take away your
freedom to share and change it.  By contrast, the GNU General Public
License is intended to guarantee your freedom to share and change free
software--to make sure the software is free for all its users.  This
General Public License applies to most of the Free Software
Foundation's software and to any other program whose authors commit to
using it.  (Some other Free Software Foundation software is covered by
the GNU Lesser General Public License instead.)  You can apply it to
your programs, too.

  When we speak of free software, we are referring to freedom, not
price.  Our General Public Licenses are designed to make sure that you
have the freedom to distribute copies of free software (and charge for
this service if you wish), that you receive source code or can get it
if you want it, that you can change the software or use pieces of it
in new free programs; and that you know you can do these things.

  To protect your rights, we need to make restrictions that forbid
anyone to deny you these rights or to ask you to surrender the rights.
These restrictions translate to certain responsibilities for you if you
distribute copies of the software, or if you modify it.

  For example, if you distribute copies of such a program, whether
gratis or for a fee, you must give the recipients all the rights that
you have.  You must make sure that they, too, receive or can get the
source code.  And you must show them these terms so they know their
rights.

  We protect your rights with two steps: (1) copyright the software, and
(2) offer you this license which gives you legal permission to copy,
distribute and/or modify the software.

  Also, for each author's protection and ours, we want to make certain
that everyone understands that there is no warranty for this free
software.  If the software is modified by someone else and passed on, we
want its recipients to know that what they have is not the original, so
that any problems introduced by others will not reflect on the original
authors' reputations.

  Finally, any free program is threatened constantly by software
patents.  We wish to avoid the danger that redistributors of a free
program will individually obtain patent licenses, in effect making the
program proprietary.  To prevent this, we have made it clear that any
patent must be licensed for everyone's free use or not licensed at all.

  The precise terms and conditions for copying, distribution and
modification follow.

		    GNU GENERAL PUBLIC LICENSE
   TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

  0. This License applies to any program or other work which contains
a notice placed by the copyright holder saying it may be distributed
under the terms of this General Public License.  The "Program", below,
refers to any such program or work, and a "work based on the Program"
means either the Program or any derivative work under copyright law:
that is to say, a work containing the Program or a portion of it,
either verbatim or with modifications and/or translated into another
language.  (Hereinafter, translation is included without limitation in
the term "modification".)  Each licensee is addressed as "you".

Activities other than copying, distribution and modification are not
covered by this License; they are outside its scope.  The act of
running the Program is not restricted, and the output from the Program
is covered only if its contents constitute a work based on the
Program (independent of having been made by running the Program).
Whether that is true depends on what the Program does.

  1. You may copy and distribute verbatim copies of the Program's
source code as you receive it, in any medium, provided that you
conspicuously and appropriately publish on each copy an appropriate
copyright notice and disclaimer of warranty; keep intact all the
notices that refer to this License and to the absence of any warranty;
and give any other recipients of the Program a copy of this License
along with the Program.

You may charge a fee for the physical act of transferring a copy, and
you may at your option offer warranty protection in exchange for a fee.

  2. You may modify your copy or copies of the Program or any portion
of it, thus forming a work based on the Program, and copy and
distribute such modifications or work under the terms of Section 1
above, provided that you also meet all of these conditions:

    a) You must cause the modified files to carry prominent notices
    stating that you changed the files and the date of any change.

    b) You must cause any work that you distribute or publish, that in
    whole or in part contains or is derived from the Program or any
    part thereof, to be licensed as a whole at no charge to all third
    parties under the terms of this License.

    c) If the modified program normally reads commands interactively
    when run, you must cause it, when started running for such
    interactive use in the most ordinary way, to print or display an
    announcement including an appropriate copyright notice and a
    notice that there is no warranty (or else, saying that you provide
    a warranty) and that users may redistribute the program under
    these conditions, and telling the user how to view a copy of this
    License.  (Exception: if the Program itself is interactive but
    does not normally print such an announcement, your work based on
    the Program is not required to print an announcement.)

These requirements apply to the modified work as a whole.  If
identifiable sections of that work are not derived from the Program,
and can be reasonably considered independent and separate works in
themselves, then this License, and its terms, do not apply to those
sections when you distribute them as separate works.  But when you
distribute the same sections as part of a whole which is a work based
on the Program, the distribution of the whole must be on the terms of
this License, whose permissions for other licensees extend to the
entire whole, and thus to each and every part regardless of who wrote it.

Thus, it is not the intent of this section to claim rights or contest
your rights to work written entirely by you; rather, the intent is to
exercise the right to control the distribution of derivative or
collective works based on the Program.

In addition, mere aggregation of another work not based on the Program
with the Program (or with a work based on the Program) on a volume of
a storage or distribution medium does not bring the other work under
the scope of this License.

  3. You may copy and distribute the Program (or a work based on it,
under Section 2) in object code or executable form under the terms of
Sections 1 and 2 above provided that you also do one of the following:

    a) Accompany it with the complete corresponding machine-readable
    source code, which must be distributed under the terms of Sections
    1 and 2 above on a medium customarily used for software interchange; or,

    b) Accompany it with a written offer, valid for at least three
    years, to give any third party, for a charge no more than your
    cost of physically performing source distribution, a complete
    machine-readable copy of the corresponding source code, to be
    distributed under the terms of Sections 1 and 2 above on a medium
    customarily used for software interchange; or,

    c) Accompany it with the information you received as to the offer
    to distribute corresponding source code.  (This alternative is
    allowed only for noncommercial distribution and only if you
    received the program in object code or executable form with such
    an offer, in accord with Subsection b above.)

The source code for a work means the preferred form of the work for
making modifications to it.  For an executable work, complete source
code means all the source code for all modules it contains, plus any
associated interface definition files, plus the scripts used to
control compilation and installation of the executable.  However, as a
special exception, the source code distributed need not include
anything that is normally distributed (in either source or binary
form) with the major components (compiler, kernel, and so on) of the
operating system on which the executable runs, unless that component
itself accompanies the executable.

If distribution of executable or object code is made by offering
access to copy from a designated place, then offering equivalent
access to copy the source code from the same place counts as
distribution of the source code, even though third parties are not
compelled to copy the source along with the object code.

  4. You may not copy, modify, sublicense, or distribute the Program
except as expressly provided under this License.  Any attempt
otherwise to copy, modify, sublicense or distribute the Program is
void, and will automatically terminate your rights under this License.
However, parties who have received copies, or rights, from you under
this License will not have their licenses terminated so long as such
parties remain in full compliance.

  5. You are not required to accept this License, since you have not
signed it.  However, nothing else grants you permission to modify or
distribute the Program or its derivative works.  These actions are
prohibited by law if you do not accept this License.  Therefore, by
modifying or distributing the Program (or any work based on the
Program), you indicate your acceptance of this License to do so, and
all its terms and conditions for copying, distributing or modifying
the Program or works based on it.

  6. Each time you redistribute the Program (or any work based on the
Program), the recipient automatically receives a license from the
original licensor to copy, distribute or modify the Program subject to
these terms and conditions.  You may not impose any further
restrictions on the recipients' exercise of the rights granted herein.
You are not responsible for enforcing compliance by third parties to
this License.

  7. If, as a consequence of a court judgment or allegation of patent
infringement or for any other reason (not limited to patent issues),
conditions are imposed on you (whether by court order, agreement or
otherwise) that contradict the conditions of this License, they do not
excuse you from the conditions of this License.  If you cannot
distribute so as to satisfy simultaneously your obligations under this
License and any other pertinent obligations, then as a consequence you
may not distribute the Program at all.  For example, if a patent
license would not permit royalty-free redistribution of the Program by
all those who receive copies directly or indirectly through you, then
the only way you could satisfy both it and this License would be to
refrain entirely from distribution of the Program.

If any portion of this section is held invalid or unenforceable under
any particular circumstance, the balance of the section is intended to
apply and the section as a whole is intended to apply in other
circumstances.

It is not the purpose of this section to induce you to infringe any
patents or other property right claims or to contest validity of any
such claims; this section has the sole purpose of protecting the
integrity of the free software distribution system, which is
implemented by public license practices.  Many people have made
generous contributions to the wide range of software distributed
through that system in reliance on consistent application of that
system; it is up to the author/donor to decide if he or she is willing
to distribute software through any other system and a licensee cannot
impose that choice.

This section is intended to make thoroughly clear what is believed to
be a consequence of the rest of this License.

  8. If the distribution and/or use of the Program is restricted in
certain countries either by patents or by copyrighted interfaces, the
original copyright holder who places the Program under this License
may add an explicit geographical distribution limitation excluding
those countries, so that distribution is permitted only in or among
countries not thus excluded.  In such case, this License incorporates
the limitation as if written in the body of this License.

  9. The Free Software Foundation may publish revised and/or new versions
of the General Public License from time to time.  Such new versions will
be similar in spirit to the present version, but may differ in detail to
address new problems or concerns.

Each version is given a distinguishing version number.  If the Program
specifies a version number of this License which applies to it and "any
later version", you have the option of following the terms and conditions
either of that version or of any later version published by the Free
Software Foundation.  If the Program does not specify a version number of
this License, you may choose any version ever published by the Free Software
Foundation.

  10. If you wish to incorporate parts of the Program into other free
programs whose distribution conditions are different, write to the author
to ask for permission.  For software which is copyrighted by the Free
Software Foundation, write to the Free Software Foundation; we sometimes
make exceptions for this.  Our decision will be guided by the two goals
of preserving the free status of all derivatives of our free software and
of promoting the sharing and reuse of software generally.

			    NO WARRANTY

  11. BECAUSE THE PROGRAM IS LICENSED FREE OF CHARGE, THERE IS NO WARRANTY
FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW.  EXCEPT WHEN
OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES
PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED
OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.  THE ENTIRE RISK AS
TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU.  SHOULD THE
PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING,
REPAIR OR CORRECTION.

  12. IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING
WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MAY MODIFY AND/OR
REDISTRIBUTE THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES,
INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING
OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED
TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY
YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER
PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES.

		     END OF TERMS AND CONDITIONS

	    How to Apply These Terms to Your New Programs

  If you develop a new program, and you want it to be of the greatest
possible use to the public, the best way to achieve this is to make it
free software which everyone can redistribute and change under these terms.

  To do so, attach the following notices to the program.  It is safest
to attach them to the start of each source file to most effectively
convey the exclusion of warranty; and each file should have at least
the "copyright" line and a pointer to where the full notice is found.

    <one line to give the program's name and a brief idea of what it does.>
    Copyright (C) <year>  <name of author>

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

Also add information on how to contact you by electronic and paper mail.

If the program is interactive, make it output a short notice like this
when it starts in an interactive mode:

    Gnomovision version 69, Copyright (C) year name of author
    Gnomovision comes with ABSOLUTELY NO WARRANTY; for details type show w'.
    This is free software, and you are welcome to redistribute it
    under certain conditions; type show c' for details.

The hypothetical commands show w' and show c' should show the appropriate
parts of the General Public License.  Of course, the commands you use may
be called something other than show w' and show c'; they could even be
mouse-clicks or menu items--whatever suits your program.

You should also get your employer (if you work as a programmer) or your
school, if any, to sign a "copyright disclaimer" for the program, if
necessary.  Here is a sample; alter the names:

  Yoyodyne, Inc., hereby disclaims all copyright interest in the program
  Gnomovision' (which makes passes at compilers) written by James Hacker.

  <signature of Ty Coon>, 1 April 1989
  Ty Coon, President of Vice

This General Public License does not permit incorporating your program into
proprietary programs.  If your program is a subroutine library, you may
consider it more useful to permit linking proprietary applications with the
library.  If this is what you want to do, use the GNU Lesser General
Public License instead of this License.
This is an [inline link](/url "title"){.class #inline-link}.

This is a [reference link][refid].

This is an ![inline image](/img "title"){.class #inline-img}.

This is a ![reference image][refid].

[refid]: /path/to/something (Title) { .class #ref data-key=val }

Just a [URL](/url/).

[URL and title](/url/ "title").

[URL and title](/url/  "title preceded by two spaces").

[URL and title](/url/	"title preceded by a tab").

[URL and title](/url/ "title has spaces afterward"  ).

[URL wrapped in angle brackets](</url/>).

[URL w/ angle brackets + title](</url/> "Here's the title").

[Empty]().

[With parens in the URL](http://en.wikipedia.org/wiki/WIMP_(computing))

(With outer parens and [parens in url](/foo(bar)))


[With parens in the URL](/foo(bar) "and a title")

(With outer parens and [parens in url](/foo(bar) "and a title"))
Foo [bar] [1].

Foo [bar][1].

Foo [bar]
[1].

[1]: /url/  "Title"


With [embedded [brackets]] [b].


Indented [once][].

Indented [twice][].

Indented [thrice][].

Indented [four][] times.

 [once]: /url

  [twice]: /url

   [thrice]: /url

    [four]: /url


[b]: /url/

* * *

[this] [this] should work

So should [this][this].

And [this] [].

And [this][].

And [this].

But not [that] [].

Nor [that][].

Nor [that].

[Something in brackets like [this][] should work]

[Same with [this].]

In this case, [this](/somethingelse/) points to something else.

Backslashing should suppress \[this] and [this\].

[this]: foo


* * *

Here's one where the [link
breaks] across lines.

Here's another where the [link 
breaks] across lines, but with a line-ending space.


[link breaks]: /url/
This is the [simple case].

[simple case]: /simple



This one has a [line
break].

This one has a [line 
break] with a line-ending space.

[line break]: /foo


[this] [that] and the [other]

[this]: /this
[that]: /that
[other]: /other
Foo [bar][].

Foo [bar](/url/ "Title with "quotes" inside").


  [bar]: /url/ "Title with "quotes" inside"

Markdown: Basics
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a class="selected" title="Markdown Basics">Basics</a></li>
    <li><a href="/projects/markdown/syntax" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


Getting the Gist of Markdown's Formatting Syntax
------------------------------------------------

This page offers a brief overview of what it's like to use Markdown.
The [syntax page] [s] provides complete, detailed documentation for
every feature, but Markdown should be very easy to pick up simply by
looking at a few examples of it in action. The examples on this page
are written in a before/after style, showing example syntax and the
HTML output produced by Markdown.

It's also helpful to simply try Markdown out; the [Dingus] [d] is a
web application that allows you type your own Markdown-formatted text
and translate it to XHTML.

**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL] [src].

  [s]: /projects/markdown/syntax  "Markdown Syntax"
  [d]: /projects/markdown/dingus  "Markdown Dingus"
  [src]: /projects/markdown/basics.text


## Paragraphs, Headers, Blockquotes ##

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

Markdown offers two styles of headers: *Setext* and *atx*.
Setext-style headers for <h1> and <h2> are created by
"underlining" with equal signs (=) and hyphens (-), respectively.
To create an atx-style header, you put 1-6 hash marks (#) at the
beginning of the line -- the number of hashes equals the resulting
HTML header level.

Blockquotes are indicated using email-style '>' angle brackets.

Markdown:

    A First Level Header
    ====================
    
    A Second Level Header
    ---------------------

    Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.

    The quick brown fox jumped over the lazy
    dog's back.
    
    ### Header 3

    > This is a blockquote.
    > 
    > This is the second paragraph in the blockquote.
    >
    > ## This is an H2 in a blockquote


Output:

    <h1>A First Level Header</h1>
    
    <h2>A Second Level Header</h2>
    
    <p>Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.</p>
    
    <p>The quick brown fox jumped over the lazy
    dog's back.</p>
    
    <h3>Header 3</h3>
    
    <blockquote>
        <p>This is a blockquote.</p>
        
        <p>This is the second paragraph in the blockquote.</p>
        
        <h2>This is an H2 in a blockquote</h2>
    </blockquote>



### Phrase Emphasis ###

Markdown uses asterisks and underscores to indicate spans of emphasis.

Markdown:

    Some of these words *are emphasized*.
    Some of these words _are emphasized also_.
    
    Use two asterisks for **strong emphasis**.
    Or, if you prefer, __use two underscores instead__.

Output:

    <p>Some of these words <em>are emphasized</em>.
    Some of these words <em>are emphasized also</em>.</p>
    
    <p>Use two asterisks for <strong>strong emphasis</strong>.
    Or, if you prefer, <strong>use two underscores instead</strong>.</p>
   


## Lists ##

Unordered (bulleted) lists use asterisks, pluses, and hyphens (*,
+, and -) as list markers. These three markers are
interchangable; this:

    *   Candy.
    *   Gum.
    *   Booze.

this:

    +   Candy.
    +   Gum.
    +   Booze.

and this:

    -   Candy.
    -   Gum.
    -   Booze.

all produce the same output:

    <ul>
    <li>Candy.</li>
    <li>Gum.</li>
    <li>Booze.</li>
    </ul>

Ordered (numbered) lists use regular numbers, followed by periods, as
list markers:

    1.  Red
    2.  Green
    3.  Blue

Output:

    <ol>
    <li>Red</li>
    <li>Green</li>
    <li>Blue</li>
    </ol>

If you put blank lines between items, you'll get <p> tags for the
list item text. You can create multi-paragraph list items by indenting
the paragraphs by 4 spaces or 1 tab:

    *   A list item.
    
        With multiple paragraphs.

    *   Another item in the list.

Output:

    <ul>
    <li><p>A list item.</p>
    <p>With multiple paragraphs.</p></li>
    <li><p>Another item in the list.</p></li>
    </ul>
    


### Links ###

Markdown supports two styles for creating links: *inline* and
*reference*. With both styles, you use square brackets to delimit the
text you want to turn into a link.

Inline-style links use parentheses immediately after the link text.
For example:

    This is an [example link](http://example.com/).

Output:

    <p>This is an <a href="http://example.com/">
    example link</a>.</p>

Optionally, you may include a title attribute in the parentheses:

    This is an [example link](http://example.com/ "With a Title").

Output:

    <p>This is an <a href="http://example.com/" title="With a Title">
    example link</a>.</p>

Reference-style links allow you to refer to your links by names, which
you define elsewhere in your document:

    I get 10 times more traffic from [Google][1] than from
    [Yahoo][2] or [MSN][3].

    [1]: http://google.com/        "Google"
    [2]: http://search.yahoo.com/  "Yahoo Search"
    [3]: http://search.msn.com/    "MSN Search"

Output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from <a href="http://search.yahoo.com/"
    title="Yahoo Search">Yahoo</a> or <a href="http://search.msn.com/"
    title="MSN Search">MSN</a>.</p>

The title attribute is optional. Link names may contain letters,
numbers and spaces, but are *not* case sensitive:

    I start my morning with a cup of coffee and
    [The New York Times][NY Times].

    [ny times]: http://www.nytimes.com/

Output:

    <p>I start my morning with a cup of coffee and
    <a href="http://www.nytimes.com/">The New York Times</a>.</p>


### Images ###

Image syntax is very much like link syntax.

Inline (titles are optional):

    ![alt text](/path/to/img.jpg "Title")

Reference-style:

    ![alt text][id]

    [id]: /path/to/img.jpg "Title"

Both of the above examples produce the same output:

    <img src="/path/to/img.jpg" alt="alt text" title="Title" />



### Code ###

In a regular paragraph, you can create code span by wrapping text in
backtick quotes. Any ampersands (&) and angle brackets (< or
>) will automatically be translated into HTML entities. This makes
it easy to use Markdown to write about HTML example code:

    I strongly recommend against using any <blink> tags.

    I wish SmartyPants used named entities like &mdash;
    instead of decimal-encoded entites like &#8212;.

Output:

    <p>I strongly recommend against using any
    <code>&lt;blink&gt;</code> tags.</p>
    
    <p>I wish SmartyPants used named entities like
    <code>&amp;mdash;</code> instead of decimal-encoded
    entites like <code>&amp;#8212;</code>.</p>


To specify an entire block of pre-formatted code, indent every line of
the block by 4 spaces or 1 tab. Just like with code spans, &, <,
and > characters will be escaped automatically.

Markdown:

    If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:

        <blockquote>
            <p>For example.</p>
        </blockquote>

Output:

    <p>If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:</p>
    
    <pre><code>&lt;blockquote&gt;
        &lt;p&gt;For example.&lt;/p&gt;
    &lt;/blockquote&gt;
    </code></pre>
Markdown: Syntax
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a href="/projects/markdown/basics" title="Markdown Basics">Basics</a></li>
    <li><a class="selected" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


*   [Overview](#overview)
    *   [Philosophy](#philosophy)
    *   [Inline HTML](#html)
    *   [Automatic Escaping for Special Characters](#autoescape)
*   [Block Elements](#block)
    *   [Paragraphs and Line Breaks](#p)
    *   [Headers](#header)
    *   [Blockquotes](#blockquote)
    *   [Lists](#list)
    *   [Code Blocks](#precode)
    *   [Horizontal Rules](#hr)
*   [Span Elements](#span)
    *   [Links](#link)
    *   [Emphasis](#em)
    *   [Code](#code)
    *   [Images](#img)
*   [Miscellaneous](#misc)
    *   [Backslash Escapes](#backslash)
    *   [Automatic Links](#autolink)


**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL][src].

  [src]: /projects/markdown/syntax.text

* * *

<h2 id="overview">Overview</h2>

<h3 id="philosophy">Philosophy</h3>

Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

Readability, however, is emphasized above all else. A Markdown-formatted
document should be publishable as-is, as plain text, without looking
like it's been marked up with tags or formatting instructions. While
Markdown's syntax has been influenced by several existing text-to-HTML
filters -- including [Setext] [1], [atx] [2], [Textile] [3], [reStructuredText] [4],
[Grutatext] [5], and [EtText] [6] -- the single biggest source of
inspiration for Markdown's syntax is the format of plain text email.

  [1]: http://docutils.sourceforge.net/mirror/setext.html
  [2]: http://www.aaronsw.com/2002/atx/
  [3]: http://textism.com/tools/textile/
  [4]: http://docutils.sourceforge.net/rst.html
  [5]: http://www.triptico.com/software/grutatxt.html
  [6]: http://ettext.taint.org/doc/

To this end, Markdown's syntax is comprised entirely of punctuation
characters, which punctuation characters have been carefully chosen so
as to look like what they mean. E.g., asterisks around a word actually
look like \*emphasis\*. Markdown lists look like, well, lists. Even
blockquotes look like quoted passages of text, assuming you've ever
used email.



<h3 id="html">Inline HTML</h3>

Markdown's syntax is intended for one purpose: to be used as a
format for *writing* for the web.

Markdown is not a replacement for HTML, or even close to it. Its
syntax is very small, corresponding only to a very small subset of
HTML tags. The idea is *not* to create a syntax that makes it easier
to insert HTML tags. In my opinion, HTML tags are already easy to
insert. The idea for Markdown is to make it easy to read, write, and
edit prose. HTML is a *publishing* format; Markdown is a *writing*
format. Thus, Markdown's formatting syntax only addresses issues that
can be conveyed in plain text.

For any markup that is not covered by Markdown's syntax, you simply
use HTML itself. There's no need to preface it or delimit it to
indicate that you're switching from Markdown to HTML; you just use
the tags.

The only restrictions are that block-level HTML elements -- e.g. <div>,
<table>, <pre>, <p>, etc. -- must be separated from surrounding
content by blank lines, and the start and end tags of the block should
not be indented with tabs or spaces. Markdown is smart enough not
to add extra (unwanted) <p> tags around HTML block-level tags.

For example, to add an HTML table to a Markdown article:

    This is a regular paragraph.

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    This is another regular paragraph.

Note that Markdown formatting syntax is not processed within block-level
HTML tags. E.g., you can't use Markdown-style *emphasis* inside an
HTML block.

Span-level HTML tags -- e.g. <span>, <cite>, or <del> -- can be
used anywhere in a Markdown paragraph, list item, or header. If you
want, you can even use HTML tags instead of Markdown formatting; e.g. if
you'd prefer to use HTML <a> or <img> tags instead of Markdown's
link or image syntax, go right ahead.

Unlike block-level HTML tags, Markdown syntax *is* processed within
span-level tags.


<h3 id="autoescape">Automatic Escaping for Special Characters</h3>

In HTML, there are two characters that demand special treatment: <
and &. Left angle brackets are used to start tags; ampersands are
used to denote HTML entities. If you want to use them as literal
characters, you must escape them as entities, e.g. &lt;, and
&amp;.

Ampersands in particular are bedeviling for web writers. If you want to
write about 'AT&T', you need to write 'AT&amp;T'. You even need to
escape ampersands within URLs. Thus, if you want to link to:

    http://images.google.com/images?num=30&q=larry+bird

you need to encode the URL as:

    http://images.google.com/images?num=30&amp;q=larry+bird

in your anchor tag href attribute. Needless to say, this is easy to
forget, and is probably the single most common source of HTML validation
errors in otherwise well-marked-up web sites.

Markdown allows you to use these characters naturally, taking care of
all the necessary escaping for you. If you use an ampersand as part of
an HTML entity, it remains unchanged; otherwise it will be translated
into &amp;.

So, if you want to include a copyright symbol in your article, you can write:

    &copy;

and Markdown will leave it alone. But if you write:

    AT&T

Markdown will translate it to:

    AT&amp;T

Similarly, because Markdown supports [inline HTML](#html), if you use
angle brackets as delimiters for HTML tags, Markdown will treat them as
such. But if you write:

    4 < 5

Markdown will translate it to:

    4 &lt; 5

However, inside Markdown code spans and blocks, angle brackets and
ampersands are *always* encoded automatically. This makes it easy to use
Markdown to write about HTML code. (As opposed to raw HTML, which is a
terrible format for writing about HTML syntax, because every single <
and & in your example code needs to be escaped.)


* * *


<h2 id="block">Block Elements</h2>


<h3 id="p">Paragraphs and Line Breaks</h3>

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing but spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

The implication of the "one or more consecutive lines of text" rule is
that Markdown supports "hard-wrapped" text paragraphs. This differs
significantly from most other text-to-HTML formatters (including Movable
Type's "Convert Line Breaks" option) which translate every line break
character in a paragraph into a <br /> tag.

When you *do* want to insert a <br /> break tag using Markdown, you
end a line with two or more spaces, then type return.

Yes, this takes a tad more effort to create a <br />, but a simplistic
"every line break is a <br />" rule wouldn't work for Markdown.
Markdown's email-style [blockquoting][bq] and multi-paragraph [list items][l]
work best -- and look better -- when you format them with hard breaks.

  [bq]: #blockquote
  [l]:  #list



<h3 id="header">Headers</h3>

Markdown supports two styles of headers, [Setext] [1] and [atx] [2].

Setext-style headers are "underlined" using equal signs (for first-level
headers) and dashes (for second-level headers). For example:

    This is an H1
    =============

    This is an H2
    -------------

Any number of underlining ='s or -'s will work.

Atx-style headers use 1-6 hash characters at the start of the line,
corresponding to header levels 1-6. For example:

    # This is an H1

    ## This is an H2

    ###### This is an H6

Optionally, you may "close" atx-style headers. This is purely
cosmetic -- you can use this if you think it looks better. The
closing hashes don't even need to match the number of hashes
used to open the header. (The number of opening hashes
determines the header level.) :

    # This is an H1 #

    ## This is an H2 ##

    ### This is an H3 ######


<h3 id="blockquote">Blockquotes</h3>

Markdown uses email-style > characters for blockquoting. If you're
familiar with quoting passages of text in an email message, then you
know how to create a blockquote in Markdown. It looks best if you hard
wrap the text and put a > before every line:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    > 
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

Markdown allows you to be lazy and only put the > before the first
line of a hard-wrapped paragraph:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

Blockquotes can be nested (i.e. a blockquote-in-a-blockquote) by
adding additional levels of >:

    > This is the first level of quoting.
    >
    > > This is nested blockquote.
    >
    > Back to the first level.

Blockquotes can contain other Markdown elements, including headers, lists,
and code blocks:

	> ## This is a header.
	> 
	> 1.   This is the first list item.
	> 2.   This is the second list item.
	> 
	> Here's some example code:
	> 
	>     return shell_exec("echo $input | $markdown_script");

Any decent text editor should make email-style quoting easy. For
example, with BBEdit, you can make a selection and choose Increase
Quote Level from the Text menu.


<h3 id="list">Lists</h3>

Markdown supports ordered (numbered) and unordered (bulleted) lists.

Unordered lists use asterisks, pluses, and hyphens -- interchangably
-- as list markers:

    *   Red
    *   Green
    *   Blue

is equivalent to:

    +   Red
    +   Green
    +   Blue

and:

    -   Red
    -   Green
    -   Blue

Ordered lists use numbers followed by periods:

    1.  Bird
    2.  McHale
    3.  Parish

It's important to note that the actual numbers you use to mark the
list have no effect on the HTML output Markdown produces. The HTML
Markdown produces from the above list is:

    <ol>
    <li>Bird</li>
    <li>McHale</li>
    <li>Parish</li>
    </ol>

If you instead wrote the list in Markdown like this:

    1.  Bird
    1.  McHale
    1.  Parish

or even:

    3. Bird
    1. McHale
    8. Parish

you'd get the exact same HTML output. The point is, if you want to,
you can use ordinal numbers in your ordered Markdown lists, so that
the numbers in your source match the numbers in your published HTML.
But if you want to be lazy, you don't have to.

If you do use lazy list numbering, however, you should still start the
list with the number 1. At some point in the future, Markdown may support
starting ordered lists at an arbitrary number.

List markers typically start at the left margin, but may be indented by
up to three spaces. List markers must be followed by one or more spaces
or a tab.

To make lists look nice, you can wrap items with hanging indents:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
        Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
        viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
        Suspendisse id sem consectetuer libero luctus adipiscing.

But if you want to be lazy, you don't have to:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.

If list items are separated by blank lines, Markdown will wrap the
items in <p> tags in the HTML output. For example, this input:

    *   Bird
    *   Magic

will turn into:

    <ul>
    <li>Bird</li>
    <li>Magic</li>
    </ul>

But this:

    *   Bird

    *   Magic

will turn into:

    <ul>
    <li><p>Bird</p></li>
    <li><p>Magic</p></li>
    </ul>

List items may consist of multiple paragraphs. Each subsequent
paragraph in a list item must be intended by either 4 spaces
or one tab:

    1.  This is a list item with two paragraphs. Lorem ipsum dolor
        sit amet, consectetuer adipiscing elit. Aliquam hendrerit
        mi posuere lectus.

        Vestibulum enim wisi, viverra nec, fringilla in, laoreet
        vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
        sit amet velit.

    2.  Suspendisse id sem consectetuer libero luctus adipiscing.

It looks nice if you indent every line of the subsequent
paragraphs, but here again, Markdown will allow you to be
lazy:

    *   This is a list item with two paragraphs.

        This is the second paragraph in the list item. You're
    only required to indent the first line. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit.

    *   Another item in the same list.

To put a blockquote within a list item, the blockquote's >
delimiters need to be indented:

    *   A list item with a blockquote:

        > This is a blockquote
        > inside a list item.

To put a code block within a list item, the code block needs
to be indented *twice* -- 8 spaces or two tabs:

    *   A list item with a code block:

            <code goes here>


It's worth noting that it's possible to trigger an ordered list by
accident, by writing something like this:

    1986. What a great season.

In other words, a *number-period-space* sequence at the beginning of a
line. To avoid this, you can backslash-escape the period:

    1986\. What a great season.



<h3 id="precode">Code Blocks</h3>

Pre-formatted code blocks are used for writing about programming or
markup source code. Rather than forming normal paragraphs, the lines
of a code block are interpreted literally. Markdown wraps a code block
in both <pre> and <code> tags.

To produce a code block in Markdown, simply indent every line of the
block by at least 4 spaces or 1 tab. For example, given this input:

    This is a normal paragraph:

        This is a code block.

Markdown will generate:

    <p>This is a normal paragraph:</p>

    <pre><code>This is a code block.
    </code></pre>

One level of indentation -- 4 spaces or 1 tab -- is removed from each
line of the code block. For example, this:

    Here is an example of AppleScript:

        tell application "Foo"
            beep
        end tell

will turn into:

    <p>Here is an example of AppleScript:</p>

    <pre><code>tell application "Foo"
        beep
    end tell
    </code></pre>

A code block continues until it reaches a line that is not indented
(or the end of the article).

Within a code block, ampersands (&) and angle brackets (< and >)
are automatically converted into HTML entities. This makes it very
easy to include example HTML source code using Markdown -- just paste
it and indent it, and Markdown will handle the hassle of encoding the
ampersands and angle brackets. For example, this:

        <div class="footer">
            &copy; 2004 Foo Corporation
        </div>

will turn into:

    <pre><code>&lt;div class="footer"&gt;
        &amp;copy; 2004 Foo Corporation
    &lt;/div&gt;
    </code></pre>

Regular Markdown syntax is not processed within code blocks. E.g.,
asterisks are just literal asterisks within a code block. This means
it's also easy to use Markdown to write about Markdown's own syntax.



<h3 id="hr">Horizontal Rules</h3>

You can produce a horizontal rule tag (<hr />) by placing three or
more hyphens, asterisks, or underscores on a line by themselves. If you
wish, you may use spaces between the hyphens or asterisks. Each of the
following lines will produce a horizontal rule:

    * * *

    ***

    *****
	
    - - -

    ---------------------------------------

	_ _ _


* * *

<h2 id="span">Span Elements</h2>

<h3 id="link">Links</h3>

Markdown supports two style of links: *inline* and *reference*.

In both styles, the link text is delimited by [square brackets].

To create an inline link, use a set of regular parentheses immediately
after the link text's closing square bracket. Inside the parentheses,
put the URL where you want the link to point, along with an *optional*
title for the link, surrounded in quotes. For example:

    This is [an example](http://example.com/ "Title") inline link.

    [This link](http://example.net/) has no title attribute.

Will produce:

    <p>This is <a href="http://example.com/" title="Title">
    an example</a> inline link.</p>

    <p><a href="http://example.net/">This link</a> has no
    title attribute.</p>

If you're referring to a local resource on the same server, you can
use relative paths:

    See my [About](/about/) page for details.

Reference-style links use a second set of square brackets, inside
which you place a label of your choosing to identify the link:

    This is [an example][id] reference-style link.

You can optionally use a space to separate the sets of brackets:

    This is [an example] [id] reference-style link.

Then, anywhere in the document, you define your link label like this,
on a line by itself:

    [id]: http://example.com/  "Optional Title Here"

That is:

*   Square brackets containing the link identifier (optionally
    indented from the left margin using up to three spaces);
*   followed by a colon;
*   followed by one or more spaces (or tabs);
*   followed by the URL for the link;
*   optionally followed by a title attribute for the link, enclosed
    in double or single quotes.

The link URL may, optionally, be surrounded by angle brackets:

    [id]: <http://example.com/>  "Optional Title Here"

You can put the title attribute on the next line and use extra spaces
or tabs for padding, which tends to look better with longer URLs:

    [id]: http://example.com/longish/path/to/resource/here
        "Optional Title Here"

Link definitions are only used for creating links during Markdown
processing, and are stripped from your document in the HTML output.

Link definition names may constist of letters, numbers, spaces, and punctuation -- but they are *not* case sensitive. E.g. these two links:

	[link text][a]
	[link text][A]

are equivalent.

The *implicit link name* shortcut allows you to omit the name of the
link, in which case the link text itself is used as the name.
Just use an empty set of square brackets -- e.g., to link the word
"Google" to the google.com web site, you could simply write:

	[Google][]

And then define the link:

	[Google]: http://google.com/

Because link names may contain spaces, this shortcut even works for
multiple words in the link text:

	Visit [Daring Fireball][] for more information.

And then define the link:
	
	[Daring Fireball]: http://daringfireball.net/

Link definitions can be placed anywhere in your Markdown document. I
tend to put them immediately after each paragraph in which they're
used, but if you want, you can put them all at the end of your
document, sort of like footnotes.

Here's an example of reference links in action:

    I get 10 times more traffic from [Google] [1] than from
    [Yahoo] [2] or [MSN] [3].

      [1]: http://google.com/        "Google"
      [2]: http://search.yahoo.com/  "Yahoo Search"
      [3]: http://search.msn.com/    "MSN Search"

Using the implicit link name shortcut, you could instead write:

    I get 10 times more traffic from [Google][] than from
    [Yahoo][] or [MSN][].

      [google]: http://google.com/        "Google"
      [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
      [msn]:    http://search.msn.com/    "MSN Search"

Both of the above examples will produce the following HTML output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from
    <a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a>
    or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p>

For comparison, here is the same paragraph written using
Markdown's inline link style:

    I get 10 times more traffic from [Google](http://google.com/ "Google")
    than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or
    [MSN](http://search.msn.com/ "MSN Search").

The point of reference-style links is not that they're easier to
write. The point is that with reference-style links, your document
source is vastly more readable. Compare the above examples: using
reference-style links, the paragraph itself is only 81 characters
long; with inline-style links, it's 176 characters; and as raw HTML,
it's 234 characters. In the raw HTML, there's more markup than there
is text.

With Markdown's reference-style links, a source document much more
closely resembles the final output, as rendered in a browser. By
allowing you to move the markup-related metadata out of the paragraph,
you can add links without interrupting the narrative flow of your
prose.


<h3 id="em">Emphasis</h3>

Markdown treats asterisks (*) and underscores (_) as indicators of
emphasis. Text wrapped with one * or _ will be wrapped with an
HTML <em> tag; double *'s or _'s will be wrapped with an HTML
<strong> tag. E.g., this input:

    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__

will produce:

    <em>single asterisks</em>

    <em>single underscores</em>

    <strong>double asterisks</strong>

    <strong>double underscores</strong>

You can use whichever style you prefer; the lone restriction is that
the same character must be used to open and close an emphasis span.

Emphasis can be used in the middle of a word:

    un*fucking*believable

But if you surround an * or _ with spaces, it'll be treated as a
literal asterisk or underscore.

To produce a literal asterisk or underscore at a position where it
would otherwise be used as an emphasis delimiter, you can backslash
escape it:

    \*this text is surrounded by literal asterisks\*



<h3 id="code">Code</h3>

To indicate a span of code, wrap it with backtick quotes (  ).
Unlike a pre-formatted code block, a code span indicates code within a
normal paragraph. For example:

    Use the printf() function.

will produce:

    <p>Use the <code>printf()</code> function.</p>

To include a literal backtick character within a code span, you can use
multiple backticks as the opening and closing delimiters:

     There is a literal backtick () here.

which will produce this:

    <p><code>There is a literal backtick () here.</code></p>

The backtick delimiters surrounding a code span may include spaces --
one after the opening, one before the closing. This allows you to place
literal backtick characters at the beginning or end of a code span:

	A single backtick in a code span:     
	
	A backtick-delimited string in a code span:   foo  

will produce:

	<p>A single backtick in a code span: <code></code></p>
	
	<p>A backtick-delimited string in a code span: <code>foo</code></p>

With a code span, ampersands and angle brackets are encoded as HTML
entities automatically, which makes it easy to include example HTML
tags. Markdown will turn this:

    Please don't use any <blink> tags.

into:

    <p>Please don't use any <code>&lt;blink&gt;</code> tags.</p>

You can write this:

    &#8212; is the decimal-encoded equivalent of &mdash;.

to produce:

    <p><code>&amp;#8212;</code> is the decimal-encoded
    equivalent of <code>&amp;mdash;</code>.</p>



<h3 id="img">Images</h3>

Admittedly, it's fairly difficult to devise a "natural" syntax for
placing images into a plain text document format.

Markdown uses an image syntax that is intended to resemble the syntax
for links, allowing for two styles: *inline* and *reference*.

Inline image syntax looks like this:

    ![Alt text](/path/to/img.jpg)

    ![Alt text](/path/to/img.jpg "Optional title")

That is:

*   An exclamation mark: !;
*   followed by a set of square brackets, containing the alt
    attribute text for the image;
*   followed by a set of parentheses, containing the URL or path to
    the image, and an optional title attribute enclosed in double
    or single quotes.

Reference-style image syntax looks like this:

    ![Alt text][id]

Where "id" is the name of a defined image reference. Image references
are defined using syntax identical to link references:

    [id]: url/to/image  "Optional title attribute"

As of this writing, Markdown has no syntax for specifying the
dimensions of an image; if this is important to you, you can simply
use regular HTML <img> tags.


* * *


<h2 id="misc">Miscellaneous</h2>

<h3 id="autolink">Automatic Links</h3>

Markdown supports a shortcut style for creating "automatic" links for URLs and email addresses: simply surround the URL or email address with angle brackets. What this means is that if you want to show the actual text of a URL or email address, and also have it be a clickable link, you can do this:

    <http://example.com/>
    
Markdown will turn this into:

    <a href="http://example.com/">http://example.com/</a>

Automatic links for email addresses work similarly, except that
Markdown will also perform a bit of randomized decimal and hex
entity-encoding to help obscure your address from address-harvesting
spambots. For example, Markdown will turn this:

    <address@example.com>

into something like this:

    <a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
    &#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
    &#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
    &#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>

which will render in a browser as a clickable link to "address@example.com".

(This sort of entity-encoding trick will indeed fool many, if not
most, address-harvesting bots, but it definitely won't fool all of
them. It's better than nothing, but an address published in this way
will probably eventually start receiving spam.)



<h3 id="backslash">Backslash Escapes</h3>

Markdown allows you to use backslash escapes to generate literal
characters which would otherwise have special meaning in Markdown's
formatting syntax. For example, if you wanted to surround a word with
literal asterisks (instead of an HTML <em> tag), you can backslashes
before the asterisks, like this:

    \*literal asterisks\*

Markdown provides backslash escapes for the following characters:

    \   backslash
       backtick
    *   asterisk
    _   underscore
    {}  curly braces
    []  square brackets
    ()  parentheses
    #   hash mark
	+	plus sign
	-	minus sign (hyphen)
    .   dot
    !   exclamation mark

# Character Escapes

The MD5 value for + is "26b17225b626fb9238849fd60eabdf60".

# HTML Blocks

<p>test</p>

The MD5 value for <p>test</p> is:

6205333b793f34273d75379350b36826* test
+ test
- test

1. test
2. test

* test
+ test
- test

1. test
2. test
> foo
>
> > bar
>
> foo
Valid nesting:

**[Link](url)**

[**Link**](url)

**[**Link**](url)**

Invalid nesting:

[[Link](url)](url)## Unordered

Asterisks tight:

*	asterisk 1
*	asterisk 2
*	asterisk 3


Asterisks loose:

*	asterisk 1

*	asterisk 2

*	asterisk 3

* * *

Pluses tight:

+	Plus 1
+	Plus 2
+	Plus 3


Pluses loose:

+	Plus 1

+	Plus 2

+	Plus 3

* * *


Minuses tight:

-	Minus 1
-	Minus 2
-	Minus 3


Minuses loose:

-	Minus 1

-	Minus 2

-	Minus 3


## Ordered

Tight:

1.	First
2.	Second
3.	Third

and:

1. One
2. Two
3. Three


Loose using tabs:

1.	First

2.	Second

3.	Third

and using spaces:

1. One

2. Two

3. Three

Multiple paragraphs:

1.	Item 1, graf one.

	Item 2. graf two. The quick brown fox jumped over the lazy dog's
	back.
	
2.	Item 2.

3.	Item 3.



## Nested

*	Tab
	*	Tab
		*	Tab

Here's another:

1. First
2. Second:
	* Fee
	* Fie
	* Foe
3. Third

Same thing but with paragraphs:

1. First

2. Second:
	* Fee
	* Fie
	* Foe

3. Third


This was an error in Markdown 1.0.1:

*	this

	*	sub

	that
[Inline link 1 with parens](/url\(test\) "title").

[Inline link 2 with parens](</url\(test\)> "title").

[Inline link 3 with non-escaped parens](/url(test) "title").

[Inline link 4 with non-escaped parens](</url(test)> "title").

[Reference link 1 with parens][1].

[Reference link 2 with parens][2].

  [1]: /url(test) "title"
  [2]: </url(test)> "title"
This tests for a bug where quotes escaped by PHP when using 
preg_replace with the /e modifier must be correctly unescaped
(hence the _UnslashQuotes function found only in PHP Markdown).



Headers below should appear exactly as they are typed (no backslash
added or removed).

Header "quoted\" again \\""
===========================

Header "quoted\" again \\""
---------------------------

### Header "quoted\" again \\"" ###



Test with tabs for _Detab:

	Code	'block'	with	some	"tabs"	and	"quotes"
[Test](/"style="color:red)
[Test](/'style='color:red)

![](/"style="border-color:red;border-size:1px;border-style:solid)
![](/'style='border-color:red;border-size:1px;border-style:solid)
***This is strong and em.***

So is ***this*** word.

___This is strong and em.___

So is ___this___ word.
# Simple tables

Header 1  | Header 2
--------- | ---------
Cell 1    | Cell 2
Cell 3    | Cell 4

With leading pipes:

| Header 1  | Header 2
| --------- | ---------
| Cell 1    | Cell 2
| Cell 3    | Cell 4

With tailing pipes:

Header 1  | Header 2  |
--------- | --------- |
Cell 1    | Cell 2    |
Cell 3    | Cell 4    |

With leading and tailing pipes:

| Header 1  | Header 2  |
| --------- | --------- |
| Cell 1    | Cell 2    |
| Cell 3    | Cell 4    |

* * *

# One-column one-row table

With leading pipes:

| Header
| -------
| Cell

With tailing pipes:

Header  |
------- |
Cell    |

With leading and tailing pipes:

| Header  |
| ------- |
| Cell    |

* * *

Table alignement:

| Default   | Right     |  Center   |     Left  |
| --------- |:--------- |:---------:| ---------:|
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

Table alignement (alternate spacing):

| Default   | Right     |  Center   |     Left  |
| --------- | :-------- | :-------: | --------: |
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

* * * 

# Empty cells

| Header 1  | Header 2  |
| --------- | --------- |
| A         | B         |
| C         |           |

Header 1  | Header 2
--------- | ---------
A         | B
          | D

* * *

# Missing tailing pipe

Header 1  | Header 2  
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- 
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      

* * *

# Too many pipes in rows

| Header 1  | Header 2  |
| --------- 
| Cell      | Cell      | Extra cell? |
| Cell      | Cell      | Extra cell? |

+	this is a list item
	indented with tabs

+   this is a list item
    indented with spaces

Code:

	this code block is indented by one tab

And:

		this code block is indented by two tabs

And:

	+	this is an example list item
		indented with tabs
	
	+   this is an example list item
	    indented with spaces
> A list within a blockquote:
> 
> *	asterisk 1
> *	asterisk 2
> *	asterisk 3
Paragraph and no space:
* ciao

Paragraph and 1 space:
 * ciao

Paragraph and 3 spaces:
  * ciao

Paragraph and 4 spaces:
   * ciao

Paragraph before header:
#Header

Paragraph before blockquote:
>Some quote.
 .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>


As above: checking for bad interractions with the HTML block parser:

 html
<div>


Some *markdown* formatting.

 html
</div>


Some *markdown*


<div>
    <html>



function test();


<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">

<html>
    <title>

</div>

Two code blocks with no blank line between them:


<div>


<div>


Testing *confusion* with markers in the middle:


<div></div>


Testing mixing with title code blocks


<p>
 
<p>

 
<p>

<p>
 

<Fenced>


Code block starting and ending with empty lines:



<Fenced>




Indented code block containing fenced code block sample:

	
	<Fenced>
	

Fenced code block with indented code block sample:


Some text

	Indented code block sample code


Fenced code block with long markers:


Fenced


Fenced code block with fenced code block markers of different length in it:


In code block

Still in code block

Still in code block


Fenced code block with Markdown header and horizontal rule:


#test
---


Fenced code block with link definitions, footnote definition and 
abbreviation definitions:


[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language


* In a list item with smalish indent:

  
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
  
  
With HTML content.
  

<b>bold</b>


Bug with block level elements in this case:

  <div>
  </div>


Indented code block of a fenced code block:

    
	haha!
	

With class:
  
html
<b>bold</b>

  
 html
<b>bold</b>

  
.html
<b>bold</b>

  
 .html
<b>bold</b>


With extra attribute block:

{.html}
<b>bold</b>

  
 {.html #codeid}
<b>bold</b>


 .html{.bold}
<div>

  
 .html {#codeid}
</div>
First line. <br/>
Second line.

This is a first paragraph,
on multiple lines.
     
This is a second paragraph.
There are spaces in between the two.This is a first paragraph,
on multiple lines.

This is a second paragraph
which has multiple lines too.A first paragraph.



A second paragraph after 3 CR (carriage return).This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
     
A few spaces and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
	
1 tab to separate them and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.

A new long long long long long long long long long long long long long long long long paragraph on 1 line.An ampersand & in the text flow is escaped as an html entity.There is an [ampersand](http://validator.w3.org/check?uri=http://www.w3.org/&verbose=1) in the URI.This is \*an asterisk which should stay as is.This is * an asterisk which should stay as is.\\   backslash
\   backtick
\*   asterisk
\_   underscore
\{\}  curly braces
\[\]  square brackets
\(\)  parentheses
\#   hash mark
\+   plus sign
\-   minus sign (hyphen)
\.   dot
\!   exclamation mark> # heading level 1
> 
> paragraph>A blockquote with a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.

>and a second very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.>This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a blockquote.> A blockquote
> on multiple lines
> like this.>A blockquote 
>on multiple lines 
>like this. >A blockquote
>on multiple lines
>like this.
>
>But it has
>two paragraphs.>A blockquote
>on multiple lines
>like this> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.
> This is the first level of quoting.
>
> > This is nested blockquote.> This is the first level of quoting.
> > This is nested blockquote.
> Back to the first level.
> This is the first level of quoting.
> > This is nested blockquote.
	10 PRINT HELLO INFINITE
	20 GOTO 10    10 PRINT < > &
    20 GOTO 10    10 PRINT HELLO INFINITE
    20 GOTO 10# Contributing to Mardown Test Suite

1. [Getting Involved](#getting-involved)
2. [Discussion](#discussion)
3. [How To Report an Issue](#how-to-report-an-issue)
4. [Editing Markdown Specification](#editing-markdown-specification)
5. [Test Suite Guidelines](#test-suite-guidelines)
6. [Pull Request Guidelines](#pull-request-guidelines)

## Getting Involved

There are a number of ways to get involved with the development of the Markdown Test Suite. If you are a first time contributor to an open source project, you can still add value to this project. You may identify grammar issues, write prose, examples or documentation for the project. You may flag some errors and open new issues.

Read all bits of this document and that will guide you on how to participate.

## Discussion

### Mailing List

The Markdown Test Suite has been started a little bit after the start of the [Markdown Community Group](http://www.w3.org/community/markdown/). You may want to discuss about Markdown and this project on the [group mailing-list](http://lists.w3.org/Archives/Public/public-markdown/).

## How to Report an Issue

Don't be afraid to add details to your issue. The more context you give, the better for people participating to the project. Make a short summary, add a description with the context and give links to places which will help to understand.

## Editing Markdown Specification

There is much needed work on the [Markdown Specification](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html). It doesn't require strong competences in coding. Be systematic in the markup and follow the way it is already organized. Each time you added a new atomic section, create a commit for this specific part.

## Test Suite Guidelines

When proposing new tests, make sure they do not already exist in the current test suite. You will notice that there is a separate section dedicated to the specific extensions that some markdown generators have created. Keep them separate. We want to keep the core clean and close to the original specification of Markdown.

If you are not sure, create an issue.

### Markdown Extensions

Markdown extension tests are accepted. Use the following rules:

- place all extension tests under the test/extensions/ENGINE directory with filename equal to the feature name
- for each ENGINE and add a README.markdown under the engine directory with a link to its specification

where ENGINE is either of:

- a command line utility. E.g. pandoc, kramdown.
- a programming API. E.g. Redcarpet::Markdown.new().
- a programmatically accessible web service. E.g.: GFM via the GitHub API.
- a non programmatically accessible web service. E.g.: Stack Overflow flavored markdown.

To avoid test duplication for common features, use the following rules:

- if file tests/extensions/ENGINE/FEATURE.md is empty or not present, use tests/extensions/FEATURE.md instead
- if file tests/extensions/ENGINE/FEATURE.out not present, use tests/extensions/FEATURE.out instead
- for a given ENGINE, only features which have either a .md or a .out are implemented by that engine.
- in case of different outputs for a single feature input, keep directly under extensions/ only the output case that happens across the most engines

**version**

Only the latest stable version of each ENGINE is considered.

**options**

The IO behavior tested is for engine defaults, without any options (command line options, extra JSON parameters, etc.) passed to the engine.

**external state**

Tests that use external state not present in the markdown input shall not be included in this test suite.

For example, what GFM @user user tags render to also depends on the state of GitHub's databases (only render to a link if user exists), not only on the input markdown.

#### Examples

GFM and the "fenced code block" use the following file structure:

    tests/extensions/gfm/README.markdown
    tests/extensions/gfm/fenced-code-block.md
    tests/extensions/gfm/fenced-code-block.out

where README.markdown contains:

    https://help.github.com/articles/github-flavored-markdown

To avoid duplication with other engines, if the input / output (normalized to DOM) is the same across multiple engines use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

If the input is the same, and outputs are DOM different, but represent the same idea (e.g. both represent computer code) use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/gfm/fenced-code-block.out
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

#### New Extensions

Tests are modular, and if you want to test a new engine for your project, that should be easy to do.

If you feel that the new engine is reasonably popular, please send a pull request adding it.

## Commits and Pull Requests

* Keep your commits clean and commented
* Do not mix in one commit different things. Keep modifications related.
* Do not mix everything in one giant pull request. Create separate pull requests for different topic. That will help to have a more meaningful debate about the pull requests and will help to review the code.
* If it relates to a specific issue, add the number of the issue in the commit message.

Thanks for Contributing
as*te*risks*single asterisks*_single underscores_HTML entities are written using ampersand notation: &copy;These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

This is an H1
=============# This is an H1 # # This is an H1# this is an h1 with two trailing spaces  
A new paragraph.# This is an H1This is an H2
-------------## This is an H2 #### This is an H2### This is an H3 ###### This is an H3#### This is an H4 ######## This is an H4##### This is an H5 ########## This is an H5###### This is an H6  ############ This is an H6- - ----***___-------![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 for everyone"![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 logo for everyone")![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png)We love <code> and & for everything We love code for everything We love code for everything The MIT License (MIT)

Copyright (c) 2013 Karl Dubost

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
A first sentence  
and a line break.A first sentence     
and a line break.This is an automatic link <http://www.w3.org/>[W3C](http://www.w3.org/ "Discover w3c")[W3C](http://www.w3.org/)[World Wide Web Consortium][w3c]

[w3c]: <http://www.w3.org/>[World Wide Web Consortium][]

[World Wide Web Consortium]: http://www.w3.org/[w3c][]

[w3c]: http://www.w3.org/[World Wide Web Consortium] [w3c]

[w3c]: http://www.w3.org/[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/
   "Discover W3C"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ (Discover w3c)[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ 'Discover w3c'[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ "Discover w3c"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/*   a list containing a blockquote

    > this the blockquote in the list* a

        b
*   a list containing a block of code

	    10 PRINT HELLO INFINITE
	    20 GOTO 10*   This is a list item with two paragraphs. Lorem ipsum dolor
	sit amet, consectetuer adipiscing elit. Aliquam hendrerit
	mi posuere lectus.

	Vestibulum enim wisi, viverra nec, fringilla in, laoreet
	vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
	sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.*   This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.1\. ordered list escape1. 1

    - inner par list

2. 2
1. list item 1
8. list item 2
1. list item 31. list item 1
2. list item 2
3. list item 3This is a paragraph
on multiple lines
with hard return.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line. This is a paragraph with a trailing and leading space. This is a paragraph with 1 trailing tab.	  This is a paragraph with 2 leading spaces.   This is a paragraph with 3 leading spaces. This is a paragraph with 1 leading space.This is a paragraph with a trailing space. # Colophon - October 1st, 2014

This project was initiated to provide a test suite for Markdown markup, and eventually create a specification from this test results. A part of of the community has started a new endeavor which seems to get traction as [CommonMark](https://github.com/jgm/stmd). **We are then closing this project** and encourage you to contribute to CommonMark. 

The most interesting part of this project would not have been possible without the dedication of [Ciro Santilli](https://github.com/cirosantilli) @cirosantilli. So big applause and thank you to him.


The rest is kept around for archives and references.

# Markdown Test Suite

Inspired by questions on [W3C Markdown Community Group](http://www.w3.org/community/markdown).

Pull Requests are welcome. See the [CONTRIBUTING Guidelines](https://github.com/karlcow/markdown-testsuite/blob/master/CONTRIBUTING.md)

## Design goals

- Comprehensive.
- Small modularized tests.
- Easy to run tests using any programming language. In particular, data representations must have an implementation on all major languages.
- Develop a consensus based markdown specification at [markdown-spec.html](markdown-spec.html). Visualize it [here](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html).

## Test Scripts

Markdown Test Suite already includes tests for many important markdown engines.

To see what the scripts do run:

    ./cat-all.py -h
    ./run-tests.py -h

To configure the scripts do:

	cp config_local.py.example config_local.py

and edit config_local.py. It is already gitignored.

A Vagrantfile is provided with a provision script that installs all installable engines.

Sample output from run-tests.py:

    blackfriday   |......FFF..............FF...F....................................F....................................|   0.93s  102    7   6%
	gfm           |FF.....F.....F...FFFF..F....F........................FFFF...FF...............FF...F.......F...........| 262.88s  102   20  19%
    hoedown       |..............................F.................................................F.....................|   0.36s  102    2   1%
	kramdown      |......FFF.....FF.......FF.......FF.FFFFFFFFFFFFF.......................F..............................|  30.69s  102   23  22%
    lunamark      |FFFFFF.F.FFFFFFFFFFFF.F.....FFFF..FF............FFFFF..FFFFFFFFFF..............F...FFFFFFFFFFF........|   1.58s  103   53  51%
    markdown_pl   |.....................FFFF...............................F...............F.............................|   2.56s  102    6   5%
    markdown2     |......................................................................................................|   5.39s  103    0   0%
    marked        |..............F.................FFFFFFFFFFFFFFFF......................F.F.............................|   6.22s  102   19  18%
    maruku        |......FFF......F.......F.FFF...............................................FF.........................|  37.02s  102   10   9%
    md2html       |.........................FFF...F............................................FF........................|   7.42s  102    6   5%
    multimarkdown |......FFF....FF...F............FFF.FFFFFFFFFFFFF.....FFFF.........F...................................|   0.58s  102   27  26%
    pandoc        |FF...........F.F.FFFF..FFFFF....FF.FFFFFFFFFFFFF.....FFFF.....FF............FFF.FFF..................F|   1.11s  102   41  40%
    peg_markdown  |.................................................................F....................................|   0.46s  102    1   0%
    rdiscount     |.......F.........................................................F....................................|  25.19s  102    3   2%
    redcarpet     |......................................................................................................|  21.49s  102    0   0%
    showdown      |.......................................................................F..............................|   6.85s  102    1   0%

	Extensions:

    blackfriday   |F..|  0.04s    3    1  33%
	gfm           |F.|   2.37s    2    1  50%
    hoedown       |.|    0.00s    1    0   0%
    lunamark      |F.F|  0.05s    3    2  66%
    kramdown      |..|   0.62s    2    0   0%
    markdown_pl   ||     0.00s    0    0   0%
    markdown2     |F.|   0.14s    2    1  50%
    marked        |F.|   0.13s    2    1  50%
    maruku        |F..|  1.06s    3    1  33%
    md2html       |F.|   0.14s    2    0   0%
    multimarkdown |F.|   0.01s    2    1  50%
    pandoc        |F.|   0.02s    2    1  50%
    peg_markdown  |...|  0.02s    3    0   0%
    rdiscount     |F..|   0.74s    3    1  33%
    redcarpet     |..|   0.42s    2    0   0%
    showdown      |F..|  0.20s    3    1  33%

Where F indicates a failing test.

## Other Noticeable Test Suites

We hav en't been the first test suite effort. Some projects have maintained their own test suite for a long time. Hopefully we can reach a state where people agree on the terms of what should be a good test suite for all developers.

- [Original test suite](http://daringfireball.net/projects/downloads/MarkdownTest_1.0.zip)
- [PHP markdown test suite:](https://github.com/michelf/mdtest/tree/master/Markdown.mdtest)
- [Markdown-js test suite](https://github.com/evilstreak/markdown-js/tree/master/test/features)
- [Python markdown 2 test suite](https://github.com/trentm/python-markdown2/tree/master/test/tm-cases)
- [multimarkdown test suite](https://github.com/fletcher/MMD-Test-Suite)
- [John MacFarlane's Standard Markdown spec](https://github.com/jgm/stmd)

In addition we should note the [wonderful work](http://johnmacfarlane.net/babelmark2/) made by John Mac Farlane. The Web service output the differences in between the different markdown implementations. It helps a lot when searching on the most common output.
as**te**risks**double asterisks**__double underscores__* list item 1
* list item 2
* list item 3
- list item 1
- list item 2
- list item 3 * list item 1
 * list item 2
 * list item 3  * list item 1
  * list item 2
  * list item 3   * list item 1
   * list item 2
   * list item 3+ list item 1
+ list item 2
+ list item 3* list item in paragraph

* another list item in paragraph*   This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a list.
*   and yet another long long long long long long long long long long long long long long long long long long long long long long line.*   This is a list item
    with the content on
    multiline and indented.
*   And this another list item
    with the same principle.€Some text about HTML, SGML and HTML4.

Let's talk about the U.S.A., (É.U. or É.-U. d'A. in French).

*[HTML4]: Hyper Text Markup Language version 4
*[HTML]: Hyper Text Markup Language
*[SGML]: Standard Generalized Markup Language
*[U.S.A.]: United States of America
*[É.U.] : États-Unis d'Amérique
*[É.-U. d'A.] : États-Unis d'Amérique

And here we have a CD, some CDs, and some other CD's.

*[CD]: Compact Disk

Let's transfert documents through TCP/IP, using TCP packets.

*[IP]: Internet Protocol
*[TCP]: Transmission Control Protocol

 ---

Bienvenue sur [CMS](http://www.bidulecms.com "Bidule CMS").

*[CMS]: Content Management System

 ---

ATCCE

*[ATCCE]: Abbreviation "Testing" Correct 'Character' < Escapes >* one
* two

1. three
2. four

* one
* two
1. three
2. fourAT&T has an ampersand in their name.

AT&amp;T is another way to write it.

This & that.

4 < 5.

6 > 5.

Here's a [link] [1] with an ampersand in the URL.

Here's a link with an amersand in the link text: [AT&T] [2].

Here's an inline [link](/script?foo=1&bar=2).

Here's an inline [link](</script?foo=1&bar=2>).


[1]: http://example.com/?foo=1&bar=2
[2]: http://att.com/  "AT&T"Link: <http://example.com/>.

With an ampersand: <http://example.com/?foo=1&bar=2>

* In a list?
* <http://example.com/>
* It should.

> Blockquoted: <http://example.com/>

Auto-links should not occur here: <http://example.com/>

	or here: <http://example.com/>These should all get escaped:

Backslash: \\

Backtick: \

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-



These should not, because they occur within a code block:

	Backslash: \\

	Backtick: \

	Asterisk: \*

	Underscore: \_

	Left brace: \{

	Right brace: \}

	Left bracket: \[

	Right bracket: \]

	Left paren: \(

	Right paren: \)

	Greater-than: \>

	Hash: \#

	Period: \.

	Bang: \!

	Plus: \+

	Minus: \-


Nor should these, which occur in code spans:

Backslash: \\

Backtick:   \  

Asterisk: \*

Underscore: \_

Left brace: \{

Right brace: \}

Left bracket: \[

Right bracket: \]

Left paren: \(

Right paren: \)

Greater-than: \>

Hash: \#

Period: \.

Bang: \!

Plus: \+

Minus: \-


These should get escaped, even though they're matching pairs for
other Markdown constructs:

\*asterisks\*

\_underscores\_

\backticks\

This is a code span with a literal backslash-backtick sequence:   \  

This is a tag with unescaped backticks <span attr='ticks'>bar</span>.

This is a tag with backslashes <span attr='\\backslashes\\'>bar</span>.
  .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>
 

As above: checking for bad interractions with the HTML block parser:

  html
<div>
 

Some *markdown* formatting.

  html
</div>
 

Some *markdown*

 
<div>
    <html>
 

 
function test();
 

<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">
 
<html>
    <title>
 
</div>

Two code blocks with no blank line between them:

 
<div>
 
 
<div>
 

Testing *confusion* with code spans at the HTML block parser:

 
<div></div>
 

Testing mixing with title code blocks

 
<p>

<p>
 

<p>
 
<p>

 
<Fenced>
 

Code block starting and ending with empty lines:
 


<Fenced>


 

Indented code block containing fenced code block sample:

	 
	<Fenced>
	 

Fenced code block with indented code block sample:

 
Some text

	Indented code block sample code
 

Fenced code block with long markers:

 
Fenced
 

Fenced code block with fenced code block markers of different length in it:

 
In code block
 
Still in code block
 
Still in code block
 

Fenced code block with Markdown header and horizontal rule:

 
#test
---
 

Fenced code block with link definitions, footnote definition and
abbreviation definitions:

 
[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language
 

* In a list item with smalish indent:

   
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
   

With HTML content.

 
<b>bold</b>
 

Bug with block level elements in this case:
 
  <div>
  </div>
 

Indented code block of a fenced code block:

     
	haha!
	 

With class:

 html
<b>bold</b>
 

  html
<b>bold</b>
 

 .html
<b>bold</b>
 

  .html
<b>bold</b>
 

With extra attribute block:

 {.html}
<b>bold</b>
 

  {.html #codeid}
<b>bold</b>
 

  .html{.bold}
<div>
 
  
  .html {#codeid}
</div>
 > Example:
> 
>     sub status {
>         print "working";
>     }
> 
> Or:
> 
>     sub status {
>         return "working";
>     }

*	List Item:

		code block

		with a blank line

	within a list item.

*       code block
        as first element of a list item

*	List Item:
	
		code block with whitespace on preceding line
    Codeblock on second line
    <?php
    echo "hello!";
    ?>

foo bar

    <?php
    echo "hello!";

lorem ipsum

    echo "hello!";
    ?>
    
lorem ipsum	code block on the first line
	
Regular text.

    code block indented by spaces

Regular text.

	the lines in this block  
	all contain trailing spaces  

Regular Text.

	code block on the last line<test a=" content of attribute ">

Fix for backticks within HTML tag: <span attr='ticks'>like this</span>

Here's how you put   backticks   in a code span.A simple definition list:

Term 1
:   Definition 1

Term 2
:   Definition 2

With multiple terms:

Term 1
Term 2
:   Definition 1

Term 3
Term 4
:   Definition 2

With multiple definitions:

Term 1
:   Definition 1
:   Definition 2

Term 2
:   Definition 3
:   Definition 4

With multiple lines per definition:

Term 1
:   Definition 1 line 1 ...
Definition 1 line 2
:   Definition 2 line 1 ...
Definition 2 line 2

Term 2
:   Definition 3 line 2 ...
    Definition 3 line 2
:   Definition 4 line 2 ...
    Definition 4 line 2

With paragraphs:

Term 1

:   Definition 1 (paragraph)

Term 2

:   Definition 2 (paragraph)

With multiple paragraphs:

Term 1

:   Definition 1 paragraph 1 line 1 ...
	Definition 1 paragraph 1 line 2

    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)

    Definition 1 paragraph 2 line 1 ...
Definition 1 paragraph 2 line 2 (lazy)

* * *

A mix:

Term 1
Term 2

:   Definition 1 paragraph 1 line 1 ...
Definition 1 paragraph 1 line 2 (lazy)
    
    Definition 1 paragraph 2 line 1 ...
    Definition 1 paragraph 2 line 2

:   Definition 2 paragraph 1 line 1 ...
Definition 2 paragraph 1 line 2 (lazy)

Term 3
:   Definition 3 (no paragraph)
:   Definition 4 (no paragraph)
:   Definition 5 line 1 ...
    Definition 5 line 2 (no paragraph)

:   Definition 6 paragraph 1 line 1 ...
Definition 6 paragraph 1 line 2
:   Definition 7 (no paragraph)
:   Definition 8 paragraph 1 line 1 (forced paragraph) ...
    Definition 8 paragraph 1 line 2
    
    Definition 8 paragraph 2 line 1
    
Term 4
:   Definition 9 paragraph 1 line 1 (forced paragraph) ...
    Definition 9 paragraph 1 line 2
    
    Definition 9 paragraph 2 line 1
:   Definition 10 (no paragraph)

* * *

Special cases:

Term

:       code block
        as first element of a definition<michel.fortin@michelf.ca>

International domain names: <help@tūdaliņ.lv>


## Some weird valid email addresses

<abc.123@example.com>

<1234567890@example.com>

<_______@example.com>

<abc+mailbox/department=shipping@example.com>

<!#$%&'*+-/=?^_.{|}@example.com> (all of these characters are allowed)

<"abc@def"@example.com> (anything goes inside quotation marks)

<"Fred Bloggs"@example.com>

<jsmith@[192.0.2.1]>

<"A"@example.com>Combined emphasis:

1.  ***test test***
2.  ___test test___
3.  *test **test***
4.  **test *test***
5.  ***test* test**
6.  ***test** test*
7.  ***test* test**
8.  **test *test***
9.  *test **test***
10. _test __test___
11. __test _test___
12. ___test_ test__
13. ___test__ test_
14. ___test_ test__
15. __test _test___
16. _test __test___
17. *test __test__*
18. **test _test_**
19. **_test_ test**
20. *__test__ test*
21. **_test_ test**
22. **test _test_**
23. *test __test__*
24. _test **test**_
25. __test *test*__
26. __*test* test__
27. _**test** test_
28. __*test* test__
29. __test *test*__
30. _test **test**_


Incorrect nesting:

1.  *test  **test*  test**
2.  _test  __test_  test__
3.  **test  *test** test*
4.  __test  _test__ test_
5.  *test   *test*  test*
6.  _test   _test_  test_
7.  **test **test** test**
8.  __test __test__ test__
9. _**some text_**
10. *__some text*__
11. **_some text**_
12. *__some text*__

No emphasis:

1.  test*  test  *test
2.  test** test **test
3.  test_  test  _test
4.  test__ test __test



Middle-word emphasis (asterisks):

1.  *a*b
2.   a*b*
3.   a*b*c
4. **a**b
5.   a**b**
6.   a**b**c


Middle-word emphasis (underscore):

1.  _a_b
2.   a_b_
3.   a_b_c
4. __a__b
5.   a__b__
6.   a__b__c

my_precious_file.txt


## Tricky Cases

E**. **Test** TestTestTest

E**. **Test** Test Test Test


## Overlong emphasis

Name: ____________  
Organization: ____  
Region/Country: __

_____Cut here_____

____Cut here____

# Regression

_**Note**_: This _is emphasis_.
With asterisks

 * List item
 *
 * List item

With numbers

1. List item
2.
3. List item

With hyphens

- List item
-
- List item

With asterisks

 * List item
 * List item
 *

With numbers

1. List item
2. List item
3.

With hyphens

- List item
- List item
-
This is the first paragraph.[^first]

[^first]:  This is the first note.

* List item one.[^second]
* List item two.[^third]

[^third]: This is the third note, defined out of order.
[^second]: This is the second note.
[^fourth]: This is the fourth note.

# Header[^fourth]

Some paragraph with a footnote[^1], and another[^2].

[^1]: Content for fifth footnote.
[^2]: Content for sixth footnote spaning on 
    three lines, with some span-level markup like
    _emphasis_, a [link][].

[link]: http://michelf.ca/

Another paragraph with a named footnote[^fn-name].

[^fn-name]:
    Footnote beginning on the line next to the marker.

This paragraph should not have a footnote marker since 
the footnote is undefined.[^3]

This paragraph has a second footnote marker to footnote number one.[^1]

This paragraph links to a footnote with plenty of 
block-level content.[^block]

[^block]:
	Paragraph.
	
	*   List item
	
	> Blockquote
	
	    Code block

This paragraph host the footnote reference within a 
footnote test[^reference].

[^reference]:
	This footnote has a footnote of its own.[^nested]

[^nested]:
	This footnote should appear even though it is referenced
	from another footnote. But [^reference] should be litteral
	since the footnote with that name has already been used.

 - - -

Testing unusual footnote name[^1$^!"'].

[^1$^!"']: Haha!

 - - -
 
Footnotes mixed with images[^image-mixed]
![1800 Travel][img6]
![1830 Travel][img7]

[img6]: images/MGR-1800-travel.jpeg "Travel Speeds in 1800"
[^image-mixed]: Footnote Content
[img7]: images/MGR-1830-travel.jpeg "Travel Speeds in 1830"
In Markdown 1.0.0 and earlier. Version
8. This line turns into a list item.
Because a hard-wrapped line in the
middle of a paragraph looked like a
list item.

Here's one with a bullet.
* criminey.
Header  {#id1}
======

Header  { #id2}
------

### Header  {#id3 }
#### Header ##  { #id4 }

 - - -

Header  {.cl}
======

Header  { .cl}
------

### Header  {.cl }
#### Header ##  { .cl }

 - - -

Header  {.cl.class}
======

Header  { .cl .class}
------

### Header  {.cl .class }
#### Header ##  { .cl.class }

 - - -

Header  {#id5.cl.class}
======

Header  { #id6 .cl .class}
------

### Header  {.cl.class#id7 }
#### Header ##  { .cl.class#id8 }
Header
======

Header
------

### Header

 - - -

Header
======
Paragraph

Header
------
Paragraph

### Header
Paragraph

 - - -

Paragraph
Header
======
Paragraph

Paragraph
Header
------
Paragraph

Paragraph
### Header
ParagraphDashes:

---

 ---
 
  ---

   ---

	---

- - -

 - - -
 
  - - -

   - - -

	- - -


Asterisks:

***

 ***
 
  ***

   ***

	***

* * *

 * * *
 
  * * *

   * * *

	* * *


Underscores:

___

 ___
 
  ___

   ___

    ___

_ _ _

 _ _ _
 
  _ _ _

   _ _ _

    _ _ _
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")

Inline within a paragraph: [alt text](/url/).

![alt text](/url/  "title preceded by two spaces")

![alt text](/url/  "title has spaces afterward"  )

![alt text](</url/>)

![alt text](</url/> "with a title").

![Empty]()

![this is a stupid URL](http://example.com/(parens).jpg)


![alt text][foo]

  [foo]: /url/

![alt text][bar]

  [bar]: /url/ "Title here"Simple block on one line:

<div>foo</div>

And nested without indentation:

<div>
<div>
<div>
foo
</div>
<div style=">"/>
</div>
<div>bar</div>
</div>

And with attributes:

<div>
	<div id="foo">
	</div>
</div>

This was broken in 1.0.2b7:

<div class="inlinepage">
<div class="toggleableend">
foo
</div>
</div>
Here's a simple block:

<div>
	foo
</div>

This should be a code block, though:

	<div>
		foo
	</div>

As should this:

	<div>foo</div>

Now, nested:

<div>
	<div>
		<div>
			foo
		</div>
	</div>
</div>

This should just be an HTML comment:

<!-- Comment -->

Multiline:

<!--
Blah
Blah
-->

Code block:

	<!-- Comment -->

Just plain comment, with trailing spaces on the line:

<!-- foo -->   

Code:

	<hr />
	
Hr's:

<hr>

<hr/>

<hr />

<hr>   

<hr/>  

<hr /> 

<hr class="foo" id="bar" />

<hr class="foo" id="bar"/>

<hr class="foo" id="bar" >

<abbr title=" **Attribute Content Is Not A Code Span** ">ACINACS</abbr>

<abbr title="first backtick!">SB</abbr> 
<abbr title="second backtick!">SB</abbr>Paragraph one.

<!-- This is a simple comment -->

<!--
	This is another comment.
-->

Paragraph two.

<!-- one comment block -- -- with two comments -->

The end.
# Markdown inside code blocks

<div markdown="1">
foo
</div>

<div markdown='1'>
foo
</div>

<div markdown=1>
foo
</div>

<table>
<tr><td markdown="1">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="span">test _emphasis_ (span)</td></tr>
</table>

<table>
<tr><td markdown="block">test _emphasis_ (block)</td></tr>
</table>

## More complicated

<table>
<tr><td markdown="1">
* this is _not_ a list item</td></tr>
<tr><td markdown="span">
* this is _not_ a list item</td></tr>
<tr><td markdown="block">
* this _is_ a list item
</td></tr>
</table>

## With indent

<div>
    <div markdown="1">
    This text is no code block: if it was, the 
    closing <div> would be too and the HTML block 
    would be invalid.

    Markdown content in HTML blocks is assumed to be 
    indented the same as the block opening tag.

    **This should be the third paragraph after the header.**
    </div>
</div>

## Code block with rogue </div>s in Markdown code span and block

<div>
    <div markdown="1">

    This is a code block however:

        </div>

    Funny isn't it? Here is a code span: </div>.

    </div>
</div>

<div>
  <div markdown="1">
    * List item, not a code block

Some text

      This is a code block.
  </div>
</div>

## No code block in markdown span mode

<p markdown="1">
    This is not a code block since Markdown parse paragraph 
    content as span. Code spans like </p> are allowed though.
</p>

<p markdown="1">_Hello_ _world_</p>

## Preserving attributes and tags on more than one line:

<p class="test" markdown="1" 
id="12">
Some _span_ content.
</p>


## Header confusion bug

<table class="canvas">
<tr>
<td id="main" markdown="1">Hello World!
============

Hello World!</td>
</tr>
</table>
Here is a block tag ins:

<ins>
<p>Some text</p>
</ins>

<ins>And here it is inside a paragraph.</ins>

And here it is <ins>in the middle of</ins> a paragraph.

<del>
<p>Some text</p>
</del>

<del>And here is ins as a paragraph.</del>

And here it is <del>in the middle of</del> a paragraph.
		    GNU GENERAL PUBLIC LICENSE
		       Version 2, June 1991

 Copyright (C) 1989, 1991 Free Software Foundation, Inc.,
 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA
 Everyone is permitted to copy and distribute verbatim copies
 of this license document, but changing it is not allowed.

			    Preamble

  The licenses for most software are designed to take away your
freedom to share and change it.  By contrast, the GNU General Public
License is intended to guarantee your freedom to share and change free
software--to make sure the software is free for all its users.  This
General Public License applies to most of the Free Software
Foundation's software and to any other program whose authors commit to
using it.  (Some other Free Software Foundation software is covered by
the GNU Lesser General Public License instead.)  You can apply it to
your programs, too.

  When we speak of free software, we are referring to freedom, not
price.  Our General Public Licenses are designed to make sure that you
have the freedom to distribute copies of free software (and charge for
this service if you wish), that you receive source code or can get it
if you want it, that you can change the software or use pieces of it
in new free programs; and that you know you can do these things.

  To protect your rights, we need to make restrictions that forbid
anyone to deny you these rights or to ask you to surrender the rights.
These restrictions translate to certain responsibilities for you if you
distribute copies of the software, or if you modify it.

  For example, if you distribute copies of such a program, whether
gratis or for a fee, you must give the recipients all the rights that
you have.  You must make sure that they, too, receive or can get the
source code.  And you must show them these terms so they know their
rights.

  We protect your rights with two steps: (1) copyright the software, and
(2) offer you this license which gives you legal permission to copy,
distribute and/or modify the software.

  Also, for each author's protection and ours, we want to make certain
that everyone understands that there is no warranty for this free
software.  If the software is modified by someone else and passed on, we
want its recipients to know that what they have is not the original, so
that any problems introduced by others will not reflect on the original
authors' reputations.

  Finally, any free program is threatened constantly by software
patents.  We wish to avoid the danger that redistributors of a free
program will individually obtain patent licenses, in effect making the
program proprietary.  To prevent this, we have made it clear that any
patent must be licensed for everyone's free use or not licensed at all.

  The precise terms and conditions for copying, distribution and
modification follow.

		    GNU GENERAL PUBLIC LICENSE
   TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

  0. This License applies to any program or other work which contains
a notice placed by the copyright holder saying it may be distributed
under the terms of this General Public License.  The "Program", below,
refers to any such program or work, and a "work based on the Program"
means either the Program or any derivative work under copyright law:
that is to say, a work containing the Program or a portion of it,
either verbatim or with modifications and/or translated into another
language.  (Hereinafter, translation is included without limitation in
the term "modification".)  Each licensee is addressed as "you".

Activities other than copying, distribution and modification are not
covered by this License; they are outside its scope.  The act of
running the Program is not restricted, and the output from the Program
is covered only if its contents constitute a work based on the
Program (independent of having been made by running the Program).
Whether that is true depends on what the Program does.

  1. You may copy and distribute verbatim copies of the Program's
source code as you receive it, in any medium, provided that you
conspicuously and appropriately publish on each copy an appropriate
copyright notice and disclaimer of warranty; keep intact all the
notices that refer to this License and to the absence of any warranty;
and give any other recipients of the Program a copy of this License
along with the Program.

You may charge a fee for the physical act of transferring a copy, and
you may at your option offer warranty protection in exchange for a fee.

  2. You may modify your copy or copies of the Program or any portion
of it, thus forming a work based on the Program, and copy and
distribute such modifications or work under the terms of Section 1
above, provided that you also meet all of these conditions:

    a) You must cause the modified files to carry prominent notices
    stating that you changed the files and the date of any change.

    b) You must cause any work that you distribute or publish, that in
    whole or in part contains or is derived from the Program or any
    part thereof, to be licensed as a whole at no charge to all third
    parties under the terms of this License.

    c) If the modified program normally reads commands interactively
    when run, you must cause it, when started running for such
    interactive use in the most ordinary way, to print or display an
    announcement including an appropriate copyright notice and a
    notice that there is no warranty (or else, saying that you provide
    a warranty) and that users may redistribute the program under
    these conditions, and telling the user how to view a copy of this
    License.  (Exception: if the Program itself is interactive but
    does not normally print such an announcement, your work based on
    the Program is not required to print an announcement.)

These requirements apply to the modified work as a whole.  If
identifiable sections of that work are not derived from the Program,
and can be reasonably considered independent and separate works in
themselves, then this License, and its terms, do not apply to those
sections when you distribute them as separate works.  But when you
distribute the same sections as part of a whole which is a work based
on the Program, the distribution of the whole must be on the terms of
this License, whose permissions for other licensees extend to the
entire whole, and thus to each and every part regardless of who wrote it.

Thus, it is not the intent of this section to claim rights or contest
your rights to work written entirely by you; rather, the intent is to
exercise the right to control the distribution of derivative or
collective works based on the Program.

In addition, mere aggregation of another work not based on the Program
with the Program (or with a work based on the Program) on a volume of
a storage or distribution medium does not bring the other work under
the scope of this License.

  3. You may copy and distribute the Program (or a work based on it,
under Section 2) in object code or executable form under the terms of
Sections 1 and 2 above provided that you also do one of the following:

    a) Accompany it with the complete corresponding machine-readable
    source code, which must be distributed under the terms of Sections
    1 and 2 above on a medium customarily used for software interchange; or,

    b) Accompany it with a written offer, valid for at least three
    years, to give any third party, for a charge no more than your
    cost of physically performing source distribution, a complete
    machine-readable copy of the corresponding source code, to be
    distributed under the terms of Sections 1 and 2 above on a medium
    customarily used for software interchange; or,

    c) Accompany it with the information you received as to the offer
    to distribute corresponding source code.  (This alternative is
    allowed only for noncommercial distribution and only if you
    received the program in object code or executable form with such
    an offer, in accord with Subsection b above.)

The source code for a work means the preferred form of the work for
making modifications to it.  For an executable work, complete source
code means all the source code for all modules it contains, plus any
associated interface definition files, plus the scripts used to
control compilation and installation of the executable.  However, as a
special exception, the source code distributed need not include
anything that is normally distributed (in either source or binary
form) with the major components (compiler, kernel, and so on) of the
operating system on which the executable runs, unless that component
itself accompanies the executable.

If distribution of executable or object code is made by offering
access to copy from a designated place, then offering equivalent
access to copy the source code from the same place counts as
distribution of the source code, even though third parties are not
compelled to copy the source along with the object code.

  4. You may not copy, modify, sublicense, or distribute the Program
except as expressly provided under this License.  Any attempt
otherwise to copy, modify, sublicense or distribute the Program is
void, and will automatically terminate your rights under this License.
However, parties who have received copies, or rights, from you under
this License will not have their licenses terminated so long as such
parties remain in full compliance.

  5. You are not required to accept this License, since you have not
signed it.  However, nothing else grants you permission to modify or
distribute the Program or its derivative works.  These actions are
prohibited by law if you do not accept this License.  Therefore, by
modifying or distributing the Program (or any work based on the
Program), you indicate your acceptance of this License to do so, and
all its terms and conditions for copying, distributing or modifying
the Program or works based on it.

  6. Each time you redistribute the Program (or any work based on the
Program), the recipient automatically receives a license from the
original licensor to copy, distribute or modify the Program subject to
these terms and conditions.  You may not impose any further
restrictions on the recipients' exercise of the rights granted herein.
You are not responsible for enforcing compliance by third parties to
this License.

  7. If, as a consequence of a court judgment or allegation of patent
infringement or for any other reason (not limited to patent issues),
conditions are imposed on you (whether by court order, agreement or
otherwise) that contradict the conditions of this License, they do not
excuse you from the conditions of this License.  If you cannot
distribute so as to satisfy simultaneously your obligations under this
License and any other pertinent obligations, then as a consequence you
may not distribute the Program at all.  For example, if a patent
license would not permit royalty-free redistribution of the Program by
all those who receive copies directly or indirectly through you, then
the only way you could satisfy both it and this License would be to
refrain entirely from distribution of the Program.

If any portion of this section is held invalid or unenforceable under
any particular circumstance, the balance of the section is intended to
apply and the section as a whole is intended to apply in other
circumstances.

It is not the purpose of this section to induce you to infringe any
patents or other property right claims or to contest validity of any
such claims; this section has the sole purpose of protecting the
integrity of the free software distribution system, which is
implemented by public license practices.  Many people have made
generous contributions to the wide range of software distributed
through that system in reliance on consistent application of that
system; it is up to the author/donor to decide if he or she is willing
to distribute software through any other system and a licensee cannot
impose that choice.

This section is intended to make thoroughly clear what is believed to
be a consequence of the rest of this License.

  8. If the distribution and/or use of the Program is restricted in
certain countries either by patents or by copyrighted interfaces, the
original copyright holder who places the Program under this License
may add an explicit geographical distribution limitation excluding
those countries, so that distribution is permitted only in or among
countries not thus excluded.  In such case, this License incorporates
the limitation as if written in the body of this License.

  9. The Free Software Foundation may publish revised and/or new versions
of the General Public License from time to time.  Such new versions will
be similar in spirit to the present version, but may differ in detail to
address new problems or concerns.

Each version is given a distinguishing version number.  If the Program
specifies a version number of this License which applies to it and "any
later version", you have the option of following the terms and conditions
either of that version or of any later version published by the Free
Software Foundation.  If the Program does not specify a version number of
this License, you may choose any version ever published by the Free Software
Foundation.

  10. If you wish to incorporate parts of the Program into other free
programs whose distribution conditions are different, write to the author
to ask for permission.  For software which is copyrighted by the Free
Software Foundation, write to the Free Software Foundation; we sometimes
make exceptions for this.  Our decision will be guided by the two goals
of preserving the free status of all derivatives of our free software and
of promoting the sharing and reuse of software generally.

			    NO WARRANTY

  11. BECAUSE THE PROGRAM IS LICENSED FREE OF CHARGE, THERE IS NO WARRANTY
FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW.  EXCEPT WHEN
OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES
PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED
OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE.  THE ENTIRE RISK AS
TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU.  SHOULD THE
PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING,
REPAIR OR CORRECTION.

  12. IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING
WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MAY MODIFY AND/OR
REDISTRIBUTE THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES,
INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING
OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED
TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY
YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER
PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES.

		     END OF TERMS AND CONDITIONS

	    How to Apply These Terms to Your New Programs

  If you develop a new program, and you want it to be of the greatest
possible use to the public, the best way to achieve this is to make it
free software which everyone can redistribute and change under these terms.

  To do so, attach the following notices to the program.  It is safest
to attach them to the start of each source file to most effectively
convey the exclusion of warranty; and each file should have at least
the "copyright" line and a pointer to where the full notice is found.

    <one line to give the program's name and a brief idea of what it does.>
    Copyright (C) <year>  <name of author>

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

Also add information on how to contact you by electronic and paper mail.

If the program is interactive, make it output a short notice like this
when it starts in an interactive mode:

    Gnomovision version 69, Copyright (C) year name of author
    Gnomovision comes with ABSOLUTELY NO WARRANTY; for details type show w'.
    This is free software, and you are welcome to redistribute it
    under certain conditions; type show c' for details.

The hypothetical commands show w' and show c' should show the appropriate
parts of the General Public License.  Of course, the commands you use may
be called something other than show w' and show c'; they could even be
mouse-clicks or menu items--whatever suits your program.

You should also get your employer (if you work as a programmer) or your
school, if any, to sign a "copyright disclaimer" for the program, if
necessary.  Here is a sample; alter the names:

  Yoyodyne, Inc., hereby disclaims all copyright interest in the program
  Gnomovision' (which makes passes at compilers) written by James Hacker.

  <signature of Ty Coon>, 1 April 1989
  Ty Coon, President of Vice

This General Public License does not permit incorporating your program into
proprietary programs.  If your program is a subroutine library, you may
consider it more useful to permit linking proprietary applications with the
library.  If this is what you want to do, use the GNU Lesser General
Public License instead of this License.
This is an [inline link](/url "title"){.class #inline-link}.

This is a [reference link][refid].

This is an ![inline image](/img "title"){.class #inline-img}.

This is a ![reference image][refid].

[refid]: /path/to/something (Title) { .class #ref data-key=val }

Just a [URL](/url/).

[URL and title](/url/ "title").

[URL and title](/url/  "title preceded by two spaces").

[URL and title](/url/	"title preceded by a tab").

[URL and title](/url/ "title has spaces afterward"  ).

[URL wrapped in angle brackets](</url/>).

[URL w/ angle brackets + title](</url/> "Here's the title").

[Empty]().

[With parens in the URL](http://en.wikipedia.org/wiki/WIMP_(computing))

(With outer parens and [parens in url](/foo(bar)))


[With parens in the URL](/foo(bar) "and a title")

(With outer parens and [parens in url](/foo(bar) "and a title"))
Foo [bar] [1].

Foo [bar][1].

Foo [bar]
[1].

[1]: /url/  "Title"


With [embedded [brackets]] [b].


Indented [once][].

Indented [twice][].

Indented [thrice][].

Indented [four][] times.

 [once]: /url

  [twice]: /url

   [thrice]: /url

    [four]: /url


[b]: /url/

* * *

[this] [this] should work

So should [this][this].

And [this] [].

And [this][].

And [this].

But not [that] [].

Nor [that][].

Nor [that].

[Something in brackets like [this][] should work]

[Same with [this].]

In this case, [this](/somethingelse/) points to something else.

Backslashing should suppress \[this] and [this\].

[this]: foo


* * *

Here's one where the [link
breaks] across lines.

Here's another where the [link 
breaks] across lines, but with a line-ending space.


[link breaks]: /url/
This is the [simple case].

[simple case]: /simple



This one has a [line
break].

This one has a [line 
break] with a line-ending space.

[line break]: /foo


[this] [that] and the [other]

[this]: /this
[that]: /that
[other]: /other
Foo [bar][].

Foo [bar](/url/ "Title with "quotes" inside").


  [bar]: /url/ "Title with "quotes" inside"

Markdown: Basics
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a class="selected" title="Markdown Basics">Basics</a></li>
    <li><a href="/projects/markdown/syntax" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


Getting the Gist of Markdown's Formatting Syntax
------------------------------------------------

This page offers a brief overview of what it's like to use Markdown.
The [syntax page] [s] provides complete, detailed documentation for
every feature, but Markdown should be very easy to pick up simply by
looking at a few examples of it in action. The examples on this page
are written in a before/after style, showing example syntax and the
HTML output produced by Markdown.

It's also helpful to simply try Markdown out; the [Dingus] [d] is a
web application that allows you type your own Markdown-formatted text
and translate it to XHTML.

**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL] [src].

  [s]: /projects/markdown/syntax  "Markdown Syntax"
  [d]: /projects/markdown/dingus  "Markdown Dingus"
  [src]: /projects/markdown/basics.text


## Paragraphs, Headers, Blockquotes ##

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

Markdown offers two styles of headers: *Setext* and *atx*.
Setext-style headers for <h1> and <h2> are created by
"underlining" with equal signs (=) and hyphens (-), respectively.
To create an atx-style header, you put 1-6 hash marks (#) at the
beginning of the line -- the number of hashes equals the resulting
HTML header level.

Blockquotes are indicated using email-style '>' angle brackets.

Markdown:

    A First Level Header
    ====================
    
    A Second Level Header
    ---------------------

    Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.

    The quick brown fox jumped over the lazy
    dog's back.
    
    ### Header 3

    > This is a blockquote.
    > 
    > This is the second paragraph in the blockquote.
    >
    > ## This is an H2 in a blockquote


Output:

    <h1>A First Level Header</h1>
    
    <h2>A Second Level Header</h2>
    
    <p>Now is the time for all good men to come to
    the aid of their country. This is just a
    regular paragraph.</p>
    
    <p>The quick brown fox jumped over the lazy
    dog's back.</p>
    
    <h3>Header 3</h3>
    
    <blockquote>
        <p>This is a blockquote.</p>
        
        <p>This is the second paragraph in the blockquote.</p>
        
        <h2>This is an H2 in a blockquote</h2>
    </blockquote>



### Phrase Emphasis ###

Markdown uses asterisks and underscores to indicate spans of emphasis.

Markdown:

    Some of these words *are emphasized*.
    Some of these words _are emphasized also_.
    
    Use two asterisks for **strong emphasis**.
    Or, if you prefer, __use two underscores instead__.

Output:

    <p>Some of these words <em>are emphasized</em>.
    Some of these words <em>are emphasized also</em>.</p>
    
    <p>Use two asterisks for <strong>strong emphasis</strong>.
    Or, if you prefer, <strong>use two underscores instead</strong>.</p>
   


## Lists ##

Unordered (bulleted) lists use asterisks, pluses, and hyphens (*,
+, and -) as list markers. These three markers are
interchangable; this:

    *   Candy.
    *   Gum.
    *   Booze.

this:

    +   Candy.
    +   Gum.
    +   Booze.

and this:

    -   Candy.
    -   Gum.
    -   Booze.

all produce the same output:

    <ul>
    <li>Candy.</li>
    <li>Gum.</li>
    <li>Booze.</li>
    </ul>

Ordered (numbered) lists use regular numbers, followed by periods, as
list markers:

    1.  Red
    2.  Green
    3.  Blue

Output:

    <ol>
    <li>Red</li>
    <li>Green</li>
    <li>Blue</li>
    </ol>

If you put blank lines between items, you'll get <p> tags for the
list item text. You can create multi-paragraph list items by indenting
the paragraphs by 4 spaces or 1 tab:

    *   A list item.
    
        With multiple paragraphs.

    *   Another item in the list.

Output:

    <ul>
    <li><p>A list item.</p>
    <p>With multiple paragraphs.</p></li>
    <li><p>Another item in the list.</p></li>
    </ul>
    


### Links ###

Markdown supports two styles for creating links: *inline* and
*reference*. With both styles, you use square brackets to delimit the
text you want to turn into a link.

Inline-style links use parentheses immediately after the link text.
For example:

    This is an [example link](http://example.com/).

Output:

    <p>This is an <a href="http://example.com/">
    example link</a>.</p>

Optionally, you may include a title attribute in the parentheses:

    This is an [example link](http://example.com/ "With a Title").

Output:

    <p>This is an <a href="http://example.com/" title="With a Title">
    example link</a>.</p>

Reference-style links allow you to refer to your links by names, which
you define elsewhere in your document:

    I get 10 times more traffic from [Google][1] than from
    [Yahoo][2] or [MSN][3].

    [1]: http://google.com/        "Google"
    [2]: http://search.yahoo.com/  "Yahoo Search"
    [3]: http://search.msn.com/    "MSN Search"

Output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from <a href="http://search.yahoo.com/"
    title="Yahoo Search">Yahoo</a> or <a href="http://search.msn.com/"
    title="MSN Search">MSN</a>.</p>

The title attribute is optional. Link names may contain letters,
numbers and spaces, but are *not* case sensitive:

    I start my morning with a cup of coffee and
    [The New York Times][NY Times].

    [ny times]: http://www.nytimes.com/

Output:

    <p>I start my morning with a cup of coffee and
    <a href="http://www.nytimes.com/">The New York Times</a>.</p>


### Images ###

Image syntax is very much like link syntax.

Inline (titles are optional):

    ![alt text](/path/to/img.jpg "Title")

Reference-style:

    ![alt text][id]

    [id]: /path/to/img.jpg "Title"

Both of the above examples produce the same output:

    <img src="/path/to/img.jpg" alt="alt text" title="Title" />



### Code ###

In a regular paragraph, you can create code span by wrapping text in
backtick quotes. Any ampersands (&) and angle brackets (< or
>) will automatically be translated into HTML entities. This makes
it easy to use Markdown to write about HTML example code:

    I strongly recommend against using any <blink> tags.

    I wish SmartyPants used named entities like &mdash;
    instead of decimal-encoded entites like &#8212;.

Output:

    <p>I strongly recommend against using any
    <code>&lt;blink&gt;</code> tags.</p>
    
    <p>I wish SmartyPants used named entities like
    <code>&amp;mdash;</code> instead of decimal-encoded
    entites like <code>&amp;#8212;</code>.</p>


To specify an entire block of pre-formatted code, indent every line of
the block by 4 spaces or 1 tab. Just like with code spans, &, <,
and > characters will be escaped automatically.

Markdown:

    If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:

        <blockquote>
            <p>For example.</p>
        </blockquote>

Output:

    <p>If you want your page to validate under XHTML 1.0 Strict,
    you've got to put paragraph tags in your blockquotes:</p>
    
    <pre><code>&lt;blockquote&gt;
        &lt;p&gt;For example.&lt;/p&gt;
    &lt;/blockquote&gt;
    </code></pre>
Markdown: Syntax
================

<ul id="ProjectSubmenu">
    <li><a href="/projects/markdown/" title="Markdown Project Page">Main</a></li>
    <li><a href="/projects/markdown/basics" title="Markdown Basics">Basics</a></li>
    <li><a class="selected" title="Markdown Syntax Documentation">Syntax</a></li>
    <li><a href="/projects/markdown/license" title="Pricing and License Information">License</a></li>
    <li><a href="/projects/markdown/dingus" title="Online Markdown Web Form">Dingus</a></li>
</ul>


*   [Overview](#overview)
    *   [Philosophy](#philosophy)
    *   [Inline HTML](#html)
    *   [Automatic Escaping for Special Characters](#autoescape)
*   [Block Elements](#block)
    *   [Paragraphs and Line Breaks](#p)
    *   [Headers](#header)
    *   [Blockquotes](#blockquote)
    *   [Lists](#list)
    *   [Code Blocks](#precode)
    *   [Horizontal Rules](#hr)
*   [Span Elements](#span)
    *   [Links](#link)
    *   [Emphasis](#em)
    *   [Code](#code)
    *   [Images](#img)
*   [Miscellaneous](#misc)
    *   [Backslash Escapes](#backslash)
    *   [Automatic Links](#autolink)


**Note:** This document is itself written using Markdown; you
can [see the source for it by adding '.text' to the URL][src].

  [src]: /projects/markdown/syntax.text

* * *

<h2 id="overview">Overview</h2>

<h3 id="philosophy">Philosophy</h3>

Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

Readability, however, is emphasized above all else. A Markdown-formatted
document should be publishable as-is, as plain text, without looking
like it's been marked up with tags or formatting instructions. While
Markdown's syntax has been influenced by several existing text-to-HTML
filters -- including [Setext] [1], [atx] [2], [Textile] [3], [reStructuredText] [4],
[Grutatext] [5], and [EtText] [6] -- the single biggest source of
inspiration for Markdown's syntax is the format of plain text email.

  [1]: http://docutils.sourceforge.net/mirror/setext.html
  [2]: http://www.aaronsw.com/2002/atx/
  [3]: http://textism.com/tools/textile/
  [4]: http://docutils.sourceforge.net/rst.html
  [5]: http://www.triptico.com/software/grutatxt.html
  [6]: http://ettext.taint.org/doc/

To this end, Markdown's syntax is comprised entirely of punctuation
characters, which punctuation characters have been carefully chosen so
as to look like what they mean. E.g., asterisks around a word actually
look like \*emphasis\*. Markdown lists look like, well, lists. Even
blockquotes look like quoted passages of text, assuming you've ever
used email.



<h3 id="html">Inline HTML</h3>

Markdown's syntax is intended for one purpose: to be used as a
format for *writing* for the web.

Markdown is not a replacement for HTML, or even close to it. Its
syntax is very small, corresponding only to a very small subset of
HTML tags. The idea is *not* to create a syntax that makes it easier
to insert HTML tags. In my opinion, HTML tags are already easy to
insert. The idea for Markdown is to make it easy to read, write, and
edit prose. HTML is a *publishing* format; Markdown is a *writing*
format. Thus, Markdown's formatting syntax only addresses issues that
can be conveyed in plain text.

For any markup that is not covered by Markdown's syntax, you simply
use HTML itself. There's no need to preface it or delimit it to
indicate that you're switching from Markdown to HTML; you just use
the tags.

The only restrictions are that block-level HTML elements -- e.g. <div>,
<table>, <pre>, <p>, etc. -- must be separated from surrounding
content by blank lines, and the start and end tags of the block should
not be indented with tabs or spaces. Markdown is smart enough not
to add extra (unwanted) <p> tags around HTML block-level tags.

For example, to add an HTML table to a Markdown article:

    This is a regular paragraph.

    <table>
        <tr>
            <td>Foo</td>
        </tr>
    </table>

    This is another regular paragraph.

Note that Markdown formatting syntax is not processed within block-level
HTML tags. E.g., you can't use Markdown-style *emphasis* inside an
HTML block.

Span-level HTML tags -- e.g. <span>, <cite>, or <del> -- can be
used anywhere in a Markdown paragraph, list item, or header. If you
want, you can even use HTML tags instead of Markdown formatting; e.g. if
you'd prefer to use HTML <a> or <img> tags instead of Markdown's
link or image syntax, go right ahead.

Unlike block-level HTML tags, Markdown syntax *is* processed within
span-level tags.


<h3 id="autoescape">Automatic Escaping for Special Characters</h3>

In HTML, there are two characters that demand special treatment: <
and &. Left angle brackets are used to start tags; ampersands are
used to denote HTML entities. If you want to use them as literal
characters, you must escape them as entities, e.g. &lt;, and
&amp;.

Ampersands in particular are bedeviling for web writers. If you want to
write about 'AT&T', you need to write 'AT&amp;T'. You even need to
escape ampersands within URLs. Thus, if you want to link to:

    http://images.google.com/images?num=30&q=larry+bird

you need to encode the URL as:

    http://images.google.com/images?num=30&amp;q=larry+bird

in your anchor tag href attribute. Needless to say, this is easy to
forget, and is probably the single most common source of HTML validation
errors in otherwise well-marked-up web sites.

Markdown allows you to use these characters naturally, taking care of
all the necessary escaping for you. If you use an ampersand as part of
an HTML entity, it remains unchanged; otherwise it will be translated
into &amp;.

So, if you want to include a copyright symbol in your article, you can write:

    &copy;

and Markdown will leave it alone. But if you write:

    AT&T

Markdown will translate it to:

    AT&amp;T

Similarly, because Markdown supports [inline HTML](#html), if you use
angle brackets as delimiters for HTML tags, Markdown will treat them as
such. But if you write:

    4 < 5

Markdown will translate it to:

    4 &lt; 5

However, inside Markdown code spans and blocks, angle brackets and
ampersands are *always* encoded automatically. This makes it easy to use
Markdown to write about HTML code. (As opposed to raw HTML, which is a
terrible format for writing about HTML syntax, because every single <
and & in your example code needs to be escaped.)


* * *


<h2 id="block">Block Elements</h2>


<h3 id="p">Paragraphs and Line Breaks</h3>

A paragraph is simply one or more consecutive lines of text, separated
by one or more blank lines. (A blank line is any line that looks like a
blank line -- a line containing nothing but spaces or tabs is considered
blank.) Normal paragraphs should not be intended with spaces or tabs.

The implication of the "one or more consecutive lines of text" rule is
that Markdown supports "hard-wrapped" text paragraphs. This differs
significantly from most other text-to-HTML formatters (including Movable
Type's "Convert Line Breaks" option) which translate every line break
character in a paragraph into a <br /> tag.

When you *do* want to insert a <br /> break tag using Markdown, you
end a line with two or more spaces, then type return.

Yes, this takes a tad more effort to create a <br />, but a simplistic
"every line break is a <br />" rule wouldn't work for Markdown.
Markdown's email-style [blockquoting][bq] and multi-paragraph [list items][l]
work best -- and look better -- when you format them with hard breaks.

  [bq]: #blockquote
  [l]:  #list



<h3 id="header">Headers</h3>

Markdown supports two styles of headers, [Setext] [1] and [atx] [2].

Setext-style headers are "underlined" using equal signs (for first-level
headers) and dashes (for second-level headers). For example:

    This is an H1
    =============

    This is an H2
    -------------

Any number of underlining ='s or -'s will work.

Atx-style headers use 1-6 hash characters at the start of the line,
corresponding to header levels 1-6. For example:

    # This is an H1

    ## This is an H2

    ###### This is an H6

Optionally, you may "close" atx-style headers. This is purely
cosmetic -- you can use this if you think it looks better. The
closing hashes don't even need to match the number of hashes
used to open the header. (The number of opening hashes
determines the header level.) :

    # This is an H1 #

    ## This is an H2 ##

    ### This is an H3 ######


<h3 id="blockquote">Blockquotes</h3>

Markdown uses email-style > characters for blockquoting. If you're
familiar with quoting passages of text in an email message, then you
know how to create a blockquote in Markdown. It looks best if you hard
wrap the text and put a > before every line:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    > consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    > Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
    > 
    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    > id sem consectetuer libero luctus adipiscing.

Markdown allows you to be lazy and only put the > before the first
line of a hard-wrapped paragraph:

    > This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
    consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
    Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

    > Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
    id sem consectetuer libero luctus adipiscing.

Blockquotes can be nested (i.e. a blockquote-in-a-blockquote) by
adding additional levels of >:

    > This is the first level of quoting.
    >
    > > This is nested blockquote.
    >
    > Back to the first level.

Blockquotes can contain other Markdown elements, including headers, lists,
and code blocks:

	> ## This is a header.
	> 
	> 1.   This is the first list item.
	> 2.   This is the second list item.
	> 
	> Here's some example code:
	> 
	>     return shell_exec("echo $input | $markdown_script");

Any decent text editor should make email-style quoting easy. For
example, with BBEdit, you can make a selection and choose Increase
Quote Level from the Text menu.


<h3 id="list">Lists</h3>

Markdown supports ordered (numbered) and unordered (bulleted) lists.

Unordered lists use asterisks, pluses, and hyphens -- interchangably
-- as list markers:

    *   Red
    *   Green
    *   Blue

is equivalent to:

    +   Red
    +   Green
    +   Blue

and:

    -   Red
    -   Green
    -   Blue

Ordered lists use numbers followed by periods:

    1.  Bird
    2.  McHale
    3.  Parish

It's important to note that the actual numbers you use to mark the
list have no effect on the HTML output Markdown produces. The HTML
Markdown produces from the above list is:

    <ol>
    <li>Bird</li>
    <li>McHale</li>
    <li>Parish</li>
    </ol>

If you instead wrote the list in Markdown like this:

    1.  Bird
    1.  McHale
    1.  Parish

or even:

    3. Bird
    1. McHale
    8. Parish

you'd get the exact same HTML output. The point is, if you want to,
you can use ordinal numbers in your ordered Markdown lists, so that
the numbers in your source match the numbers in your published HTML.
But if you want to be lazy, you don't have to.

If you do use lazy list numbering, however, you should still start the
list with the number 1. At some point in the future, Markdown may support
starting ordered lists at an arbitrary number.

List markers typically start at the left margin, but may be indented by
up to three spaces. List markers must be followed by one or more spaces
or a tab.

To make lists look nice, you can wrap items with hanging indents:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
        Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
        viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
        Suspendisse id sem consectetuer libero luctus adipiscing.

But if you want to be lazy, you don't have to:

    *   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
    *   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.

If list items are separated by blank lines, Markdown will wrap the
items in <p> tags in the HTML output. For example, this input:

    *   Bird
    *   Magic

will turn into:

    <ul>
    <li>Bird</li>
    <li>Magic</li>
    </ul>

But this:

    *   Bird

    *   Magic

will turn into:

    <ul>
    <li><p>Bird</p></li>
    <li><p>Magic</p></li>
    </ul>

List items may consist of multiple paragraphs. Each subsequent
paragraph in a list item must be intended by either 4 spaces
or one tab:

    1.  This is a list item with two paragraphs. Lorem ipsum dolor
        sit amet, consectetuer adipiscing elit. Aliquam hendrerit
        mi posuere lectus.

        Vestibulum enim wisi, viverra nec, fringilla in, laoreet
        vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
        sit amet velit.

    2.  Suspendisse id sem consectetuer libero luctus adipiscing.

It looks nice if you indent every line of the subsequent
paragraphs, but here again, Markdown will allow you to be
lazy:

    *   This is a list item with two paragraphs.

        This is the second paragraph in the list item. You're
    only required to indent the first line. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit.

    *   Another item in the same list.

To put a blockquote within a list item, the blockquote's >
delimiters need to be indented:

    *   A list item with a blockquote:

        > This is a blockquote
        > inside a list item.

To put a code block within a list item, the code block needs
to be indented *twice* -- 8 spaces or two tabs:

    *   A list item with a code block:

            <code goes here>


It's worth noting that it's possible to trigger an ordered list by
accident, by writing something like this:

    1986. What a great season.

In other words, a *number-period-space* sequence at the beginning of a
line. To avoid this, you can backslash-escape the period:

    1986\. What a great season.



<h3 id="precode">Code Blocks</h3>

Pre-formatted code blocks are used for writing about programming or
markup source code. Rather than forming normal paragraphs, the lines
of a code block are interpreted literally. Markdown wraps a code block
in both <pre> and <code> tags.

To produce a code block in Markdown, simply indent every line of the
block by at least 4 spaces or 1 tab. For example, given this input:

    This is a normal paragraph:

        This is a code block.

Markdown will generate:

    <p>This is a normal paragraph:</p>

    <pre><code>This is a code block.
    </code></pre>

One level of indentation -- 4 spaces or 1 tab -- is removed from each
line of the code block. For example, this:

    Here is an example of AppleScript:

        tell application "Foo"
            beep
        end tell

will turn into:

    <p>Here is an example of AppleScript:</p>

    <pre><code>tell application "Foo"
        beep
    end tell
    </code></pre>

A code block continues until it reaches a line that is not indented
(or the end of the article).

Within a code block, ampersands (&) and angle brackets (< and >)
are automatically converted into HTML entities. This makes it very
easy to include example HTML source code using Markdown -- just paste
it and indent it, and Markdown will handle the hassle of encoding the
ampersands and angle brackets. For example, this:

        <div class="footer">
            &copy; 2004 Foo Corporation
        </div>

will turn into:

    <pre><code>&lt;div class="footer"&gt;
        &amp;copy; 2004 Foo Corporation
    &lt;/div&gt;
    </code></pre>

Regular Markdown syntax is not processed within code blocks. E.g.,
asterisks are just literal asterisks within a code block. This means
it's also easy to use Markdown to write about Markdown's own syntax.



<h3 id="hr">Horizontal Rules</h3>

You can produce a horizontal rule tag (<hr />) by placing three or
more hyphens, asterisks, or underscores on a line by themselves. If you
wish, you may use spaces between the hyphens or asterisks. Each of the
following lines will produce a horizontal rule:

    * * *

    ***

    *****
	
    - - -

    ---------------------------------------

	_ _ _


* * *

<h2 id="span">Span Elements</h2>

<h3 id="link">Links</h3>

Markdown supports two style of links: *inline* and *reference*.

In both styles, the link text is delimited by [square brackets].

To create an inline link, use a set of regular parentheses immediately
after the link text's closing square bracket. Inside the parentheses,
put the URL where you want the link to point, along with an *optional*
title for the link, surrounded in quotes. For example:

    This is [an example](http://example.com/ "Title") inline link.

    [This link](http://example.net/) has no title attribute.

Will produce:

    <p>This is <a href="http://example.com/" title="Title">
    an example</a> inline link.</p>

    <p><a href="http://example.net/">This link</a> has no
    title attribute.</p>

If you're referring to a local resource on the same server, you can
use relative paths:

    See my [About](/about/) page for details.

Reference-style links use a second set of square brackets, inside
which you place a label of your choosing to identify the link:

    This is [an example][id] reference-style link.

You can optionally use a space to separate the sets of brackets:

    This is [an example] [id] reference-style link.

Then, anywhere in the document, you define your link label like this,
on a line by itself:

    [id]: http://example.com/  "Optional Title Here"

That is:

*   Square brackets containing the link identifier (optionally
    indented from the left margin using up to three spaces);
*   followed by a colon;
*   followed by one or more spaces (or tabs);
*   followed by the URL for the link;
*   optionally followed by a title attribute for the link, enclosed
    in double or single quotes.

The link URL may, optionally, be surrounded by angle brackets:

    [id]: <http://example.com/>  "Optional Title Here"

You can put the title attribute on the next line and use extra spaces
or tabs for padding, which tends to look better with longer URLs:

    [id]: http://example.com/longish/path/to/resource/here
        "Optional Title Here"

Link definitions are only used for creating links during Markdown
processing, and are stripped from your document in the HTML output.

Link definition names may constist of letters, numbers, spaces, and punctuation -- but they are *not* case sensitive. E.g. these two links:

	[link text][a]
	[link text][A]

are equivalent.

The *implicit link name* shortcut allows you to omit the name of the
link, in which case the link text itself is used as the name.
Just use an empty set of square brackets -- e.g., to link the word
"Google" to the google.com web site, you could simply write:

	[Google][]

And then define the link:

	[Google]: http://google.com/

Because link names may contain spaces, this shortcut even works for
multiple words in the link text:

	Visit [Daring Fireball][] for more information.

And then define the link:
	
	[Daring Fireball]: http://daringfireball.net/

Link definitions can be placed anywhere in your Markdown document. I
tend to put them immediately after each paragraph in which they're
used, but if you want, you can put them all at the end of your
document, sort of like footnotes.

Here's an example of reference links in action:

    I get 10 times more traffic from [Google] [1] than from
    [Yahoo] [2] or [MSN] [3].

      [1]: http://google.com/        "Google"
      [2]: http://search.yahoo.com/  "Yahoo Search"
      [3]: http://search.msn.com/    "MSN Search"

Using the implicit link name shortcut, you could instead write:

    I get 10 times more traffic from [Google][] than from
    [Yahoo][] or [MSN][].

      [google]: http://google.com/        "Google"
      [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
      [msn]:    http://search.msn.com/    "MSN Search"

Both of the above examples will produce the following HTML output:

    <p>I get 10 times more traffic from <a href="http://google.com/"
    title="Google">Google</a> than from
    <a href="http://search.yahoo.com/" title="Yahoo Search">Yahoo</a>
    or <a href="http://search.msn.com/" title="MSN Search">MSN</a>.</p>

For comparison, here is the same paragraph written using
Markdown's inline link style:

    I get 10 times more traffic from [Google](http://google.com/ "Google")
    than from [Yahoo](http://search.yahoo.com/ "Yahoo Search") or
    [MSN](http://search.msn.com/ "MSN Search").

The point of reference-style links is not that they're easier to
write. The point is that with reference-style links, your document
source is vastly more readable. Compare the above examples: using
reference-style links, the paragraph itself is only 81 characters
long; with inline-style links, it's 176 characters; and as raw HTML,
it's 234 characters. In the raw HTML, there's more markup than there
is text.

With Markdown's reference-style links, a source document much more
closely resembles the final output, as rendered in a browser. By
allowing you to move the markup-related metadata out of the paragraph,
you can add links without interrupting the narrative flow of your
prose.


<h3 id="em">Emphasis</h3>

Markdown treats asterisks (*) and underscores (_) as indicators of
emphasis. Text wrapped with one * or _ will be wrapped with an
HTML <em> tag; double *'s or _'s will be wrapped with an HTML
<strong> tag. E.g., this input:

    *single asterisks*

    _single underscores_

    **double asterisks**

    __double underscores__

will produce:

    <em>single asterisks</em>

    <em>single underscores</em>

    <strong>double asterisks</strong>

    <strong>double underscores</strong>

You can use whichever style you prefer; the lone restriction is that
the same character must be used to open and close an emphasis span.

Emphasis can be used in the middle of a word:

    un*fucking*believable

But if you surround an * or _ with spaces, it'll be treated as a
literal asterisk or underscore.

To produce a literal asterisk or underscore at a position where it
would otherwise be used as an emphasis delimiter, you can backslash
escape it:

    \*this text is surrounded by literal asterisks\*



<h3 id="code">Code</h3>

To indicate a span of code, wrap it with backtick quotes (  ).
Unlike a pre-formatted code block, a code span indicates code within a
normal paragraph. For example:

    Use the printf() function.

will produce:

    <p>Use the <code>printf()</code> function.</p>

To include a literal backtick character within a code span, you can use
multiple backticks as the opening and closing delimiters:

     There is a literal backtick () here.

which will produce this:

    <p><code>There is a literal backtick () here.</code></p>

The backtick delimiters surrounding a code span may include spaces --
one after the opening, one before the closing. This allows you to place
literal backtick characters at the beginning or end of a code span:

	A single backtick in a code span:     
	
	A backtick-delimited string in a code span:   foo  

will produce:

	<p>A single backtick in a code span: <code></code></p>
	
	<p>A backtick-delimited string in a code span: <code>foo</code></p>

With a code span, ampersands and angle brackets are encoded as HTML
entities automatically, which makes it easy to include example HTML
tags. Markdown will turn this:

    Please don't use any <blink> tags.

into:

    <p>Please don't use any <code>&lt;blink&gt;</code> tags.</p>

You can write this:

    &#8212; is the decimal-encoded equivalent of &mdash;.

to produce:

    <p><code>&amp;#8212;</code> is the decimal-encoded
    equivalent of <code>&amp;mdash;</code>.</p>



<h3 id="img">Images</h3>

Admittedly, it's fairly difficult to devise a "natural" syntax for
placing images into a plain text document format.

Markdown uses an image syntax that is intended to resemble the syntax
for links, allowing for two styles: *inline* and *reference*.

Inline image syntax looks like this:

    ![Alt text](/path/to/img.jpg)

    ![Alt text](/path/to/img.jpg "Optional title")

That is:

*   An exclamation mark: !;
*   followed by a set of square brackets, containing the alt
    attribute text for the image;
*   followed by a set of parentheses, containing the URL or path to
    the image, and an optional title attribute enclosed in double
    or single quotes.

Reference-style image syntax looks like this:

    ![Alt text][id]

Where "id" is the name of a defined image reference. Image references
are defined using syntax identical to link references:

    [id]: url/to/image  "Optional title attribute"

As of this writing, Markdown has no syntax for specifying the
dimensions of an image; if this is important to you, you can simply
use regular HTML <img> tags.


* * *


<h2 id="misc">Miscellaneous</h2>

<h3 id="autolink">Automatic Links</h3>

Markdown supports a shortcut style for creating "automatic" links for URLs and email addresses: simply surround the URL or email address with angle brackets. What this means is that if you want to show the actual text of a URL or email address, and also have it be a clickable link, you can do this:

    <http://example.com/>
    
Markdown will turn this into:

    <a href="http://example.com/">http://example.com/</a>

Automatic links for email addresses work similarly, except that
Markdown will also perform a bit of randomized decimal and hex
entity-encoding to help obscure your address from address-harvesting
spambots. For example, Markdown will turn this:

    <address@example.com>

into something like this:

    <a href="&#x6D;&#x61;i&#x6C;&#x74;&#x6F;:&#x61;&#x64;&#x64;&#x72;&#x65;
    &#115;&#115;&#64;&#101;&#120;&#x61;&#109;&#x70;&#x6C;e&#x2E;&#99;&#111;
    &#109;">&#x61;&#x64;&#x64;&#x72;&#x65;&#115;&#115;&#64;&#101;&#120;&#x61;
    &#109;&#x70;&#x6C;e&#x2E;&#99;&#111;&#109;</a>

which will render in a browser as a clickable link to "address@example.com".

(This sort of entity-encoding trick will indeed fool many, if not
most, address-harvesting bots, but it definitely won't fool all of
them. It's better than nothing, but an address published in this way
will probably eventually start receiving spam.)



<h3 id="backslash">Backslash Escapes</h3>

Markdown allows you to use backslash escapes to generate literal
characters which would otherwise have special meaning in Markdown's
formatting syntax. For example, if you wanted to surround a word with
literal asterisks (instead of an HTML <em> tag), you can backslashes
before the asterisks, like this:

    \*literal asterisks\*

Markdown provides backslash escapes for the following characters:

    \   backslash
       backtick
    *   asterisk
    _   underscore
    {}  curly braces
    []  square brackets
    ()  parentheses
    #   hash mark
	+	plus sign
	-	minus sign (hyphen)
    .   dot
    !   exclamation mark

# Character Escapes

The MD5 value for + is "26b17225b626fb9238849fd60eabdf60".

# HTML Blocks

<p>test</p>

The MD5 value for <p>test</p> is:

6205333b793f34273d75379350b36826* test
+ test
- test

1. test
2. test

* test
+ test
- test

1. test
2. test
> foo
>
> > bar
>
> foo
Valid nesting:

**[Link](url)**

[**Link**](url)

**[**Link**](url)**

Invalid nesting:

[[Link](url)](url)## Unordered

Asterisks tight:

*	asterisk 1
*	asterisk 2
*	asterisk 3


Asterisks loose:

*	asterisk 1

*	asterisk 2

*	asterisk 3

* * *

Pluses tight:

+	Plus 1
+	Plus 2
+	Plus 3


Pluses loose:

+	Plus 1

+	Plus 2

+	Plus 3

* * *


Minuses tight:

-	Minus 1
-	Minus 2
-	Minus 3


Minuses loose:

-	Minus 1

-	Minus 2

-	Minus 3


## Ordered

Tight:

1.	First
2.	Second
3.	Third

and:

1. One
2. Two
3. Three


Loose using tabs:

1.	First

2.	Second

3.	Third

and using spaces:

1. One

2. Two

3. Three

Multiple paragraphs:

1.	Item 1, graf one.

	Item 2. graf two. The quick brown fox jumped over the lazy dog's
	back.
	
2.	Item 2.

3.	Item 3.



## Nested

*	Tab
	*	Tab
		*	Tab

Here's another:

1. First
2. Second:
	* Fee
	* Fie
	* Foe
3. Third

Same thing but with paragraphs:

1. First

2. Second:
	* Fee
	* Fie
	* Foe

3. Third


This was an error in Markdown 1.0.1:

*	this

	*	sub

	that
[Inline link 1 with parens](/url\(test\) "title").

[Inline link 2 with parens](</url\(test\)> "title").

[Inline link 3 with non-escaped parens](/url(test) "title").

[Inline link 4 with non-escaped parens](</url(test)> "title").

[Reference link 1 with parens][1].

[Reference link 2 with parens][2].

  [1]: /url(test) "title"
  [2]: </url(test)> "title"
This tests for a bug where quotes escaped by PHP when using 
preg_replace with the /e modifier must be correctly unescaped
(hence the _UnslashQuotes function found only in PHP Markdown).



Headers below should appear exactly as they are typed (no backslash
added or removed).

Header "quoted\" again \\""
===========================

Header "quoted\" again \\""
---------------------------

### Header "quoted\" again \\"" ###



Test with tabs for _Detab:

	Code	'block'	with	some	"tabs"	and	"quotes"
[Test](/"style="color:red)
[Test](/'style='color:red)

![](/"style="border-color:red;border-size:1px;border-style:solid)
![](/'style='border-color:red;border-size:1px;border-style:solid)
***This is strong and em.***

So is ***this*** word.

___This is strong and em.___

So is ___this___ word.
# Simple tables

Header 1  | Header 2
--------- | ---------
Cell 1    | Cell 2
Cell 3    | Cell 4

With leading pipes:

| Header 1  | Header 2
| --------- | ---------
| Cell 1    | Cell 2
| Cell 3    | Cell 4

With tailing pipes:

Header 1  | Header 2  |
--------- | --------- |
Cell 1    | Cell 2    |
Cell 3    | Cell 4    |

With leading and tailing pipes:

| Header 1  | Header 2  |
| --------- | --------- |
| Cell 1    | Cell 2    |
| Cell 3    | Cell 4    |

* * *

# One-column one-row table

With leading pipes:

| Header
| -------
| Cell

With tailing pipes:

Header  |
------- |
Cell    |

With leading and tailing pipes:

| Header  |
| ------- |
| Cell    |

* * *

Table alignement:

| Default   | Right     |  Center   |     Left  |
| --------- |:--------- |:---------:| ---------:|
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

Table alignement (alternate spacing):

| Default   | Right     |  Center   |     Left  |
| --------- | :-------- | :-------: | --------: |
| Long Cell | Long Cell | Long Cell | Long Cell |
| Cell      | Cell      |   Cell    |     Cell  |

* * * 

# Empty cells

| Header 1  | Header 2  |
| --------- | --------- |
| A         | B         |
| C         |           |

Header 1  | Header 2
--------- | ---------
A         | B
          | D

* * *

# Missing tailing pipe

Header 1  | Header 2  
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- 
Cell      | Cell      |
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      
Cell      | Cell      |

Header 1  | Header 2  |
--------- | --------- |
Cell      | Cell      |
Cell      | Cell      

* * *

# Too many pipes in rows

| Header 1  | Header 2  |
| --------- 
| Cell      | Cell      | Extra cell? |
| Cell      | Cell      | Extra cell? |

+	this is a list item
	indented with tabs

+   this is a list item
    indented with spaces

Code:

	this code block is indented by one tab

And:

		this code block is indented by two tabs

And:

	+	this is an example list item
		indented with tabs
	
	+   this is an example list item
	    indented with spaces
> A list within a blockquote:
> 
> *	asterisk 1
> *	asterisk 2
> *	asterisk 3
Paragraph and no space:
* ciao

Paragraph and 1 space:
 * ciao

Paragraph and 3 spaces:
  * ciao

Paragraph and 4 spaces:
   * ciao

Paragraph before header:
#Header

Paragraph before blockquote:
>Some quote.
 .html
<ul>
    <li>Code block first in file</li>
    <li>doesn't work under some circumstances</li>
</ul>


As above: checking for bad interractions with the HTML block parser:

 html
<div>


Some *markdown* formatting.

 html
</div>


Some *markdown*


<div>
    <html>



function test();


<div markdown="1">
    <html>
        <title>
</div>

<div markdown="1">

<html>
    <title>

</div>

Two code blocks with no blank line between them:


<div>


<div>


Testing *confusion* with markers in the middle:


<div></div>


Testing mixing with title code blocks


<p>
 
<p>

 
<p>

<p>
 

<Fenced>


Code block starting and ending with empty lines:



<Fenced>




Indented code block containing fenced code block sample:

	
	<Fenced>
	

Fenced code block with indented code block sample:


Some text

	Indented code block sample code


Fenced code block with long markers:


Fenced


Fenced code block with fenced code block markers of different length in it:


In code block

Still in code block

Still in code block


Fenced code block with Markdown header and horizontal rule:


#test
---


Fenced code block with link definitions, footnote definition and 
abbreviation definitions:


[example]: http://example.com/

[^1]: Footnote def

*[HTML]: HyperText Markup Language


* In a list item with smalish indent:

  
  #!/bin/sh
  #
  # Preload driver binary
  LD_PRELOAD=libusb-driver.so $0.bin $*
  
  
With HTML content.
  

<b>bold</b>


Bug with block level elements in this case:

  <div>
  </div>


Indented code block of a fenced code block:

    
	haha!
	

With class:
  
html
<b>bold</b>

  
 html
<b>bold</b>

  
.html
<b>bold</b>

  
 .html
<b>bold</b>


With extra attribute block:

{.html}
<b>bold</b>

  
 {.html #codeid}
<b>bold</b>


 .html{.bold}
<div>

  
 .html {#codeid}
</div>
First line. <br/>
Second line.

This is a first paragraph,
on multiple lines.
     
This is a second paragraph.
There are spaces in between the two.This is a first paragraph,
on multiple lines.

This is a second paragraph
which has multiple lines too.A first paragraph.



A second paragraph after 3 CR (carriage return).This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
     
A few spaces and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.
	
1 tab to separate them and a new long long long long long long long long long long long long long long long long paragraph on 1 line.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line.

A new long long long long long long long long long long long long long long long long paragraph on 1 line.An ampersand & in the text flow is escaped as an html entity.There is an [ampersand](http://validator.w3.org/check?uri=http://www.w3.org/&verbose=1) in the URI.This is \*an asterisk which should stay as is.This is * an asterisk which should stay as is.\\   backslash
\   backtick
\*   asterisk
\_   underscore
\{\}  curly braces
\[\]  square brackets
\(\)  parentheses
\#   hash mark
\+   plus sign
\-   minus sign (hyphen)
\.   dot
\!   exclamation mark> # heading level 1
> 
> paragraph>A blockquote with a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.

>and a second very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long line.>This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a blockquote.> A blockquote
> on multiple lines
> like this.>A blockquote 
>on multiple lines 
>like this. >A blockquote
>on multiple lines
>like this.
>
>But it has
>two paragraphs.>A blockquote
>on multiple lines
>like this> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.
> This is the first level of quoting.
>
> > This is nested blockquote.> This is the first level of quoting.
> > This is nested blockquote.
> Back to the first level.
> This is the first level of quoting.
> > This is nested blockquote.
	10 PRINT HELLO INFINITE
	20 GOTO 10    10 PRINT < > &
    20 GOTO 10    10 PRINT HELLO INFINITE
    20 GOTO 10# Contributing to Mardown Test Suite

1. [Getting Involved](#getting-involved)
2. [Discussion](#discussion)
3. [How To Report an Issue](#how-to-report-an-issue)
4. [Editing Markdown Specification](#editing-markdown-specification)
5. [Test Suite Guidelines](#test-suite-guidelines)
6. [Pull Request Guidelines](#pull-request-guidelines)

## Getting Involved

There are a number of ways to get involved with the development of the Markdown Test Suite. If you are a first time contributor to an open source project, you can still add value to this project. You may identify grammar issues, write prose, examples or documentation for the project. You may flag some errors and open new issues.

Read all bits of this document and that will guide you on how to participate.

## Discussion

### Mailing List

The Markdown Test Suite has been started a little bit after the start of the [Markdown Community Group](http://www.w3.org/community/markdown/). You may want to discuss about Markdown and this project on the [group mailing-list](http://lists.w3.org/Archives/Public/public-markdown/).

## How to Report an Issue

Don't be afraid to add details to your issue. The more context you give, the better for people participating to the project. Make a short summary, add a description with the context and give links to places which will help to understand.

## Editing Markdown Specification

There is much needed work on the [Markdown Specification](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html). It doesn't require strong competences in coding. Be systematic in the markup and follow the way it is already organized. Each time you added a new atomic section, create a commit for this specific part.

## Test Suite Guidelines

When proposing new tests, make sure they do not already exist in the current test suite. You will notice that there is a separate section dedicated to the specific extensions that some markdown generators have created. Keep them separate. We want to keep the core clean and close to the original specification of Markdown.

If you are not sure, create an issue.

### Markdown Extensions

Markdown extension tests are accepted. Use the following rules:

- place all extension tests under the test/extensions/ENGINE directory with filename equal to the feature name
- for each ENGINE and add a README.markdown under the engine directory with a link to its specification

where ENGINE is either of:

- a command line utility. E.g. pandoc, kramdown.
- a programming API. E.g. Redcarpet::Markdown.new().
- a programmatically accessible web service. E.g.: GFM via the GitHub API.
- a non programmatically accessible web service. E.g.: Stack Overflow flavored markdown.

To avoid test duplication for common features, use the following rules:

- if file tests/extensions/ENGINE/FEATURE.md is empty or not present, use tests/extensions/FEATURE.md instead
- if file tests/extensions/ENGINE/FEATURE.out not present, use tests/extensions/FEATURE.out instead
- for a given ENGINE, only features which have either a .md or a .out are implemented by that engine.
- in case of different outputs for a single feature input, keep directly under extensions/ only the output case that happens across the most engines

**version**

Only the latest stable version of each ENGINE is considered.

**options**

The IO behavior tested is for engine defaults, without any options (command line options, extra JSON parameters, etc.) passed to the engine.

**external state**

Tests that use external state not present in the markdown input shall not be included in this test suite.

For example, what GFM @user user tags render to also depends on the state of GitHub's databases (only render to a link if user exists), not only on the input markdown.

#### Examples

GFM and the "fenced code block" use the following file structure:

    tests/extensions/gfm/README.markdown
    tests/extensions/gfm/fenced-code-block.md
    tests/extensions/gfm/fenced-code-block.out

where README.markdown contains:

    https://help.github.com/articles/github-flavored-markdown

To avoid duplication with other engines, if the input / output (normalized to DOM) is the same across multiple engines use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

If the input is the same, and outputs are DOM different, but represent the same idea (e.g. both represent computer code) use:

    tests/extensions/gfm/fenced-code-block.md       [empty]
    tests/extensions/gfm/fenced-code-block.out
    tests/extensions/fenced-code-block.md
    tests/extensions/fenced-code-block.out

#### New Extensions

Tests are modular, and if you want to test a new engine for your project, that should be easy to do.

If you feel that the new engine is reasonably popular, please send a pull request adding it.

## Commits and Pull Requests

* Keep your commits clean and commented
* Do not mix in one commit different things. Keep modifications related.
* Do not mix everything in one giant pull request. Create separate pull requests for different topic. That will help to have a more meaningful debate about the pull requests and will help to review the code.
* If it relates to a specific issue, add the number of the issue in the commit message.

Thanks for Contributing
as*te*risks*single asterisks*_single underscores_HTML entities are written using ampersand notation: &copy;These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

These lines all end with end of line (EOL) sequences.

Seriously, they really do.

If you don't believe me: HEX EDIT!

This is an H1
=============# This is an H1 # # This is an H1# this is an h1 with two trailing spaces  
A new paragraph.# This is an H1This is an H2
-------------## This is an H2 #### This is an H2### This is an H3 ###### This is an H3#### This is an H4 ######## This is an H4##### This is an H5 ########## This is an H5###### This is an H6  ############ This is an H6- - ----***___-------![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 for everyone"![HTML5][h5]

[h5]: http://www.w3.org/html/logo/img/mark-word-icon.png![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png "HTML5 logo for everyone")![HTML5](http://www.w3.org/html/logo/img/mark-word-icon.png)We love <code> and & for everything We love code for everything We love code for everything The MIT License (MIT)

Copyright (c) 2013 Karl Dubost

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
A first sentence  
and a line break.A first sentence     
and a line break.This is an automatic link <http://www.w3.org/>[W3C](http://www.w3.org/ "Discover w3c")[W3C](http://www.w3.org/)[World Wide Web Consortium][w3c]

[w3c]: <http://www.w3.org/>[World Wide Web Consortium][]

[World Wide Web Consortium]: http://www.w3.org/[w3c][]

[w3c]: http://www.w3.org/[World Wide Web Consortium] [w3c]

[w3c]: http://www.w3.org/[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/
   "Discover W3C"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ (Discover w3c)[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ 'Discover w3c'[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/ "Discover w3c"[World Wide Web Consortium][w3c]

[w3c]: http://www.w3.org/*   a list containing a blockquote

    > this the blockquote in the list* a

        b
*   a list containing a block of code

	    10 PRINT HELLO INFINITE
	    20 GOTO 10*   This is a list item with two paragraphs. Lorem ipsum dolor
	sit amet, consectetuer adipiscing elit. Aliquam hendrerit
	mi posuere lectus.

	Vestibulum enim wisi, viverra nec, fringilla in, laoreet
	vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
	sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.*   This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

*   Suspendisse id sem consectetuer libero luctus adipiscing.1\. ordered list escape1. 1

    - inner par list

2. 2
1. list item 1
8. list item 2
1. list item 31. list item 1
2. list item 2
3. list item 3This is a paragraph
on multiple lines
with hard return.This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph on 1 line. This is a paragraph with a trailing and leading space. This is a paragraph with 1 trailing tab.	  This is a paragraph with 2 leading spaces.   This is a paragraph with 3 leading spaces. This is a paragraph with 1 leading space.This is a paragraph with a trailing space. # Colophon - October 1st, 2014

This project was initiated to provide a test suite for Markdown markup, and eventually create a specification from this test results. A part of of the community has started a new endeavor which seems to get traction as [CommonMark](https://github.com/jgm/stmd). **We are then closing this project** and encourage you to contribute to CommonMark. 

The most interesting part of this project would not have been possible without the dedication of [Ciro Santilli](https://github.com/cirosantilli) @cirosantilli. So big applause and thank you to him.


The rest is kept around for archives and references.

# Markdown Test Suite

Inspired by questions on [W3C Markdown Community Group](http://www.w3.org/community/markdown).

Pull Requests are welcome. See the [CONTRIBUTING Guidelines](https://github.com/karlcow/markdown-testsuite/blob/master/CONTRIBUTING.md)

## Design goals

- Comprehensive.
- Small modularized tests.
- Easy to run tests using any programming language. In particular, data representations must have an implementation on all major languages.
- Develop a consensus based markdown specification at [markdown-spec.html](markdown-spec.html). Visualize it [here](http://htmlpreview.github.io/?https://github.com/karlcow/markdown-testsuite/blob/master/markdown-spec.html).

## Test Scripts

Markdown Test Suite already includes tests for many important markdown engines.

To see what the scripts do run:

    ./cat-all.py -h
    ./run-tests.py -h

To configure the scripts do:

	cp config_local.py.example config_local.py

and edit config_local.py. It is already gitignored.

A Vagrantfile is provided with a provision script that installs all installable engines.

Sample output from run-tests.py:

    blackfriday   |......FFF..............FF...F....................................F....................................|   0.93s  102    7   6%
	gfm           |FF.....F.....F...FFFF..F....F........................FFFF...FF...............FF...F.......F...........| 262.88s  102   20  19%
    hoedown       |..............................F.................................................F.....................|   0.36s  102    2   1%
	kramdown      |......FFF.....FF.......FF.......FF.FFFFFFFFFFFFF.......................F..............................|  30.69s  102   23  22%
    lunamark      |FFFFFF.F.FFFFFFFFFFFF.F.....FFFF..FF............FFFFF..FFFFFFFFFF..............F...FFFFFFFFFFF........|   1.58s  103   53  51%
    markdown_pl   |.....................FFFF...............................F...............F.............................|   2.56s  102    6   5%
    markdown2     |......................................................................................................|   5.39s  103    0   0%
    marked        |..............F.................FFFFFFFFFFFFFFFF......................F.F.............................|   6.22s  102   19  18%
    maruku        |......FFF......F.......F.FFF...............................................FF.........................|  37.02s  102   10   9%
    md2html       |.........................FFF...F............................................FF........................|   7.42s  102    6   5%
    multimarkdown |......FFF....FF...F............FFF.FFFFFFFFFFFFF.....FFFF.........F...................................|   0.58s  102   27  26%
    pandoc        |FF...........F.F.FFFF..FFFFF....FF.FFFFFFFFFFFFF.....FFFF.....FF............FFF.FFF..................F|   1.11s  102   41  40%
    peg_markdown  |.................................................................F....................................|   0.46s  102    1   0%
    rdiscount     |.......F.........................................................F....................................|  25.19s  102    3   2%
    redcarpet     |......................................................................................................|  21.49s  102    0   0%
    showdown      |.......................................................................F..............................|   6.85s  102    1   0%

	Extensions:

    blackfriday   |F..|  0.04s    3    1  33%
	gfm           |F.|   2.37s    2    1  50%
    hoedown       |.|    0.00s    1    0   0%
    lunamark      |F.F|  0.05s    3    2  66%
    kramdown      |..|   0.62s    2    0   0%
    markdown_pl   ||     0.00s    0    0   0%
    markdown2     |F.|   0.14s    2    1  50%
    marked        |F.|   0.13s    2    1  50%
    maruku        |F..|  1.06s    3    1  33%
    md2html       |F.|   0.14s    2    0   0%
    multimarkdown |F.|   0.01s    2    1  50%
    pandoc        |F.|   0.02s    2    1  50%
    peg_markdown  |...|  0.02s    3    0   0%
    rdiscount     |F..|   0.74s    3    1  33%
    redcarpet     |..|   0.42s    2    0   0%
    showdown      |F..|  0.20s    3    1  33%

Where F indicates a failing test.

## Other Noticeable Test Suites

We haven't been the first test suite effort. Some projects have maintained their own test suite for a long time. Hopefully we can reach a state where people agree on the terms of what should be a good test suite for all developers.

- [Original test suite](http://daringfireball.net/projects/downloads/MarkdownTest_1.0.zip)
- [PHP markdown test suite:](https://github.com/michelf/mdtest/tree/master/Markdown.mdtest)
- [Markdown-js test suite](https://github.com/evilstreak/markdown-js/tree/master/test/features)
- [Python markdown 2 test suite](https://github.com/trentm/python-markdown2/tree/master/test/tm-cases)
- [multimarkdown test suite](https://github.com/fletcher/MMD-Test-Suite)
- [John MacFarlane's Standard Markdown spec](https://github.com/jgm/stmd)

In addition we should note the [wonderful work](http://johnmacfarlane.net/babelmark2/) made by John Mac Farlane. The Web service output the differences in between the different markdown implementations. It helps a lot when searching on the most common output.
as**te**risks**double asterisks**__double underscores__* list item 1
* list item 2
* list item 3
- list item 1
- list item 2
- list item 3 * list item 1
 * list item 2
 * list item 3  * list item 1
  * list item 2
  * list item 3   * list item 1
   * list item 2
   * list item 3+ list item 1
+ list item 2
+ list item 3* list item in paragraph

* another list item in paragraph*   This a very long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long long paragraph in a list.
*   and yet another long long long long long long long long long long long long long long long long long long long long long long line.*   This is a list item
    with the content on
    multiline and indented.
*   And this another list item
    with the same prin
