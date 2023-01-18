# WCAG 2.1

## About This Document:

These are my notes from amazing the Web Content Accessibility Guidelines udemy course by Ross Mullen (director of CANAXESS).

https://www.udemy.com/course/introduction-to-web-accessibility-wcag21/


## **What is it:**

The Web Content Accessibility Guidelines are part of a series of web accessibility guidelines published by the Web Accessibility Initiative of the World Wide Web Consortium, the main international standards organisation for the Internet.

## **Who is it for:**

Not only for the blind and visually impaired, also for people with learning difficulties, short term memory issues, and so on.

## **Conformancy:**

**A:** basic accessibility aids - easy to add

**AA:** mid accessibility aids - so so to add

**AAA:** advanced aids- difficult to add

## **Four Principles of accessibility: POUR**

**Perceivable** : The user can access the content/ information AND interface

**Operable** : The user can access use the site and it's features

**Understandable** : The user can understand the content/ information AND interface

**Robust** : The site can be used by assistive tech (screen readers, etc)

## **Each POUR principle has:**

**Several success criteria** :

**Sufficient techniques** :

**Failure criteria** : ways to test content to see if it passes/ fails

## **Examples of codes:**

**h55** : H = html guild

**c12** : C = css guild

**g88** : G = general

**aria54:** aria = aria screen readers

**scr13** : scr = client side script techniques (usually javascript)

----------------------------

## **Descriptive Page Tiles Examples:**

**document** : the default webpage name

**About** : the name of the page

**Facebook** : the site name

**About Facebook** : The site name and page

## **Page Language:**

**lang=en** :

- declare the language in the head
- This can be used for individual elements too! _ **\<p lang=es\>Hola!\</p\>** _

**lang=en-au** :

- There are regional differences too

## **Bypass Repeating Content:**

**What is it:**

When uses press tab to circle through elements, users should be able to skip repeated content like a navbar.

**How:**

BEFORE the repeated content, have a \<a href="#content"\> to link to AFTER the repeated content.
**Tips:**

- don't use this more than 3 or 4 times per page

- the skip link can be hidden/ or placed out of the visible site so its only noticed when 'tab' is pressed

## **Headings:**

**|\<h1\>** Only ONE on a page, it's the title

|

|-- **\<h2\>** a heading

|----- **\<h3\>** sub-heading of \<h2\>

|----- **\<h3\>** sub-heading of \<h2\>

|----- **\<h3\>** sub-heading of \<h2\>

|-------- **\<h4\>** sub-heading of \<h3\>

|----- **\<h3\>** sub-heading of \<h2\>

|

|-- **\<h2\>** a heading

|----- **\<h3\>** sub-heading of \<h2\>

\*Never skip a heading!

\*\* Must be a h1!

\*\*\* Must be in sequence

\*\*\*\* Use as many headings as needed

## **Landmark Region tags:**

**What is it:**

They wrap around sections of the html to show regions. Only relevant to the screen readers etc

**Main ones:**

- **\<header\>**
- **\<footer\>**
- **\<main\>** only one main region per page! Not nested in an article, prominent unique text
- **\<article\>** complete content, can nest other articles
- **\<nav\>**


## **TabIndex:**

**What is it:**

Change the order of what is selected when tab is pressed

**Values:**

**tabindex="-1"** not selected by tab
**tabindex="0"** adds element to the default and natural flow of tab selection

**tabindex="1"(and above)** the sequence changing this is messy! **NEVER USE!**

**Some DON'T have tab index:**

\<div\> and \<span\>

----------------------------

## **Colour Contrast:**

**AA Guidelines are Confusing and strict!:**

Contrast ratios, expectation clauses, large and small text (all overlap)

**Useful tool:**

CCA, an eyedrop tool that allows you to check the contrast between text and background

## **Images- Decorative & Descriptive:**

**Decorative:**

An image that isn't important and doesn't need to be read by a screen reader.

**Alt=""**

**Descriptive:**

An image that should be explained. Not longer than a sentence and not too short!

Eg:

![](RackMultipart20230118-1-h3ig73_html_9ca00a7c3db6bfae.png)

**alt="a blue sports car driving fast on a mountainous desert road"**

## **Semantic Elements:**

Reply less on **\<div\>** and **\<span\>** and more on descriptive elements.

**Common Semantic Elements:**

**\<h1\> +
 \<ol\> \<ul\>
 \<blockquote cite="source of quote"\>**

**\<em\>** adds stress to word

**\<header\> \<footer\> \<main\> \<article\> \<nav\>**

**\<time datetime="2022-03-26"\>March 26 \</time\>** \*must match!
 **\<address\>**

## **Keyboard & Mouse Focus:**

The default focus on an element is often not enough and differs between browsers.

