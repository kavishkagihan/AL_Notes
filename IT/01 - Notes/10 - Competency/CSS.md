- CSS describes how HTML elements are to be displayed on screen, paper, or in other media
- For easy maintenance and update web pages, style sheets guarantees the consistency throughout the website, can restyle the HTML without modifying it, a single document can be presented in multiple styles.


# Selectors

```
CSS selectors are used to "find" (or select) HTML elements based on their element name, id, class, attribute, and more
```

There are a couple of different selectors.
1. element selector - here we find the element using the element name i.e `div`, `p`

```css
p { text-align: center; color: red; }

 <p>Me too!</p>
```

2. id selector - here we find the element by giving it a `id` attribute

```css
#para1 { text-align: center; color: red; }

<p id="para1">Hello World!</p>
```

3. class selector - here we find the element by the class its in

```css
 .center { text-align: center; color: red; }

<h1 class="center">Red and center-aligned heading</h1> 
<p class="center">Red and center-aligned paragraph.</p>
```

Here, this style will be applied to both `h1` and `p` tags as the class is set as `center`

If we want to be specific of what element we want to center using the class, we can use it like this 

```css
p.center { text-align: center; color: red; }

<h1 class="center">This is not affected</h1> 
<p class="center">Red and center-aligned paragraph.</p>
```

In this case, the `h1` won't be affected as in the CSS we are specifying it to **only affect `p` elements in the `center` class**.

4. group selectors - here we can specify multiple tags to have the same style

```css
 h1, h2, p { text-align: center; color: red; }

<h1>Hello World!</h1> 
<h2>Smaller heading!</h2> 
<p>This is a paragraph.</p>
```

In here, we can specify all the tags that have the same style once. So here all `h1`, `h2` and `p` tags will be affected.

> When it comes to the order or interpreting them, **whatever is defined first will be applied to elements.**

```html
<html>
<head> 
 <style> .hehe { color: red; }; p { color: green; } </style>
 
</head>
<body>
 <p class="hehe"> hello </p>
</body>
</html>
```
![](../../../assets/Images/Pasted%20image%2020240619150531.png)

Here since the `hehe`, id selector is defined first for color red, that will be applied regardless of having a p element selector after 

# Inserting CSS

There are three ways to insert CSS
- External style sheet
- Internal style sheet
- Inline style

#### External style sheet

With external style sheets, we can change the look of the entire web page. We use the `link` tags to include the style sheet. **This should be included under the `head` tags**


```html
<head> 
	<link rel="stylesheet" type="text/css" href="mystyle.css"> 
</head>
```

###### **Advantages of external styling**
- Less code lines to manage (modification in one place)
- Same style can be applied to multiple web pages
- Reduce code complexity
#### Internal style sheet

An internal style sheet may be used if one single page has a unique style. These should be specified inside `style` tags. **These should also be included under the `head` tags**

```html
<head> 
	<style> 
		body { background-color: red; } 
		h1 { color: maroon; margin-left: 40px; } 
	</style> 
</head>


<body> 
	<h1>This is a heading</h1>
	<p>This is a paragraph.</p> 
</body>
```
![](../../../assets/Images/Pasted%20image%2020240619151133.png)
Here the style will be applied to only the `h1` tag, not the `p`
#### Inline style

This is used to specify style to a single tag in the body. **This is included under the `style` attribute of elements**

```html
<body> 
	<h1 style="color:blue;margin-left:30px;">This is a heading</h1> 
	<p>This is a paragraph.</p> 
</body>
```

Here the style will be applied to the `h1` tag

## Cascading Order

If we were to use all these inserting types in a single document, there is a specific order that the styles will be shown. From the highest priority to lowest, it looks like this.
1. Inline style (inside an HTML element)
2. External and internal style sheets (in the head section)
3. Browser default

I.e say you have `h1` colour set to `red` in a external style sheet for the entire web page. But in one `h1` tag, its color to `blue` is changed by inline style. That means the inline style will take priority and change it to `blue`


```html
<h1> this will be red </h1>
<h1 style="color:blue"> this will be blue </h1>
```


# Misc

- Embed an image in the background
```css
body {
    background-image: url("school.png");
}
```

- Color representation

```html
<h1 style="background-color:rgb(255, 99, 71);">RGB</ h1>
<h1 style="background-color:#ff6347;">Hexa decimal</h1>
```