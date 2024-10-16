- MCQ
1. 4
2. 2
3. 2
4. 1
5. 1
6. 4
7. 2
8. 1
9. 5
10. 1
11. 2
12. 1
13. 3 ?
14. 4
15. 2
16. 2
17. 5
18. 2
19. 5
20. 1
21. 3
22. 1
23. 5
24. 1
25. 2 ?
26. 1
27. 5
28. 3 ? countries?
29. 3
30. 5
31. 2
32. 1
33. 2
34. 1
35. 3
36. 2
37. 2
38. 4
39. 4
40. 1
41. 3
42. 2
43. 4
44. 1
45. 5

- Essay
#### 2011

a)

```html
<h1 style="color:red"></h1>
```
Here the `h1` tag is the element and the `style` is the attribute

b) 

i) element 
ii) attribute 
iii) attribute 
iv) element

24. 
```css
p { font-family: 'arial'; font-size: 14px, color: blue; }
```

25. This will include the image `elephants_tnl.jpg` with no borders and given sizes, and when it's clicked the image `elephants.jpg` will be opened in the window.

26. 
```html
<input type="radio">Blue Whale</input>
<input type="radio">Leopard</input>
<input type="radio">Elephant</input>
```

27. 
```html
<table> 
	<caption>Wild Sri Lanka</caption>
	<tr>
		<th>Days</th>
		<th>Price</th>
	</tr>
	<tr>
		<td>7</td>
		<td>US$910</td>
	</tr>
	<tr>
		<td>10</td>
		<td>US$1220</td>
	</tr>

</table>
```

#### 2012

a. It would add a blank line after the text in the paragraph is displayed. 
b.
```
Our evergreen school days
will not come back again
............................................
From the nursery to high school we learnt the best
```

c. 
```html
<html>
<head>
    <title>AgriSL</title>
</head>
<body>
    <h1>Agriculture in Sri Lanka</h1>
    <img src="agriSL.jpg">
    <p> Sri Lanka is an agricultural country. Agriculture is one of the main sectors of Sri Lankan economy.</p>

    <p>The main plantation crops are</p>
    <ul>
        <li>tea</li>
        <li>rubber</li>
        <li>coconut</li>
    </ul>

    <p>Links to agricultural firms</p>
    <a href="http://www.jayagrotec.com">Jay Agro Technologies</a><br>
    <a href="http://www.lkagrisys.com ">Lanka Agri Systems Pvt Ltd.</a>
</body>
</html>
```

#### 2013

1. 

```html
1. title
2. /title
3. h1
4. /h1
5. hr
6. u
7. /u
8. h6
9. /h6
10. ul
11. /ul
12. h4
13. /h4
14. img src="cricket.jpg" alt="cricket"
15. table
16. caption
17. /caption
```


#### 2014

1) a)

```html
<dt>CPU</dt>
	<dd>Central Processing Unit</dd>

<dt>ROM</dt>
	<dd>Read Only Memory</dd>
```


b) 
i) `<abc>Greetings!</abc>`
ii) Greetings!

c)

```html
<form method="GET" action="">
	<input type="checkbox" name="prg-lang" value="c"> C
	<input type="checkbox" name="prg-lang" value="java"> Java
	<input type="checkbox" name="prg-lang" value="python"> Python
</form>
```


#### 2015

a)

```
1. "text"
2. textarea
3. /textarea
4. Send your message
```

b) 

i) The given image is not found in the system.
ii) The browser can't access the URL to the remote URL provided for the image.
ii) Source link incorrect, browser doesn't support images, problem in downloading images, image has been corrupted.

c) 
	i) correct, wrong 
	ii) correct, wrong
	iii) correct

#### 2016

1) a)
	i) Open `coverPage.jpg` in a new tab once clicked
	ii) Open `content.html` in the same tab once clicked
	iii) Open `figures.html` in the same frame and open `figures.jpg` in the same tab once clicked

b) 
```
External CSS
Internal CSS
Inline CSS
```

c) 

```css
<style>
	h2 { color: red; text-align: center; }
	p {font-family: 'courier new'; font-size: 14px}
</style>
```


#### 2017

6. a)

```html
<!DOCTYPE html>
<html>
<head>
    <title>Information</title>
    <style>
        li { font-family: 'Calibri'; font-size: 14px; color: red;}
    </style>
</head>
<body>
    <h1>Student Art Competition</h1>
    <br>
    <h2>Theme: Litter on the environment</h2>
    <h3>PRIZES</h3>
    <ul type="square">
        <li>1st place Rs. 10,000/=</li>
        <li>2nd place Rs. 7,500/=</li>
        <li>3rd place Rs. 5,000/=</li>
    </ul>
    <h3>ENTRY FORM</h3>

    <p>Please fill and submit this <a href="form.html" taget="_blank">online entry form</a> to the competition.</p>
</body>
</html>
```


