tasks = {}

def add_task(task):
    task_id = len(tasks) + 1
    tasks[task_id] = task
    print(f"Task added with ID: {task_id}")

def view_tasks():
    for task_id, task in tasks.items():
        print(f"{task_id}: {task}")

def delete_task(task_id):
    if task_id in tasks:
        del tasks[task_id]
        print(f"Deleted task {task_id}")
    else:
        print("Task ID not found")

while True:
    print("\n1. Add Task\n2. View Tasks\n3. Delete Task\n4. Exit")
    choice = input("Choose an option: ")

    if choice == "1":
        task = input("Enter task: ")
        add_task(task)
    elif choice == "2":
        view_tasks()
    elif choice == "3":
        task_id = int(input("Enter Task ID to delete: "))
        delete_task(task_id)
    elif choice == "4":
        break
    else:
        print("Invalid choice")
