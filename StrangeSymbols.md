Markdown syntax guide

Bitbucket Server uses Markdown for formatting text, as specified in CommonMark (with a few extensions). You can use Markdown in the following places:

    any pull request's descriptions or comments, or
    in README files (if they have the .md file extension).

Use Control-Shift-P or Command-Shift-P to preview your markdown.

Markdown syntax

The page below contains examples of Markdown syntax. For a full list of all the Markdown syntax, consult the CommonMark help or specification.
On this page:

    Markdown syntax
        Headings
        Paragraphs
        Character styles
        Unordered list
        Ordered list
        List in list
        Quotes or citations
        Inline code characters
        Code blocks
        Links to external websites
        Linking issue keys to JIRA applications
        Linking to pull requests
        Images
        Tables
    Backslash escapes
    README files

Headings
1

# This is an H1

2

## This is an H2

3

###### This is an H6

4

​

5

This is also an H1

6

==================

7

​

8

This is also an H2

9

------------------

Paragraphs

1

Paragraphs are separated by empty lines. Within a paragraph it's possible to have a line break,

2

simply press <return> for a new line.

3

​

4

For example,

5

like this.

Character styles

1

*Italic characters* 

2

_Italic characters_

3

**bold characters**

4

__bold characters__

5

~~strikethrough text~~

Unordered list

1

* Item 1

2

* Item 2

3

* Item 3

4

  * Item 3a

5

  * Item 3b

6

  * Item 3c

Ordered list

1

1. Step 1

2

2. Step 2

3

3. Step 3

4

   1. Step 3.1

5

   2. Step 3.2

6

   3. Step 3.3

List in list

1

1. Step 1

2

2. Step 2

3

3. Step 3

4

   * Item 3a

5

   * Item 3b

6

   * Item 3c

Quotes or citations

1

Introducing my quote:

2

​

3

> Neque porro quisquam est qui 

4

> dolorem ipsum quia dolor sit amet, 

5

> consectetur, adipisci velit...

Inline code characters

1

Use the backtick to refer to a `function()`.

2

 

3

There is a literal ``backtick (`)`` here.

Code blocks

1

Indent every line of the block by at least 4 spaces.

2

​

3

This is a normal paragraph:

4

​

5

    This is a code block.

6

    With multiple lines.

7

​

8

Alternatively, you can use 3 backtick quote marks before and after the block, like this:

9

​

10

```

11

This is a code block

12

```

13

​

14

To add syntax highlighting to a code block, add the name of the language immediately

15

after the backticks: 

16

​

17

```javascript

18

var oldUnload = window.onbeforeunload;

19

window.onbeforeunload = function() {

20

    saveCoverage();

21

    if (oldUnload) {

22

        return oldUnload.apply(this, arguments);

23

    }

24

};

25

```

Bitbucket Server uses CodeMirror to apply syntax highlighting to the rendered markdown in comments, READMEs and pull request descriptions. All the common coding languages are supported, including C, C++, Java, Scala, Python and JavaScript. See Configuring syntax highlighting for file extensions.

Within a code block, ampersands (&) and angle brackets (< and >) are automatically converted into HTML entities.
Links to external websites

1

This is [an example](http://www.example.com/) inline link.

2

​

3

[This link](http://example.com/ "Title") has a title attribute.

4

​

5

Links are also auto-detected in text: http://example.com/

Linking issue keys to JIRA applications

When you use JIRA application issue keys (of the default format) in comments and pull request descriptions Bitbucket Server automatically links them to the JIRA application instance.

The default JIRA application issue key format is two or more uppercase letters ([A-Z][A-Z]+), followed by a hyphen and the issue number, for example TEST-123.

Linking to pull requests

Introduced with Bitbucket Server 4.9, you can reference pull requests from comments and descriptions in other pull requests. The syntax for linking to pull request looks like this: 

1

projectkey/repo-slug#pr_id

To link to a pull request in the same project and repository, you only need to include the pull request ID. 

1

#123

To link to a pull request in the same project but a different repository, include the repository slug before the pull request ID.

1

example-repo#123

To link to a pull request in a different project and repository, include the project key and the repository slug before the pull request ID.

1

PROJ/example-repo#123

 
Images

Inline image syntax looks like this:

1

![Alt text](/path/to/image.jpg)

2

![Alt text](/path/to/image.png "Optional title attribute")

3

![Alt text](/url/to/image.jpg)

For example:

1

...

2

![Mockup for feature A](http://monosnap.com/image/bOcxxxxLGF.png)

3

...

Reference image links look like this:

1

![Alt text][id]

where 'id' is the name of a previously defined image reference, using syntax similar to link references:

1

[id]: url/to/image.jpg "Optional title attribute"

For example:

1

...

2

<--Collected image definitions-->

3

[MockupA]: http://monosnap.com/image/bOcxxxxLGF.png "Screenshot of Feature A mockup" 

4

...

5

<!--Using an image reference-->

6

![Mockup for feature A][MockupA]

7

...

Tables

1

| Day     | Meal    | Price |

2

| --------|---------|-------|

3

| Monday  | pasta   | $6    |

4

| Tuesday | chicken | $8    |

Backslash escapes

Certain characters can be escaped with a preceding backslash to preserve the literal display of a character instead of its special Markdown meaning. This applies to the following characters:

\  backslash
`  backtick
*  asterisk
_  underscore
{} curly braces
[] square brackets
() parentheses
#  hash mark
>  greater than
+  plus sign
-  minus sign (hyphen)
.  dot
!  exclamation mark
README files

If your repository contains a README.md file at the root level, Bitbucket Server displays its contents on the repository's Overview page if the file has the .md extension. The file can contain Markdown and a restricted set of HTML tags.
