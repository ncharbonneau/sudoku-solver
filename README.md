# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: The Naked Twins problem is a constraint propagation strategy that can be used to reduce the number of possible values in other boxes in a unit in order to facilitate the identification of values in each box of a Sudoku grid. For all units, after finding out the occurrence of naked twins, we are eliminating these numbers as possible values for other boxes of the same unit. The elimination process goes like this: First, use a loop to go through each unit of unitlist; Then, find the boxes that have two possible values for each unit; Next, produce a list of possible twin pairs; Proceed with loop again through the list of possbile twin pairs to evaluate if there are naked twin pairs; In the eventuality that there was naked twin pairs, Eliminate the naked twin values in each unit; Finally, proceed to the next unit of unitlist until reaching the end of the unitlist.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: The diagonal Sudoku problem is adding a new constraint which allows the values from 1 to 9 only once for all 9 boxes on each of the 2 diagonals on the Sudoku grid. In order to solve the diagonal Sudoku problem, we need to first create a list of diagonal units for each of the 2 diagonals; Then, we need to add the diagonal units to the unitlist; Finally, we just revert to the regular procedure to solve a Sudoku grid.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solution.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Submission
Before submitting your solution to a reviewer, you are required to submit your project to Udacity's Project Assistant, which will provide some initial feedback.  

The setup is simple.  If you have not installed the client tool already, then you may do so with the command `pip install udacity-pa`.  

To submit your code to the project assistant, run `udacity submit` from within the top-level directory of this project.  You will be prompted for a username and password.  If you login using google or facebook, visit [this link](https://project-assistant.udacity.com/auth_tokens/jwt_login for alternate login instructions.

This process will create a zipfile in your top-level directory named sudoku-<id>.zip.  This is the file that you should submit to the Udacity reviews system.

