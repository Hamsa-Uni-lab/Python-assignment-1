# Python-assignment-1
DESIGN
Below is a brief on my design for a solution to this assignment- to read a file containing a list of names of some kind, and generate three-letter abbreviations for each of the objects:

i.	Create a main() function and prompt for input file. This function is key to execute the whole program.
ASSUMPTION: Input file contains one name per line.
ii.	Read input file line by line and store as a list.
iii.	For each name, call process_name() function where:
a.	Values.txt - A list of alphabets and its value are read and stored as a dictionary.
b.	Each name is converted to Upper case, non-alphabetical characters ignored and split into different words.
c.	For each character in each word of the name, calculate the value based on the defined rules and create a list of values and store it in a list.
d.	Split the name into characters and store in another list.
e.	Using the list from step (d) and keeping the first character constant, create abbreviations of 3 letters using the remaining characters of the list in order. Calculate the abbreviations value by reading the value of each character from its corresponding list in step (d).
f.	Prepare a dictionary with abbreviation as key and the value of this abbreviation as the value to the key.
NOTE: Take care to retain different keys with same value. For repeating abbreviations retain the ones with least value.
g.	Create a list of abbreviations only. This will be used later to find repeating abbreviations and eliminate from the final output.
NOTE: Repeat step (iii) for each name in the input file and append the output to create a list of dictionaries and a list of abbreviations only.
iv.	Pass the output from step(iii) to process_sort() function where:
a.	Apply the counter() to the list of abbreviations, to find the repeating abbreviations and store these in a list.
NOTE: Import counter from collections to support the counter()
b.	Iterate through the list of abbreviations dictionary and delete key and its corresponding values from the abbreviations.
c.	On the  final dictionary list, for each dictionary return null(if no abbreviations) or return the key/keys with least value.
v.	Use the return from the previous step and print the output to a file in the format:
Name
Abbreviation
NOTE: 	Follow output file name convention. 
Print empty line in case no abbreviation is available for a name after all the processing steps.
Print all the abbreviations available with least value. 
