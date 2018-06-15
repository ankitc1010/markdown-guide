# Markdown Guide

The purpose of this is for **quick reference** to various elements of markdown and the **best practices** on how they can be applied.

I wanted to better contribute to projects on **Github**. Thats why I learned _markdown_. Hope this documentation is of good help to you too. 😀 👍 

## Table of Contents

>[1. Heading 🤩][head]<br>
>[2. Bold, Italic and Strike Through 👐][bis]<br>
>[3. Linking 🔗][link]<br>
>[4. Images 🖼][img]<br>
>[5. Lists ᬮ][list]<br>
>[6. LineBreaks, Horizontal Rules and BlockQuotes 🍳][lhb]<br>
>[7. Code Blocks and Syntax High Lighting 🔆][cbshl]<br>
>[8. Tables 🍽][tab]<br>
>[9. Checkbox 🧠][check]<br>
>[10. Github Treats 🎁][githubtreats]<br>
>[11. Special Thanks ][thank]


[head]: #1-headings-
[bis]: #2-bold-italic-and-strike-through-
[link]: #3-linking-
[img]: #4-images-
[list]: #5-lists-ᬮ
[lhb]: #6-linebreaks-horizontal-rules-and-blockquotes-
[cbshl]: #7-code-blocks-and-syntax-high-lighting-
[tab]: #8-tables-
[check]: #9-checkbox-
[githubtreats]: #10-github-treats-
[thank]: #11-special-thanks

## 1. Headings 🤩

