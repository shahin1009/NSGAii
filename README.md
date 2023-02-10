## Table of contents:

    Introduction
        Purpose of the NSGAii Jupyter Notebook
        Description of the Non-dominated Sorting Genetic Algorithm (NSGA-II)
        Overview of Multi-Objective Test Problems (MOTPs)

    Libraries Used
        Explanation of the libraries used in the implementation of the NSGA-II algorithm

    Utility Functions
        Overview of the utility functions used in the implementation of the NSGA-II algorithm
        Explanation of the purpose and usage of each utility function

    Main Program
        Overview of the main program
        Explanation of the steps involved in the implementation of the NSGA-II algorithm

    Plotting the Results
        Explanation of how the results of the NSGA-II algorithm are visualized

    Usage
        Explanation of how to use the NSGAii Jupyter Notebook.

## NSGAii

The NSGAii Jupyter Notebook is an implementation of the Non-dominated Sorting Genetic Algorithm (NSGA-II), which is a multi-objective optimization algorithm. The NSGA-II algorithm is used to find a set of non-dominated solutions from a population of solutions, where each solution is evaluated based on multiple objectives. The algorithm is applied to the Multi-Objective Test Problems (MOTPs) and the results are visualized in 2D plots.
Libraries Used

The algorithm is implemented in Python and uses the following libraries:

    numpy for numerical computations
    matplotlib for visualizing the results
    random for generating random numbers

## Utility Functions

The notebook includes several utility functions that are used throughout the implementation of the NSGA-II algorithm. These functions are:

    generate_random_pop: This function generates a random population of solutions, where each solution is represented as an array of decision variables.
    
    crowding_distance: This function calculates the crowding distance of a set of solutions, which is used as a measure of diversity in the population. The crowding distance is used to maintain diversity in the population as the algorithm progresses through generations.
    
    sort_by_values: This function sorts a list of solutions based on the values of one of their objectives.
    
    fast_non_dominated_sort: This function performs the non-dominated sorting step of the NSGA-II algorithm. It separates the solutions into different levels of non-domination and returns a list of indices for each level.
    
    calculate_crowding_distance: This function calculates the crowding distance for each solution in a set.
    
    crowded_comparison_operator: This function compares two solutions based on their crowding distance and their rank in the non-dominated sorting process.

## Main Program

The main program of the NSGAii notebook is divided into the following steps:

    Initialization: A random population of solutions is generated.
    
    Non-dominated Sorting: The solutions are sorted into different levels of non-domination using the fast_non_dominated_sort function.
    
    Crowding Distance Calculation: The crowding distance is calculated for each solution in the population using the calculate_crowding_distance function.
    
    Parent Selection: Parents are selected for mating based on their crowding distance and their rank in the non-dominated sorting process, using the crowded_comparison_operator function.
    
    Mating: The parents are mated to produce offspring, which are used to replace the least crowded solutions in the population.
    
    Environmental Selection: The solutions from the previous generation and the new offspring are combined to form a new population, which is then used for the next iteration.
    
    Termination: The algorithm terminates when a specified number of generations have been completed.

## Plotting the Results

The results of the NSGA-II algorithm are visualized using the matplotlib library. The results are displayed in 2D plots, where each solution is represented as a point in the plot. The solutions are colored based on their level of non-domination, and the plots show the distribution of solutions in the population. The plot also highlights the Pareto front, which is the set of non-dominated solutions that represent the optimal trade-off between the objectives. The Pareto front is typically visualized as a line in the plot, with the solutions on the line representing the most optimal solutions.

By visualizing the results in this way, it is possible to see the trade-off between the objectives and to understand the relationships between the solutions. The plots also provide a clear representation of the diversity of the solutions in the population, which is important for maintaining diversity and avoiding premature convergence in the optimization process.

## Usage

To use the NSGAii notebook, you will need to have Jupyter Notebook installed on your system. You can download Jupyter Notebook from here.

Once you have Jupyter Notebook installed, you can download the NSGAii.ipynb file from the GitHub repository and open it in Jupyter Notebook.

The parameters of the algorithm, such as population size, number of generations, etc., can be modified in the Main Program section of the notebook.

After making any necessary changes, you can run the cells in the notebook to see the results. The results will be visualized in 2D plots, showing the non-dominated solutions obtained by the NSGA-II algorithm.
Note

This implementation is just for educational purposes and there might be better and more optimized implementations available. It is recommended to thoroughly understand the NSGA-II algorithm and its underlying principles before using this implementation.
