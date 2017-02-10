# Homework #2

## Instructions
---

1. Setup your initial route at `/` to return `'Hello World'`.

	***Example***: A GET request to `localhost:5000/` would return `'Hello World'`.


2. Build a route called `/birthday` that returns your birthday as a `string` in this format: `'October 30 1911'`.

	***Example***: A GET request to `localhost:5000/birthday` returns `'October 30 1911'` (Use your birthday instead)


3. Build a route called `/greeting` that accepts a parameter called `name`.  The route should return a string
that says `'Hello <name>'` where `<name>` is the name that you passed to the route.  

	***Example***: A GET request to `localhost:5000/greeting/ben` would return 'Hello ben!'
    
4. Modify your home route (`/`) to return the html template provided below.
	* Create a folder called `templates` in the root of your project's directory.
	* Create a file called `home.html` in the templates directory.
	* Paste the HTML shown below into `home.html` and save.
	* In your main server file modify the `flask` import line to say: `from flask import Flask, render_template`
	* In your home (`/`) route `return render_template('home.html')`.
	* Navigate to `localhost:5000/` and you should see the rendered HTML.
	
Your file structure should look like this:
```
 project-name/
 --server.py (or whatever you named your python script)
 --templates/
 ---- home.html
 --venv/
```
    
Paste this HTML into `home.html`.

```
<!DOCTYPE html>
<html>
  <body>
    <img src="https://lambdaschool.com/static/assets/images/lambda.png">
    <h1>Congrats!</h1>
    <h3>You just served your first webpage.</h3>
    <p>This page is pretty bare right now but these are the fundamentals that all websites are built on.  Later in the course we will teach you some basic HTML, CSS, and Javascript so that you can structure more sophisticated pages with more detailed designs and complex functionality</p>
    <p>Our full time and part time courses will go much more in depth as to what it takes to build the same kinds of web applications that you know and love.  We will be covering the cutting edge frameworks used by industry leaders to create high performant and beautiful applications.</p>
  </body>
</html>
```
---

### Extra Credit

1. Create a route called `/sum` that adds two parameteres together and returns them.
	* `localhost:5000/sum/5/10` would return `'15'`
	* You will need to convert the parameters to integers using `int()`
	* Example: `fiveAsInt = int('5')` => `fiveAsInt == 5`
	* You then have to convert the `int` back into a `string` using `str()`
	* Example: `fiveAsString = str(5)` => `fiveAsString == '5'`
	* You can also prefix the parameter with the keyword `int` => `<int:param>`. Make sure you turn it back into a `string`

2. Create a route called `/multiply` and a route called `/subtract` 
	* `localhost:5000/multiply/6/5` would return `'30'`
	* `localhost:5000/subtract/25/5` would return `'20'`
	* Make sure you are converting the parameters to `int`s and returning a `string`

3. Create a route called `/favoritefoods` that returns a `list` of your favorite foods
	* A `list` is a collection of different values. => `['football', 'basketball', 'rugby']`
	* The server must return a string so we need to convert our list into a string.
	* One common string format for sending complex data is `JSON`.
	* Change the top line of your server file to `from flask import Flask, render_template, jsonify`
	* Pass your `list` to `jsonify()` when returning it. `return jsonify(myList)`

---
#### Congratulations on finishing Homework #2
Apply to our full time or part time immersive program to learn cutting edge technologies that are used by top technology companies around the world.

Our part time and full time courses are 13 intense weeks of focused study on the most relevant technologies.  

Class sizes are small to ensure that each student gets individual attention from our world class instructors to help them succeed.

For more information visit: https://lambdaschool.com
