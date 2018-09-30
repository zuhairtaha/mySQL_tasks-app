# mySQL_tasks-db
```
#Find out how many tasks are in the task table
SELECT
  COUNT(*) AS tasks_count
FROM task;

#Find out how many tasks in the task table do not have a valid due date
SELECT
  COUNT(task.id) AS tasks_count_task_do_not_have_a_valid_due_date
FROM task
WHERE task.due_date IS NULL;

#Find all the tasks that are marked as done
SELECT
  task.title AS task_title,
  status.name AS task_status
FROM task
  INNER JOIN status
    ON task.status_id = status.id
WHERE status.name = 'done'

#Find all the tasks that are not marked as done
#Get all the tasks, sorted with the most recently created first
#Get the single most recently created task
#Get the title and due date of all tasks where the title or description contains database
#Get the title and status (as text) of all tasks
#Get the name of each status, along with a count of how many tasks have that status
#Get the names of all statuses, sorted by the status with most tasks first
```
