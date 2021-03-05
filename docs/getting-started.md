# Getting Started

## Welcome to the Developer Portal!

To onboard properly into the Fiserv Developer Portal as a tenant each product must support these APIs so that we can retrieve product specific API specifications and documentation.

# Using Markdown in Documentation

### What is Markdown?
>Markdown is a text-to-HTML conversion tool for web writers.

>Markdown allows you to write using an easy-to-read, easy-to-write plain text format, then convert it to structurally valid XHTML (or HTML).

For example, this entire page was created using Markdown!

Below is a quick reference of all the Markdown syntax that is supported by Stoplight.

### Table of Contents  
* [Headers](#headers)
* [Emphasis](#emphasis)  
* [Lists](#lists)  
* [Links](#lnks)  
* [Images](#imgs)  
* [Code and Syntax Highlighting](#code)  
* [Tables](#tables)  
* [Blockquotes](#blockquotes)   
* [Horizontal Rule](#hr)

## <a name="headers"/>  Headers

```no-highlight
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

# H1
## H2
### H3
#### H4
##### H5
###### H6

## <a name="emphasis"/> Emphasis

```no-highlight
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~
```

Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~

## <a name="lists"/> Lists

>In this example, leading and trailing spaces are shown with with dots: ⋅⋅⋅

```no-highlight
1. First ordered list item
2. Another item
   ..- Unordered sub-list
3. Actual numbers don't matter, just that it's a number
   ..1. Ordered sub-list
4. And another item

...You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).
```

1. First ordered list item
2. Another item
     - Unordered sub-list
3. Actual numbers don't matter, just that it's a number
     1. Ordered sub-list
4. And another item

   You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

## <a name="lnks"/> Links

There are four ways to create links.

```no-highlight
1. To link Inline-style
[I'm an inline-style link](https://www.google.com)

2. To link Reference-style
[I'm a reference-style link][https://www.google.com "Google's Homepage"]

3. To link to API explorer from documentation pages
[API page](../api?type=post&path=/v1/apis)

4. To link/reference to another document/markdown
[Charge](?path=docs/Transactions/Charges.md)
```
1. To link Inline-style<br />
[I'm an inline-style link](https://www.google.com)

2. To link Reference-style<br />
[I'm a reference-style link][https://www.google.com "Google's Homepage"]

3. To link to API explorer from documentation pages<br />
[API page](../api?type=post&path=/v1/apis)

4. To link/reference to another document/markdown<br />
[Charge](?path=docs/Transactions/Charges.md)

## <a name="imgs"/> Images

```no-highlight
Here's our logo (hover to see the title text):

![Fiserv Logo](http://dev-dev-portal-ui-dev-developer-portal.roks-eck-cluster-8a571839bba611238ae425f409ae5396-0000.us-south.containers.appdomain.cloud/assets/img/fiserv_logo_orange_rgb.png "Fiserv Logo")
```

Here's our logo (hover to see the title text):

![Fiserv Logo](http://dev-dev-portal-ui-dev-developer-portal.roks-eck-cluster-8a571839bba611238ae425f409ae5396-0000.us-south.containers.appdomain.cloud/assets/img/fiserv_logo_orange_rgb.png "Fiserv Logo")

## <a name="code"/> Code and Syntax Highlighting

Inline `code` has `back-ticks around` it.

>In the examples below, remove the three back-ticks <code>```</code> at the start and end of the javascript code fence before using.

<pre><code>```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 </code></pre>

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
>Use language tags to change the syntax highlighting:

<pre><code>```json
{
  "JSON": "Syntax Highlighting"
}
```
</code></pre>

```json
{
  "JSON": "Syntax Highlighting"
}
```

## <a name="tables"/> Tables

Tables aren't part of the core Markdown spec, but they are part of GFM and *Markdown Here* supports them. They are an easy way of adding tables to your email -- a task that would otherwise require copy-pasting from another application.

```no-highlight
Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
```

Colons can be used to align columns.

| Tables        | Are           | Cool |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

The outer pipes (|) are optional, and you don't need to make the raw Markdown line up prettily. You can also use inline Markdown.

| Markdown | Less | Pretty |
| --- | --- | --- |
| *Still* | `renders` | **nicely** |
| 1 | 2 | 3 |

## <a name="blockquotes"/> Blockquotes

```no-highlight
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote. 
```

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote. 

## <a name="hr"/> Horizontal Rule

```
Three or more...

---

Hyphens

***

Asterisks

___

Underscores
```

Three or more...

---

Hyphens

***

Asterisks

___

Underscores

## Fiserv GitHub Account Details

[Fiserv-GitHub](https://github.com/Fiserv)

## Fiserv Stoplight Account Details

[Fiserv-Stoplight](https://fiserv-portal.stoplight.io/)

>> Please reach out to [Alvin Cho](mailto:alvin.cho@fiserv.com) for both GitHub/Stoplight account access(es).
