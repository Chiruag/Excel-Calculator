#Excel Calculator

I have made a simple makefile that makes the executable and also has a command called clean that will clean all the unnecessary files.

To run the code there must be two files present, inp.txt and in.txt.

inp.txt contains the queries that need to be executed, in.txt contains the info of all the values of the spreadsheet.

lexer.mll is the lexer that creates tokens, parser.mly is the parser that contains the grammar and calls the functions which have been defined in functions.ml. The main file is calc.ml and the executable file is called ass4.

The lexer creates the tokens which is sent to the parser with the grammar,the parser also initialises the sheet.

The functions are in functions.ml file.

I have assumed the sheet to be a cell array array where cell is a datatype which can be "Nothing" or a float. The functions have been documented in the functions.ml file.

The general apprach towards the max/avg/sum/min/count functions was that there is a functions which is a helper function that calculates the value and the main function just assigns that value to the particular cell. These functions(the ones that calculate the value) use recursion to calculate the values, these function have O(n) time complexity.

For the add_const and add_range type queries there is a loop(2 loops in case of add_range) that calculate and assign the value to the corresponding cells.
