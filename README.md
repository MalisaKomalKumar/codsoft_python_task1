# codsoft_python_task1
#This is my Task 1 as an intern at codsoft ,  This is a program written in the Python language (TO-DO List)

import collections

# Initialize an empty list to store tasks
tasks = []

# Function to add tasks to the list
def add_task(task):
  task = input("Enter a task to add (or 'q' to quit): ")
  if task.lower() != 'q':  # Check if the user wants to quit
    tasks.append(task)
    print(f"Task '{task}' added successfully!")
  else:
    print("Exiting...")

# Function to display the tasks in the list
def view_tasks():
  if tasks:
    print("Your To-Do List:")
    for i, task in enumerate(tasks, start=1):  # Enumerate for task numbering
      print(f"{i}. {task}")
  else:
    print("Your to-do list is empty.")

# Main function to handle user interaction
if __name__ == "__main__":
  while True:
    choice = input("Enter 'a' to add a task, 'v' to view tasks, or 'q' to quit: ")
    if choice.lower() == 'a':
      add_task("")  # Empty string to prompt for input
    elif choice.lower() == 'v':
      view_tasks()
    elif choice.lower() == 'q':
      break
    else:
      print("Invalid choice. Please try again.")