To make headings we use # symbol, and the number of # symbol determine the order of headings.<br>
With _#_ being the most important heading and _######_ being the least important heading.

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
##### This is heading 5
###### This is heading 6
```

>#### Result
>
># This is heading 1
>## This is heading 2
>### This is heading 3
>#### This is heading 4
>##### This is heading 5
>###### This is heading 6

---
---

## 2. Bold, Italic and Strike Through 👐

### Bold

To make text bold use the ** symbol.

```markdown
This is **bold**
```

>#### Result
>
>This is **bold**

---

### Italic

To make text italic use the _ symbol.

```markdown
This is _italic_
```

>#### Result
>
>This is _italic_

---

### Strike Through

To make a strikethrough use the ~~ symbol.

```markdown
This is ~~strikethrough~~
```

>#### Result
>
>This is ~~strikethrough~~

---
---

## 3. Linking 🔗

### Basic

In order to make a site clickable just encapsulate it using <> symbol.

```markdown
<https://www.google.co.in>
```

>#### Result
>
><https://www.google.co.in>

---

### Old School 

In order to link a particular text to another document use the following snippet

```markdown
A link to [Google](https://www.google.co.in)
```

>#### Result
>
>A link to [Google](https://www.google.co.in)

---

### Old School with Title text
In order to attach a Title Text(i.e. on hover the title text appears in the form of a tooltip).


```markdown
A link to [Ankit's Github Account](https://github.com/ankitc1010, "Check out his awesome repositories")
```

>#### Result
>
>A link to [Ankit's Github Account](https://github.com/ankitc1010, "Check out his awesome repositories")

---

### Recommended Method

In order to create maintainable documentation assign a variable to the link specified and set its value at the bottom of the document.

```markdown
[Github][1] is an awesome place. In [Github][1] you can do awesome stuff.
Literally you can contribute to the open world projects of the organizations like [facebook][face], [google][goo], etc.
[Github][1] has now been acquired by [Microsoft][micro].

[1]: https://github.com
[face]: https://facebook.com
[goo]: https://google.co.in "Google Title Text 🕶"
[micro]: https://microsoft.com
```

>#### Result
>
>[Github][1] is an awesome place. In [Github][1] you can do awesome stuff.
Literally you can contribute to the open world projects of the organizations like [facebook][face], [google][goo], etc.<br>
[Github][1] has been acquired by [Microsoft][micro].

[1]: https://github.com
[face]: https://facebook.com
[goo]: https://google.co.in "Google Title Text 🕶"
[micro]: https://microsoft.com

---
---
## 4. Images 🖼

### Oldschool Method

This is used to add images to your document.

```markdown
![This is the default text which is displayed if the image fails to load and can be left blank!](https://unsplash.it/500/500?random "This is Title Text")
```

>#### Result
>
>![This is the default text which is displayed if the image fails to load and can be left blank!](https://unsplash.it/200/200?image=1019 "This is Tooltip and can be omitted altogether")

---

### Recommended Method

This is the recommended method to add image.

```markdown
![Cute Image][image]

[image]: https://unsplash.it/200/200?image=1012 "Image Title Text"
```

>#### Result
>
>![Ocean Image][ocean]

[ocean]: https://unsplash.it/200/200?image=1015 "Image Title Text 🐥"

---

### Using Nested Link

In this a smaller image is referring to its bigger resolution counterpart.

```markdown
[![](https://unsplash.it/50/50?image=1015)](https://unsplash.it/200/200?image=1015)
```

>#### Result
>
>[![](https://unsplash.it/50/50?image=1015)](https://unsplash.it/200/200?image=1015)

---

### Using HTML Tag in Nested Link

You can use html image tag in the above example and it will work the same.

```markdown
[<img src="https://unsplash.it/50/50?image=1015" alt='image'/>](https://unsplash.it/200/200?image=1015)
```

>#### Result
>
>[<img src="https://unsplash.it/50/50?image=1015" alt='image'/>](https://unsplash.it/200/200?image=1015)

---

### Using only HTML Tags To Display Image

There are limitations with respect to styling in markdown, so HTML can be used and corressponding style tags can also be added.

There is an update that Chrome and Firefox doesnt render < style /> tags. But they render inline styles.

```markdown
<img src="https://unsplash.it/500/500?image=1015" alt='cool image' style="width: 200px; height: 200px; border-radius: 200px;"/>
```

>#### Result
>
><img src="https://unsplash.it/500/500?image=1015" id='cool' alt='cool image' style="width: 200px; height: 200px; border-radius: 200px;"/>

<style
  type="text/css">
#cool { border-radius: 200px;}
</style>

---
---

## 5. Lists ᬮ

### Ordered List

Here is a code snippet for writing the nested and normal list. Best practice is we use only 1. to order them, the markdown parser will automatically number them accordingly.

```markdown
The awesome people in the world -<br>

1.  Wes Bos
    1.  Great
    1.  Awesome
1.  Dan Abramov
1.  Kent C. Dodds
```

>#### Result
>
>The awesome people in the world -<br>
1.  Wes Bos
    1.  Great
    1.  Awesome
2.  Dan Abramov
3.  Kent C. Dodds

---

### Unordered List

For unordered list we use either +, *, -.

It is the best practice to change the sign when using nested list.

```markdown
The awesome people in the world -

- Wes Bos
  * Great
  * Awesome
- Dan Abramov
- Kent C. Dodds
```

>#### Result
>
>The awesome people in the world -

- Wes Bos
  * Great
  * Awesome
- Dan Abramov
- Kent C. Dodds

---
---

## 6. LineBreaks, Horizontal Rules and BlockQuotes 🍳

### Line Breaks

In order to break the line either use Double Line Enter or use < br > tag.

```markdown
First came React. <br>
Then came Preact.

or

First came React.

Then came Preact.
```

>#### Result
>First came React. <br>
>Then came Preact.
>
>or
>
>First came React.
>
>Then came Preact.

---

### Horizontal Rules

This is used to draw lines in between.

```markdown
DownRule. 🏎

---

Advanced React.

---
```

>#### Result
>
>DownRule. 🏎
>
>---
>
>Advanced React.
>
>---

---

### BlockQuotes

```markdown
> To Be, Or Not To Be. 😹
>
> **- Tommy Wiseau**
```

>#### Result
>
>> To Be, Or Not To Be. 😹
>>
>> **- Tommy Wiseau**

---
---

## 7. Code Blocks and Syntax High Lighting 🔆

### Code Blocks

To write code blocks use ``` to start, followed by which language that code belongs to and ` for inlining the code.

```markdown
    ```javascript
    const amIRockstar = true
    ```

    Hey did you mean `var name = 'Ankit'`? 
```

>#### Result
>
>```javascript
>const amIRockstar = true
>```
>
> Hey did you mean `var name = 'Ankit'`? 

--- 

### Syntax Highlight

If you are telling someone to delete and add a line, you can use diff.

```markdown
    ```diff
    var a = 100;
    - var b = 'Barack Obama';
    + var b = 'Wes Bos';
    ```
```

>#### Result
>
>```diff
>var a = '100';
>- var b = 'Barack Obama';
>+ var b = 'Wes Bos';
>```

---
---

## 8. Tables 🍽

Tables can be made easily by using |. And one align the text based on the position of the :.

```markdown
| S. No. | Title | Description |
| :----- | :---: | ----------: |
| 1.     | Cool  | Thats cool  |
| 2.     | hey   | hey         |
```

>#### Result
>
>|S. No.| Title | Description |
>|:-----|:-----:|------------:|
>|1.| Cool | Thats cool|
>|2.| hey | hey |

---
---

## 9. Checkbox 🧠

We can make checkboxes in markdown using [ ] brackets.

```markdown
To Do List - 
* [ ] Be a Public Speaker 🤓
* [x] Be an Experienced React Developer 😎
* [ ] Learn to play Guitar 🎸
```

>#### Result
>To Do List - 
* [ ] Be a Public Speaker 🤓
* [x] Be an Experienced React Developer 😎
* [ ] Learn to play Guitar 🎸

---
---

## 10. Github Treats 🎁

You can reference pull requests and issues using # symbol. And you can tag people using @ symbol.

```markdown
Hey I found issue at #23, which was fixed in #81. @ankitc1010 can you look into it?
```

>#### Result
>
Hey I found issue at #23, which was fixed in #81. @ankitc1010 can you look into it?

---
---

## 11. Special Thanks

<img src='https://pbs.twimg.com/profile_images/877525007185858562/7G9vGTca_400x400.jpg' width='100' height='100' style="border-radius: 200px;"/><br>

Special thanks to **Wes Bos**, as I often go through his tutorials.

---
---