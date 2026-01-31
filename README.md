# Project Title

# How to set up the virtual environment

# How to run Python scripts

Edited on GitHub web interface

# Run Instructions

# Reflection
- Abstraction: What did you choose to inspect, and why?

The script chose to inspect the number of points (rows) and attributes (columns), the number of missing values per attribute, the existence of the required columns ("lat" and "lon"), and whether the "lat" and "lon" values lie within  ±90 and ±180 degrees, respectively.

- Representation: What assumptions are you making about the CSV and coordinates?

By checking whether the "lat" and "lon" values lie within the aforementioned range of values, the script is assuming that the coordinates refer to geographic latitude and longitude. As such, it assumes that each row refers to a point on the Earth's surface.

- Responsibility: What should the script check automatically vs what a human should check?

It may be easier to have the script check for more basic errors (missing values, existence of required columns, correct range of values, etc.), while a human may be required to perform more open-ended checks (e.g., whether certain values or outcomes of processes are reasonable).

- Scale: What problems might happen if the dataset becomes very large?

While pandas DataFrames perform well in handling moderately large datasets, it may start having problems handling extremely large datasets (with millions of rows). Specific portions of the script may start running very slowly or perhaps even crash. This problem is worse for parts of the script that use loops, which handle each item (e.g., row) of an array (e.g., DataFrame) one by one.