b)

```html
<!DOCTYPE html>
<html>
<head>
    <title>ENtry Form</title>

</head>
<body>
    <h1>Art Competition Online Entry</h1>
    <br>
    <h2>Theme: Litter on the environment</h2>

    <form method="POST" action="/">
        Name: <input name="name"> <br><br>
        Gender: <input name="gender" type="radio" value="Male"> Male
        <input name="gender" type="radio" value="Female"> Female

        <br><br>
        <label for="grade">Grade Category</label>
        
        <select name="grades">
            <option value="g-1-2">Grade 1 - 2</option>
            <option value="g-3-6">Grade 3 - 6</option>
            <option value="g-7-10">Grade 7 - 10</option>
            <option value="g-11-13">Grade 11- 13</option>
        </select>

        <p>Art media:</p>
        <input type="checkbox" value="water_colours"> Water Colours<br>
        <input type="checkbox" value="colour_pencils"> Colour Pencils<br>
        <input type="checkbox" value="crayon"> Crayon<br>
        <input type="checkbox" value="chalk"> Chalk<br>

        <br>
        <button onclick="refreshTab()"> Clear your Entries</button>
        <br><br>
        <button type="submit">Sbmit</button>
    </form>

    <script>
        function refreshTab() {
            // Reload the current page
            location.reload();
        }
    </script>
</body>
</html>
```


#### 2018

1. 
a)
i) 
```
Ability to change the appearance of a web page. 
Ability to make the web page more user friendly and attractive 
```

ii)


<u>Important Sites</u>

<ul>
	<li> <a href="www.nie.lk/index.html">National Institute of Education </a> </li>
	<li> <a href="www.doenets.lk/exams/index.html"> Department of Examinations </a> </li>
</ul>

iii)

<center> Department of Examinations <br> Pelawattta <br> Battaramulla </center><hr>



b) 

```css
h1 {
	color: blue;
	text-align: center;
	font-family: 'arial';

}

p {
	backgtound-color: yellow;
	font-size: 12px;
}
```

c)

```
1. form
2. type
3. text
4. id
5. type
6. radio
7. name
8. value
9. type
10. radio
11. name
12. value
13. select
14. name
15. value
16. Colombo
17. value
18. Jaffna
19. value
20. Matara
21. select
22. type
23. button
24. Submit
25. form
```



### 2019

1.
a)
i)

<p> Social networking has <br> <u> advantages</u> and disadvantages </p>

ii)

<table border="1">
<caption>Schedule</caption>
<tr>
<th>Time</th>
<th>Event</th>
</tr>
<tr>
<td>8 am</td>
<td>Drama</td>
</tr>
<tr>
<td>10 am</td>
<td>News</td>
</tr>
<tr> <td colspan=2>Lunch</td></tr>
</table>

b)
i)
```
Reduce code complexity
Can apply the same style for multiple web pages.
```

ii)
```css
p, h1, h2 {
	color: red;
	font-family: 'Calibri';
}

p, h2 { text-align: justify }
```

c)

```
1. "school_db"
2. "admin"
3. 'A!2*t'
4. INSERT
5. student
6. name
7. class
8. $sql
```

### 2020

1. a)

<table border=1>
    <tr>
        <th>No</th>
        <th>Type</th>
        <th>City</th>
    </tr>
    <tr>
        <td>1</td>
        <td rowspan="2">High</td>
        <td>Galle</td>
    </tr>
    <tr>
        <td>2</td>
        <td>Jaffna</td>
    </tr>
</table>

b)

i) 8 - Green, 9 - Blue
ii) Style can be applied to multiple tags easily and with fewer lines of code. 
iii) 
	a) `h1 {color : green; }`
	b) `#appear {font-family: 'arial';}`


c)

i) D,B,A,C
ii)
```
Code:P1/Item:Pen
Code:P2/Item:Book
```



### 2021

1. a)

i)
```html
2. background-color="green"
4. url="#one"
5. </a>
6. <!-- Section 1 --!>
8. </hr>
```
ii)
```html
4 - <a href='#ICT'>A/L Student Section</a>
7 - <section id="ICT"> A/L ICT</section>
```

b)

i)
```css
.art { font-size: 14px; text-align: center}
h1 { color: yellow; }
```
ii)
```html
<link rel="stylesheet" type="text/css" href="neat"> 
```

c)

i)
```html
1. dl
2. ul
3. ul
4. dd
5. dd
6. dd
7. dd
8. dl
9. fieldset
10. select
11. select
12. textarea
13. textarea
14. "checkbox"
15. "checkbox"
16. button
17. fieldset
```
ii)
```html
<option value="b" checked> Team B</option>
```

### 2022/2023

