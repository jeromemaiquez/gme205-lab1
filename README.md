# Project Title

GmE 205 - Laboratory Exercise 1

# How to set up the virtual environment

1. Create a folder on your computer and open it in your IDE (e.g., VS Code)
2. Open the terminal then create the virtual environment by running the following:
    ```
    py -m venv .venv
    .\.venv\Scripts\activate
    ```
3. Press ```Ctrl + Shift + P``` in VS Code, search for *Python: Select Interpreter*, then choose the interpreter inside the ```.venv``` folder
4. Install the required packages by running the following in the terminal:
    ```
    python -m pip install --upgrade pip
    pip install pandas matplotlib
    ```
5. (Recommended) List the installed packages via:
    ```
    pip freeze > requirements.txt
    ```

# How to run Python scripts

In the terminal, ensuring that ```(.venv)``` is present in the prompt, run the following:
    ```
    python <folder/script_name.py>
    ```

Edited on GitHub web interface

# Run Instructions

Lorem ipsum

# Reflection
- Abstraction: What did you choose to inspect, and why?

The script chose to inspect the number of points (rows) and attributes (columns), the number of missing values per attribute, the existence of the required columns ("lat" and "lon"), and whether the "lat" and "lon" values lie within  ±90 and ±180 degrees, respectively.

- Representation: What assumptions are you making about the CSV and coordinates?

By checking whether the "lat" and "lon" values lie within the aforementioned range of values, the script is assuming that the coordinates refer to geographic latitude and longitude. As such, it assumes that each row refers to a point on the Earth's surface.

- Responsibility: What should the script check automatically vs what a human should check?

It may be easier to have the script check for more basic errors (missing values, existence of required columns, correct range of values, etc.), while a human may be required to perform more open-ended checks (e.g., whether certain values or outcomes of processes are reasonable).

- Scale: What problems might happen if the dataset becomes very large?

While pandas DataFrames perform well in handling moderately large datasets, it may start having problems handling extremely large datasets (with millions of rows). Specific portions of the script may start running very slowly or perhaps even crash. This problem is worse for parts of the script that use loops, which handle each item (e.g., row) of an array (e.g., DataFrame) one by one.