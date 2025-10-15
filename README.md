# python-final-project
Fitness Tracker CLI Dashboard
This is a simple Command-Line Interface (CLI) application designed to help you track, save, and visualize your workout activities. It is built in Python using the pandas, matplotlib, and seaborn libraries. All data is stored in a CSV file, making it easy to manage and access your logs.

Features
Log Workouts: Add new entries with the date, workout type, time spent (in minutes), and calories burned.

Persistent Data Storage: All records are automatically saved to a .csv file (gym_members_exercise_tracking_synthetic_data.csv). If the file doesn't exist, it is created automatically.

View Summary Report: Get a quick overview of your progress, including total calories burned, average session duration, and the frequency of each workout type.

Search and Filter Logs: Search through your logs based on workout type and a specific date range (start and end dates).

Data Visualization: Generate insightful graphs and charts to understand your fitness data better:

Bar Chart: Displays the total time spent on each workout type.

Line Chart: Shows the trend of daily calories burned over time.

Pie Chart: Illustrates the distribution of different workout types.

Heatmap: Visualizes the correlation between workout duration and calories burned.

Requirements
To run this script, you will need to have the following Python libraries installed:

pandas

numpy

matplotlib

seaborn

You can install them using pip:

Bash

pip install pandas numpy matplotlib seaborn
How to Use
Save the Script: Save the provided code into a file, for example, fitness_tracker.py.

Open a Terminal/Command Prompt: Navigate to the directory where you saved the file.

Run the Script: Execute the following command:

Bash

python fitness_tracker.py
Use the Menu: Once the script is running, you will be presented with a menu. Choose an option by entering the corresponding number:

-----  Health Tracking Menu -----
1. Add Workout
2. View Report
3. Search Logs
4. Show Graphs
5. Quit
Enter option:
1. Add Workout: To log a new workout session. You will be prompted to enter the workout type, duration, and calories burned.

2. View Report: To see a summary of your overall progress.

3. Search Logs: To find specific records. You can filter by workout type and/or a date range.

4. Show Graphs: To see a visual representation of your data. A new window will open displaying the charts.

5. Quit: To exit the application.

Code Structure
FitnessDashboard Class: This is the core of the application. It handles all the methods for loading, adding, analyzing, and visualizing data.

_init_(self, file_name): Initializes the class and either loads or creates the CSV file.

add_entry(...): Adds a new workout record to the DataFrame and saves it to the CSV.

show_summary(): Prints a statistical summary of the data.

get_filtered_logs(...): Filters the records based on the given criteria.

plot_statistics(): Creates visual charts using matplotlib and seaborn.

if _name_ == "_main_": block: This is the entry point of the script. It runs a command-line menu loop that takes user input and calls the appropriate methods from the FitnessDashboard class.

Data Storage
All fitness data is stored in a file named gym_members_exercise_tracking_synthetic_data.csv, located in the same directory where the script is run. The file has the following structure:
