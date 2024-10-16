# Lists

## Types of lists
1. Definition lists
2. Ordered lists
3. Unordered lists
4. Nested lists

## List tags

- `<dl>` - defines a description/definition list
- `<dt>` - defines a term in a description
- `<dd>` - describes the term in a description data
- `<ul>` - defines an unordered list
- `<ol>` - defines an ordered list
- `<li>` - defines a list item


### Definition list

```html
<html>
	<body> 
		<dl> 
			<dt>HTML</dt> 
				<dd>Hyper Text Markup Language</dd> 
			<dt>CSS</dt> 
				<dd>Cascade Style Sheet</dd>
		</dl>
	</body>
</html>
```

<html>
	<body> 
		<dl> 
			<dt>HTML</dt> 
				<dd>Hyper Text Markup Language</dd> 
			<dt>CSS</dt> 
				<dd>Cascade Style Sheet</dd>
		</dl>
	</body>
</html>
### Ordered list

```html
<html> 
	<body> 
		<h4>Numbered list:</h4> 
		<ol> 
			<li>Apples</li>
			 <li>Bananas</li> 
			 <li>Oranges</li> 
		</ol> 
		<h4>Letters list:</h4> 
		<ol type="A"> 
			<li>Lemons</li> 
			<li>Oranges</li> 
		</ol> 
	</body> 
</html>
```

<html> 
	<body> 
		<h4>Numbered list:</h4> 
		<ol> 
			<li>Apples</li>
			 <li>Bananas</li> 
			 <li>Oranges</li> 
		</ol> 
		<h4>Letters list:</h4> 
		<ol type="A"> 
			<li>Lemons</li> 
			<li>Oranges</li> 
		</ol> 
	</body> 
</html>

![](../../../assets/Images/Pasted%20image%2020240619142416.png)
> type attribute works with or without quotes
### Unordered list

```html
<html>
   <body>
      <h4>Unorderd lists:</h4>
      <ul>
         <li>Apples</li>
         <li>Bananas</li>
         <li>Lemons</li>
         <li>Oranges</li>
      </ul>
      <h4>Disk list:</h4>
      <ul type="circle">
         <li>Apples</li>
         <li>Bananas</li>
         <li>Lemons</li>
         <li>Oranges</li>
      </ul>
   </body>
</html>
```

<html>
   <body>
      <h4>Unorderd lists:</h4>
      <ul>
         <li>Apples</li>
         <li>Bananas</li>
         <li>Lemons</li>
         <li>Oranges</li>
      </ul>
      <h4>Disk list:</h4>
      <ul type="circle">
         <li>Apples</li>
         <li>Bananas</li>
         <li>Lemons</li>
         <li>Oranges</li>
      </ul>
   </body>
</html>


![](../../../assets/Images/Pasted%20image%2020240619143203.png)
### Nested lists

```html
<html>
   <body>
      <h4>A nested List:</h4>
      <ul>
	      <li>Coffee</li>
	      <li>
	         Tea 
	         <ul>
	            <li>Black tea</li>
	            <li>Green tea</li>
	            <ol>
	               <li>aaaaa</li>
	               <li>bbbbb</li>
	            </ol>
	         </ul>
	      </li>
	      <li>
	         Ice Cream 
	         <ol type="i">
	            <li>Vanila</li>
	            <li>Chocolate</li>
	            <li>Strowberry</li>
	         </ol>
	      </li>
      </ul>
	</body>
</html>

```

<html>
   <body>
      <h4>A nested List:</h4>
      <ul>
	      <li>Coffee</li>
	      <li>
	         Tea 
	         <ul>
	            <li>Black tea</li>
	            <li>Green tea</li>
	            <ol>
	               <li>aaaaa</li>
	               <li>bbbbb</li>
	            </ol>
	         </ul>
	      </li>
	      <li>
	         Ice Cream 
	         <ol type="i">
	            <li>Vanila</li>
	            <li>Chocolate</li>
	            <li>Strowberry</li>
	         </ol>
	      </li>
      </ul>
	</body>
</html>
---
# Tables

## Table tags

`<table>` - defines a table
`<th>` - defines a header cell in the table
`<tr>` - defines a row in a table
`<td>` - defines a cell in a table
`<caption>` - defines a table caption

## Table attributes

`colspan` - makes a cell span many columns
`rowspan` - makes a cell span many rows
`border` - specifies the size of the table border
`style` - use CSS to style the table


```html
<html>
   <body>
      <table style="width:100%" border="1">
	     <caption>Personal Information</caption>
         <tr>
            <th>Firstname</th>
            <th>Lastname</th>
            <th>Age</th>
         </tr>
         <tr>
            <td>Amila</td>
            <td>Fernando</td>
            <td>38</td>
         </tr>
         <tr>
            <td>Vajira</td>
            <td>Silva</td>
            <td>40</td>
         </tr>
         <tr>
            <td>Kapila</td>
            <td>Perera</td>
            <td>42</td>
         </tr>
      </table>
   </body>
</html>
```

<html>
   <body>
      <table style="width:100%" border="1">
	    <caption>Personal Information</caption>
         <tr>
            <th>Firstname</th>
            <th>Lastname</th>
            <th>Age</th>
         </tr>
         <tr>
            <td>Amila</td>
            <td>Fernando</td>
            <td>38</td>
         </tr>
         <tr>
            <td>Vajira</td>
            <td>Silva</td>
            <td>40</td>
         </tr>
         <tr>
            <td>Kapila</td>
            <td>Perera</td>
            <td>42</td>
         </tr>
      </table>
   </body>
</html>

![](../../../assets/Images/Pasted%20image%2020231216191211.png)

> Note that the caption for the table should be under the `table` tag definition

```html
<table style="width:60%" border="1"> 
	<caption>Personal Information</caption>
```

### Embed tags

```html
<embed type="image/jpg" src="pic_trulli.jpg" width="300" height="200">
<embed type="video/webm" src="video.mp4" width="400" height="300">
<embed type="text/html" src="snippet.html" width="500" height="200">
```

### Input tags

Attributes,
- `size` - the number of characters that will be displayed (width size)
- `maxlength` - the number of characters that is allowed in the input box

Different values that `type` accepts,
- `<input type="button">`
- `<input type="checkbox">`
- `<input type="color">`
- `<input type="date">`
- `<input type="datetime-local">`
- `<input type="email">`
- `<input type="file">`
- `<input type="hidden">`
- `<input type="image">`
- `<input type="month">`
- `<input type="number">`
- `<input type="password">`
- `<input type="radio">`
- `<input type="range">`
- `<input type="reset">`
- `<input type="search">`
- `<input type="submit">` (for a form)
- `<input type="tel">`
- `<input type="text">` (default value)
- `<input type="time">`
- `<input type="url">`
- `<input type="week">`
##### Radio buttons and Check boxes

| Radio button                                                                                                                                                                    | Check boxes                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| When a user selects one radio button, it automatically deselects any other radio buttons in the same group. This ensures that the user can choose only one option from the set. | Users can select multiple checkboxes simultaneously, and each checkbox operates independently of others. |
```html
<input type="radio" name="gender" value="male" checked> Male
<input type="radio" name="gender" value="female"> Female
```


<input type="radio" name="gender" value="male" checked> Male
<input type="radio" name="gender" value="female"> Female


```html
<input type="checkbox" name="fruit" value="apple" checked> Apple
<input type="checkbox" name="fruit" value="banana"> Banana
```

<input type="checkbox" name="fruit" value="apple" checked> Apple
<input type="checkbox" name="fruit" value="banana"> Banana

### Paragraph tag

Note that **after** each and every paragraph tag, a **blank line is being inserted** **before and after** the `<p>` tag.

```html
<p>Our evergreen school days<br/> will not come back again</p> 
<p>line 2</p>
<p> line  3</p>

```


![](../../../assets/Images/Pasted%20image%2020240111195548.png)

### Break tag

This will just add a new line, this won't insert a blank line. Just take the cursor to a new line.

### Button tag

Used to create a button. (for forms)
```html
<button type="submit">Submit</button>
```

<button type="submit">Submit</button>

### iframe tag

`<iframe>` tag specifies an inline frame.

```html
<iframe src="demo_iframe.htm" style="height:200px;width:300px;" title="Iframe Example"></iframe>
```


### select tag
This tag is used to create a drop down menu

```html
<label for="cars">Choose a car:</label>  
  
<select name="cars" id="cars">  
  <option value="volvo">Volvo</option>  
  <option value="saab" selected>Saab</option>  
  <option value="mercedes">Mercedes</option>  
  <option value="audi">Audi</option>  
</select>
```

<label for="cars">Choose a car:</label>  
  
<select name="cars" id="cars">  
  <option value="volvo">Volvo</option>  
  <option value="saab" selected>Saab</option>  
  <option value="mercedes">Mercedes</option>  
  <option value="audi">Audi</option>  
</select>

### section tag

This is used to add a hyperlink to a specific section of your code.

```html
<section id="target-section">
	<h2>Target Section</h2>
</section>
<a href="#target-section">Go to Target Section</a>
```


### font tag

- To change the color of the letters
```html
<font color="red">font Color is changed to red</font>
```

<font color="red">font Color is changed to red</font>

- To change the size of the letters
```html
<p><font size="1" > Size of the font is changed to 1 </font></p> 
<p><font size="2" > Size of the font is changed to 2 </font></p>
```
<p><font size="1" > Size of the font is changed to 1 </font></p> 
<p><font size="2" > Size of the font is changed to 2 </font></p>
- To change font type
```html
<p><font face="verdana">font type is changed to "verdana"</font></p> 
<p><font face="Algerian">font type is changed to "Algerian"</font></p>
```
<p><font face="verdana">font type is changed to "verdana"</font></p><p><font face="Algerian">font type is changed to "Algerian"</font></p>



### Map tag

This creates an image with a clickable link.

```html
<img src="workplace.jpg" alt="Workplace" usemap="#workmap" width="400" height="379">

<map name="workmap">
  <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm">
  <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.htm">
  <area shape="circle" coords="337,300,44" alt="Cup of coffee" href="coffee.htm">
</map>
```

![](../../../assets/Images/Pasted%20image%2020240119191506.png)

We create a map with a name and then  we use the `img` tag with the attribute `usemap` to specify the map

When we click on a certain area of the image, we go to different pages. Those co-ordinates are specified in the `map`

### Marquee tag

- marquee with different widths
```html
<marquee width = "50%"> 50% width of page</marquee>
```
<marquee width = "50%"> 50% width of page</marquee>

#### href attributes

We can use both URLs and relative paths with this attribute.

```html
<a href="https://example.com/"> </a>
<a href="hello.png"> </a>
```