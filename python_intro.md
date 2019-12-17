# Python Intro

Due Date: Nov 30, 2019 → Dec 07, 2019
Github/Link: https://github.com/bakabrooks/dsp/tree/master/lessons/python_intro
Module (if applicable): Metis - Python
Program: Metis Pre-Work
Status: Completed 🎉
Tags: General Python, Metis

# 🧠 Recall

Write three lambda functions for any use case.

Write a function that takes two strings as input and determines if they are annograms.

# 📝 Notes

### Collections

- Tuple = ( )
    - Immutable, ordered
    - Tuples can be used as keys in dictionaries because they are immutable
- List = [ ]
    - Mutable, ordered
- Set = { }
    - Unique values
    - Can't index
- Dictionaries → key/value pairs
    - Think of them like a tree diagram
    - Iterating over dicationaries:

        `for key in career_stats.keys():`

        `for val in career_stats.values():`

        `for key, val in career_stats.items():`

### Documentation

- Comment code often → comments used or single tasks within script/notebook
- Use docstrings to define functions

### Functions

- DO NOT COPY AND PASTE! Create functions instead
- Remember that any zero or "empty" (empty list, empty string, etc.) evaluate to "False" in boolean logic.

    if len(a_list) > 0: #bad way to write this
    	print('you dumbass')
    
    if a_list: #use this bc an empty list would be false
    	print('yay')

- Example list comprehension:

    new_list = [x + 1 for x in a_list if x > 2]

- Use `sorted()` or `.sort()` to sort collections, though you should almost always use `sorted()`
    - `sorted()` creates a copy of the collection you put into the parentheses (does not modify it in place)
- Options for sorting:

    #sort in reverse order
    print(sorted(alumni, reverse=True))
    
    #sort on the second column
    print(sorted(alumni, key=lambda row: row[2]))

### Error Handling

- Input custom error message:

    if len(class_list) % 2 != 0:
    	raise ValueError('list hsould have an even no. of elements')

- Can also use `assert` to determine if something is working correctly

    def sum_up_a_list(list_to_sum):
    	"""
    	Takes a list of numbers and returns the sum
    	"""
    	assert type(list_to_sum) == list, "Input must be a list"
    	return sum(list_to_sum)
    
    print(sum_up_a_list(3))

- Use try/except blocks to help guide with potential errors in code

    def check_if_number(value):
    	try:
    		return int(value)
    	except:
    		return print("NOT A NUMBER")

**SUMMARY:** Collections, documentation, functions, and error handling = how to write clean, in-production code. Get these things down to make your code reproducible and actually used in practice (rather than just the analysis you're used to).