**For best results example with \<a\>:**

**a:focus,a:hover{**

**border: 3px solid blue;**

**Text-decoration: underline; //or this instead**

**}**

**For best results with input:**

**Input:focus, select:focus, textarea:focus, button:focus,**

**input:hover, select:hover, textarea:hover, button:hover**

**{**

**border: 3px solid blue;**

**}**

\*mouse and keyboard must be the same!

\*\* high contrast too!

## **Link Text:**

Clear link text is very important and is AAA.

Examples:

**CLICK HERE** _for contact us_

^ separate elements means that the screen reader will only read "click me"

**CLICK HERE** _ **for contact us** _

^ screen reader will read the entire thing… but "click here" will be repetitive!

Also, the links are displayed alphabetically to screen readers

_ **for contact us** _

^ This is best

## **Group related lists:**

Grouping lists with \<ul\> or \<ol\> if you want the screen reader to get the meta data, not always needed.
 eg:

**\<ul\>** ="list with 2 items"

**\<li\>Contact us\</li\>** = "bullet item a, contact us"

**\<li\>About us\</li\>** = "bullet item b, about us"

**\</ul\>**

**\<ol\>** ="list with 2 items"

**\<li\>Contact us\</li\>** = "1 bullet item a, contact us"

**\<li\>About us\</li\>** = "2 bullet item b, about us"

**\</ol\>**

\*DON'T OVER USE THIS! It adds to the audio overhead and bores the user

**Tables:**

Always use **\<th\> \<td\>** correctly!

After **\<table\>** use **\<caption\>** to describe the table

-------------------------------------

## **Labels for inputs:**

Always use a label with id and link to the input id

Eg:

**\<label for="first-name-id"\>First name\</label\>**

**\<input id="first-name-id"/\>**

\* Button and images don't need labels

\*\* Extra advantage: clickable area is now bigger

## **Data Formats for inputs:**

Write the restraints in the label so they are read to the user.

**\<label for="first-name-id"\>** First name (20 characters max) **\</label\>**

**\<input id="first-name-id" max="20"/\>**

**\<label for="DoB"\>** Date of Birth (dd/mm/yy) **\</label\>**

**\<input id="DoB" /\>**

\* Keep it short

## **Highlight "Required" fields:**

The default for a mandatory field on a form is small red \*

A better way is to include (required) in the label.

Eg:

**\<label for="DoB"\>** Date of Birth (dd/mm/yy)(required) **\</label\>**

**\<input id="DoB" /\>**

\*don't use (optional) as it's just extra noise

## **Grouping related inputs:**

It's a good idea to group related inputs using **\<fieldset\>** and **\<legend\>**

Eg:

**\<fieldset\>**

**\<legend\>** Name **\</legend\>**

**\<label for="first-name-id"\>** First name (20 characters max) **\</label\>**

**\<input id="first-name-id" max="20"/\>**

**\<label for="second-name-id"\>** Second name (20 characters max) **\</label\>**

**\<input id="second-name-id" max="20"/\>**

**\<label for="middle-name-id"\>** middle name (20 characters max) **\</label\>**

**\<input id="middle-name-id" max="20"/\>**

**\</fieldset\>**

\*most important on **type="radio"** or **type="checkbox"**

## **Inline error messages:**

When data in an input field is wrong, have an error message with the **\<label\>** appear (but unhiding it with class="")

Eg:

**\<label for="first-name-id"\>** First name (20 characters max)

**\<p class="hide"\>** First name is empty **\</p\>**

**\</label\>**

**\<input id="first-name-id" max="20"/\>**

\*never use it alone, use _Validation Summary_ too!

## **Inline error messages + Suggestions!:**

Try to always of a way to fix the error

Eg:

**\<label for="first-name-id"\>** First name (20 characters max)

**\<p class="hide"\>** First name error **\</p\>**

**\</label\>**

**\<input id="first-name-id" max="20"/\>**

**\<label for="first-name-id"\>** First name (20 characters max)

**\<p class="hide"\>** First name is empty, must be better 3 and 20 characters **\</p\>**

**\</label\>**

**\<input id="first-name-id" max="20"/\>**

## **Validation Summary:**

After the user submits a form that has errors, they should be sent back to the form and be given a summary.

- Use **\<ol\>** or **\<ul\>** so they can see how many errors
- Describe the errors
- The error section should stand out (red?)
- If the page is reloading the use # to target the error section so they don't have to tab constantly

Eg:

**\<h2\>** Validation summary **\</h2\>**

**\<ul\>
 \<li\>First name is too long\</li\>**

**\<li\>Date of birth wrong format\</li\>**

**\<li\>Address empty\</li\>**

**\</ul\>**

**\<form\>**

…
