# To-Do-List
class Task:
    def __init__(self, name, description, due_date, status='Pending'):
        self.name = name
        self.description = description
        self.due_date = due_date
        self.status = status
tasks = []  # List to store tasks

def create_task(name, description, due_date):
    task = Task(name, description, due_date)
    tasks.append(task)

def list_tasks():
    for idx, task in enumerate(tasks, start=1):
        print(f"{idx}. {task.name} - {task.description} - Due Date: {task.due_date} - Status: {task.status}")

# Other functions like update_task, delete_task, etc.

def main():
    while True:
        print("\n1. Add Task\n2. List Tasks\n3. Exit")
        choice = input("Enter your choice: ")

        if choice == '1':
            name =input("Enter task name: ")
            description = input("Enter task description: ")
            due_date = input("Enter due date (YYYY-MM-DD): ")
            create_task(name, description, due_date)
            elif choice == '2':
            list_tasks()
        elif choice == '3':
            break
        else:
            print("Invalid choice. Try again.")

if __name__ == "__main__":
    main()
