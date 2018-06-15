# Markup Guide

## Headings

To make headings use the following code snippet

```markdown
# This is heading 1

## This is heading 2
```

#### Result

# This is heading 1

## This is heading 2

## Bold, Italic and Strike Through

### Bold

To make text bold use the following code snippet

```markdown
This is **bold**
```

#### Result

This is **bold**

### Italic

To make text italic use the following code snippet

```markdown
This is _italic_
```

#### Result

This is _italic_

### Strike Through

To make a strikethrough use the following code snippet

```markdown
This is ~~strikethrough~~
```

#### Result

This is ~~strikethrough~~

## Linking

### Old School Method

In order to link a particular text to another document use the following snippet

```markdown
A link to [Google](http://www.google.co.in)
```

#### Result

A link to [Google](https://www.google.co.in)

### Old School with ToolTip

In order to attach a tooltip, on hover over the link attach a string with the link specified.

```markdown
A link to [Ankit's Github Account](https://github.com/ankitc1010, "Check out his awesome repositories")
```

#### Result

A link to [Ankit's Github Account](https://github.com/ankitc1010, "Check out his awesome repositories")

### Recommended Method

In order to create maintainable documentation assign a variable to the link specified and set its value at the bottom of the document.

```markdown
[Github][1] is an awesome place. In [Github][1] you can do awesome stuff.
Literally you can contribute to the open world projects of the organizations like [facebook][face], [google][goo], etc.
[Github][1] has now been acquired by [Microsoft][micro].

[1]: https://github.com
[face]: https://facebook.com
[goo]: https://google.co.in
[micro]: https://microsoft.com
```

#### Result

[Github][1] is an awesome place. In [Github][1] you can do awesome stuff.
Literally you can contribute to the open world projects of the organizations like [facebook][face], [google][goo], etc.
[Github][1] has now been acquired by [Microsoft][micro].

[1]: https://github.com
[face]: https://facebook.com
[goo]: https://google.co.in
[micro]: https://microsoft.com

## Images

### Oldschool Method

This is used to add images to your document.

```markdown
![This is the default text which is displayed if the image fails to load and can be left blank!](https://unsplash.it/500/500?random "This is Tooltip")
```

#### Result

![This is the default text which is displayed if the image fails to load and can be left blank!](https://unsplash.it/200/200?random "This is Tooltip and can be omitted altogether")

### Recommended Method

This is the recommended method to add image.

```markdown
![Cute Image][image]

[image]: https://unsplash.it/200/200?image=1012
```

#### Result

![Ocean Image][ocean]

[ocean]: https://unsplash.it/200/200?image=1015

### Using Nested Link

In this a smaller image is referring to its bigger resolution counterpart.

```markdown
[![](https://unsplash.it/50/50?image=1015)](https://unsplash.it/200/200?image=1015)
```

#### Result

[![](https://unsplash.it/50/50?image=1015)](https://unsplash.it/200/200?image=1015)

### Using HTML Tag in Nested Link

You can use html image tag in the above example and it will work the same.

```markdown
[<img src="https://unsplash.it/50/50?image=1015" alt='image'/>](https://unsplash.it/200/200?image=1015)
```

#### Result

[<img src="https://unsplash.it/50/50?image=1015" alt='image'/>](https://unsplash.it/200/200?image=1015)

### Using only HTML Tags To Display Image

There are limitations with respect to styling in markdown, so HTML can be used and corressponding style tags can also be added.

There is an update that Chrome and Firefox doesnt render < style /> tags. But they render inline styles.

```markdown
<img src="https://unsplash.it/500/500?image=1015" alt='cool image' style="width: 200px; height: 200px; border-radius: 200px;"/>
```

#### Result

<img src="https://unsplash.it/500/500?image=1015" id='cool' alt='cool image' style="width: 200px; height: 200px; border-radius: 200px;"/>

<style
  type="text/css">
#cool {
        border-radius: 200px;
    }
</style>

###
