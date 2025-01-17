


```OOP.python/

Baby ├- what you    have(attribute)+------------------------+
									| is_he_holding_toy = True|
									|rooms_to_play = [1,2]    |
									+-------------------------+

|
├-what you   do (methods)           +------------------------+
									| def play(room1, room2) |
									|def put_it_back(stop);  |
									+------------------------+


```


clases---->objcets
 e.g  Given a Class blueprint for a Car has the following attributes and methods, which line of code in the answers will produce an error?

**Attributes:**

`num_of_seats`

`speed`

**Methods:**

`drive()`

`brake()`

#Ans= car.brake() = 0
brake is a method, which means it's a function associated with the car object. We cannot assign a value to a function call.



Setting up Virtual enviroment 
1. in your folder path 
`python -m venv pythonAdvance`
2. Activate the Virtual Environment
3.`pythonAdvance\Scripts\activate`

4. `pip install notebook`
then `jupyter notebook

5. Deactivate the Virtual Environment (Optional)
		 `deactivate

# <span style=color:yellow>1.2 Encapsulation in Python</span>

is one of the fundamental concepts of object-oriented programming (OOP). It describes the idea of data encapsulation and the methods that work with data within a unit. It limits direct access to variables and methods and can prevent accidental modification of data.

<span style=color:yellow>public and private methods:</span>

Protected member is (in C++ and Java) accessible only from within the class and it’s subclasses.
By prefixing the name of your member with a single underscore, you are telling others “don’t touch this, unless you are a subclass”.

## <span style=color:yellow>1.3 The inheritance</span>[](http://localhost:8888/notebooks/01-Python/1.python_advanced/01.OOP/3.inheritance.ipynb#The-inheritance)

## Building a class from an already known one

Inheritance is an object feature that allows you to declare that a particular class will itself be modeled after another class, called the parent class.
## <span style=color:yellow>1.4 What is a static method in python?`</span>

Static methods are methods within a class that have no access to anything else in the class (no `self` keyword or `cls` keyword).

# <span style=color:yellow> 2.  Exception handling</span>
Exception handling in Python is a way to handle errors gracefully instead of letting your program crash when something goes wrong.

example:
- Trying to divide by zero (`ZeroDivisionError`)
- Accessing a variable that doesn’t exist (`NameError`)
- Trying to open a file that doesn’t exist (`FileNotFoundError`)

example 

`try:
	    num = int(input("Enter a number: "))
	    result = 10 / num
	    print(f"The result is {result}")
except ZeroDivisionError:
	    print("You cannot divide by zero!")`


# <span style=color:yellow>3 Regex (Regular Expressions)</span> 

Regex is a powerful tool for pattern matching and text processing in Python. It's part of the `re` module

### **Key Functions**


- **re.match()**: Matches the pattern at the **start** of the string.
    `re.match(r"\d+", "123abc")  # Matches "123"`
    
- **re.search()**: Searches for the pattern **anywhere** in the string.

    `re.search(r"\d+", "abc123")  # Matches "123"`
    
- re.findall()**: Returns **all matches** as a list.    
    `re.findall(r"\d+", "a1b2c3")  # Returns ['1', '2', '3']`
    
- **re.sub()**: Replaces all matches with a replacement string.
    `re.sub(r"\d+", "X", "a1b2c3")  # Returns "aXbXcX"`
### **Common Patterns**

- `.` : Any character except a newline.
- `\d` : Any digit (0–9).
- `\w` : Any word character (a–z, A–Z, 0–9, _).
- `\s` : Any whitespace (space, tab, newline).
- `^` : Start of the string.
- `$` : End of the string.
- `*` : 0 or more occurrences.
- `+` : 1 or more occurrences.
- `?` : 0 or 1 occurrence.
- `{n,m}`: Between `n` and `m` occurrences.



			import re 
			text = "Hello 123, this is a test." 
			# Find all numbers 
			numbers = re.findall(r"\d+", text) 
			print(numbers) # Output: ['123'] # Replace numbers with "X" 
			result = re.sub(r"\d+", "X", text) 
			print(result) # Output: "Hello X, this is a test." # Search for the                 first word 
			match = re.search(r"\w+", text) 
			if match: 
				print(match.group()) # Output: "Hello"


# <span style=color:yellow>4 File Handling </span>

File handling in Python allows you to perform operations like reading, writing, and appending data to files. It is done using built-in functions like `open()`

**Opening a File**:

- Syntax: `open(filename, mode)`
- Common modes:
    - `"r"`: Read mode (default).
    - `"w"`: Write mode (overwrites the file).
    - `"a"`: Append mode (adds to the end of the file).
    - `"r+"`: Read and write.
- Example 
	`with open("example.txt", "r") as file:
    `content = file.read() ` # Reads the entire file

### Benefits of `with` Statement:

- Automatically closes the file after use.
- Prevents resource leaks.
`



# <span style=color:yellow >Flask</span>


Flask is a **web framework** in Python. A web framework is like a toolbox that helps you build websites or web applications more easily.

Flask helps you:

- Receive user requests (like someone visiting your website or clicking a button).
- Decide what to do with those requests.
- Send back responses (like showing a webpage or sending data).


		`from flask import Flask
		
		app = Flask(__name__)  # Create a Flask app
		
		@app.route('/')  # Define a route for the homepage
		def home():
		    return "Hello, Flask!"  # Response sent to the browser
		
		if __name__ == '__main__':
		    app.run()  # Start the Flask app
`