# crossword_solver
Jupyter Python notebook to find solutions for monthly work crossword puzzle

Program takes in a prettify-ed HTML code block...
- First portion scrapes the text file based on pre-determined indicators and extracts both the clues and the crossword letters.
- Second portion goes through the keywords in order and scans the array of letters for a match to the first letter.
  Upon finding a match, it then looks in each of the 8 directions to see any match the second letter.
  If there is a second letter match, it then takes that direction vector and continues to look in that direction until either a 
  non-match or the word is completely identified.
- Once word is found, prints the word and the coordinates of the starting letter, and then moves on to the next word.
- Also prints out a copy of the puzzle with the used coordinates to aid in locating the sarting letter.

Possible improvements...
- Use the recursive vector loop immediately looking for the second letter, rather than looking for a letter and THEN going to
  recursive loop.
- Use a trie dictionary made up of the clues to search for every keyword in a single pass of the letter array, rather than cycling
  back through from the beginning for each new clue word.
